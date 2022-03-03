<template>
    <main>
        <nav class="navbar navbar-expand-lg navbar-light" style="background: #A9A9A9;">
        <a class="navbar-brand text-white" href="#"><img src="~/static/assets/logo.png" width="30" height="30" class="d-inline-block align-top" alt="">YOMART</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item active">
                                    <NuxtLink to="/" class="text-white cd-md-3">
                                        Home
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/product" class="text-white col-md-3">
                                        Product
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/contact" class="text-white col-md-3">
                                        Contact
                                    </NuxtLink>
                                </li>
            </ul>
        </div>
        </nav>
    </main>
</template>
