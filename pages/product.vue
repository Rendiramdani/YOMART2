
<template>
<main>
<navbar/>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <h1>Products</h1>
        <div class="row">
          <div class="col-md-12">
            <div v-if="loading" class="text-center">
              <img src="~/static/assets/loading.gif" alt="">
            </div>
          </div>
          <div v-for="produk in products" :key="produk.id" class="col-md-4">
            <div class="card mb-4">
              <div class="card-header">
                <img :src="produk.foto" width="95%" class="img-thumb">
              </div>
              <div class="card-body">
                <h4>{{ produk.nama }}</h4>
                <h4>Rp{{ produk.harga }}</h4>
                <a :href="produk.link_eksternal" class="btn btn-success btn-block">Beli di whatsapp</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      products: '',
      loading: true,
    }
  },
  mounted() {
    this.getProducts()
    // console.log(this.$supabase)
  },
  methods: {
    async getProducts() {
      let {data, error} = await this.$supabase
        .from('tb_produk')
        .select()
      if(data) 
      this.products = data
      this.loading = false
      if(error) console.error(error)
    }
  }
}
</script>
