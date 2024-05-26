<script>
export default {
    name: "AppFooter",
    data() {
        return {
            cards: [
                {
                    text: "DIGITAL COMICS",
                    search: "/card-dc.png",
                },
                {
                    text: "DC MERCHANDISE",
                    search: "/merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    search: "/subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    search: "/shop-locator.png",
                },
                {
                    text: "DC POWER VISA",
                    search: "/dc-power-visa.svg",
                },
            ],

            images: [
                {
                    src: "/footer-facebook.png",
                },
                {
                    src: "/footer-twitter.png",
                },
                {
                    src: "/footer-youtube.png",
                },
                {
                    src: "/footer-pinterest.png",
                },
                {
                    src: "/footer-periscope.png",
                },
            ],

            linksDcComics: [
                "CHARACTERS",
                "COMICS",
                "MOVIES",
                "TV",
                "GAMES",
                "COLLECTIBLES",
                "VIDEOS",
                "FANS",
                "NEWS",
            ],

            linksDc: [
                "CHARACTERS",
                "COMICS",
                "MOVIES",
                "TV",
                "GAMES",
                "COLLECTIBLES",
                "VIDEOS",
                "FANS",
                "NEWS",
                "CHARACTERS",
                "COMICS",
                "MOVIES",
            ],

            linksSites: [
                "DC",
                "MAD MAGAZINE",
                "DC KIDS",
                "DC UNIVERSE",
                "DC POWER VISA",
            ],
        }
    },

    methods: {

    },

    mounted() {

    }
}
</script>

<template>
    <!-- Suddivido Footer in 3 sezioni header main e footer -->
    <footer>
        <!-- Aggiuto header del footer con le img e il background azzurro -->
        <div id="footer-top" class="my-bg py-3">
            <div class="container row m-auto justify-content-evenly align-items-center p-0">
                <div class="col-12 col-sm-6 col-md-4 col-lg-2  p-0" v-for="card in cards">
                    <div class="row m-0 align-items-center py-3">
                        <figure class="col-4 m-0 p-0">
                            <img :src="card.search" alt="" class="img-fluid">
                        </figure>
                        <h5 class="col-8 m-0 my-fs p-1">
                            {{ card.text }}
                        </h5>
                    </div>
                </div>
            </div>
        </div>
        <!-- aggiungo il main del footer con background image e link vari -->
        <div id="footer-center" class="bg-image">
            <div class="container row m-auto p-0">
                <div class="col-12 col-sm-2 p-2">
                    <h3 class="m-0 fs-5">DC COMICS</h3>
                    <ul class="p-0">
                        <li v-for="link in linksDcComics">
                            <a :href="link" class="text-decoration-none my-fs">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                    <h3 class="m-0 fs-5">SHOP</h3>
                    <ul class="p-0">
                        <li>
                            <a href="#" class="text-decoration-none my-fs">Shop DC</a>
                        </li>
                        <li>
                            <a href="#" class="text-decoration-none my-fs">Shop DC Collectibles</a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-sm-2 p-2">
                    <h3 class="m-0 fs-5">DC</h3>
                    <ul class="p-0">
                        <li v-for="link in linksDc">
                            <a :href="link" class="text-decoration-none my-fs">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-sm-2 p-2">
                    <h3 class="m-0 fs-5">SITES</h3>
                    <ul class="p-0">
                        <li v-for="link in linksSites">
                            <a :href="link" class="text-decoration-none my-fs">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-sm-6 p-0 overflow-hidden">
                    <img id="logo-dc" src="/dc-logo-bg.png" alt="" class="img-fluid">
                </div>
            </div>
        </div>
        <!--  aggiungo footer del footer con bottone a sinistra e a destra le varie img social -->
        <div id="footer-bottom" class="py-4 my-bg-footer">
            <div class="container row m-auto justify-content-between align-items-center">
                <div class="col-12 col-sm-2 text-center text-md-start">
                    <button type="button" class="btn btn-outline-info text-white">SIGN-UP NOW!</button>
                </div>
                <div class="col-12 col-sm-8 text-center text-md-end">
                    <span class="text-primary p-1 my-fs">FOLLOW US</span>
                    <img :src="img.src" alt="" v-for="img in images" class="px-2">
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
a {
    color: gray;
}

.my-bg {
    background-color: #0282F9;
}

#logo-dc {
    transform: scaleY(1.60);
}

.my-bg-footer {
    background-color: #303030;
}

.bg-image {
    background-image: url(/public/footer-bg.jpg);
    background-size: cover;
}
</style>