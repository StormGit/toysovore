<template>
    <div id="app">
        <div class="row" id="topBar">
            <div class="col-sm-6 col-12">
                <div class="logo-zone">
                    <router-link to="/">
                        <img width="75" alt="Logo Toysovore" src="./assets/sceau.png">
                        <div class="brand">TOYSOVORE</div>
                    </router-link>
                </div>
            </div>
            <div class="col-sm-6">
                <div class="nav-bar" id="nav">
                    <router-link to="/">Info</router-link>
                    <router-link to="/portfolio">My Work</router-link>
                    <router-link to="/coloring">Coloring Pages</router-link>
                    <a href="https://society6.com/stormfr" target="_blank">Shop</a>
                </div>
            </div>
        </div>

        <div id="main">
            <router-view/>
        </div>

        <FooterTemplate></FooterTemplate>

    </div>
</template>

<script>
    import FooterTemplate from './components/Footer.vue'

    export default {
        components: {
            FooterTemplate
        }
    }
</script>

<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
    @import '../styles/responsive.scss';

    @font-face {
        font-family: 'Moon Get';
        src: url('./assets/fonts/moon_get-Heavy.otf') format('truetype');
        font-weight: 900;
        font-style: normal;
    }

    @font-face {
        font-family: 'Quick Sand';
        src: url('./assets/fonts/Quicksand_Book.otf') format('truetype');
        font-weight: 300;
        font-style: normal;
    }

    @font-face {
        font-family: 'Quick Sand';
        src: url('./assets/fonts/Quicksand_Bold.otf') format('truetype');
        font-weight: 900;
        font-style: normal;
    }

    body {
        background: url("./assets/lightpaperfibers.png");
        padding: 0 10%;
    }

    a {
        color: #2c3e50;
        text-decoration: none;

        &:hover {
            color: #d20b10;
            text-decoration: none;
        }

        &:focus, &:active {
            color: inherit;
        }
    }

    #app {
        font-family: 'Moon Get', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
    }

    .page-title {
        text-align: center;
        margin: 30px 0;
        font-family: 'Quick Sand';
        font-size: 3em;
        color: #d20b10;
        text-transform: uppercase;
    }

    #nav {
        font-family: 'Quick Sand';
        font-size: 15px;
        line-height: 102px;
        float: right;
        margin-right: 15px;
        font-size: 15px;

        a {
            text-transform: uppercase;
            margin: 0 10px;
            color: #b5b5b5;
            text-decoration: none;

            &.router-link-exact-active {
                color: #d1060c;
                font-weight: 900;
            }
        }
    }

    .logo-zone {
        margin-top: 15px;
        padding-left: 15px;
        float: left;
    }

    .brand {
        vertical-align: middle;
        font-size: 25px;
        padding: 0 0 0 20px;
        display: inline-block;
    }

    .subtitle {
        font-family: "Quick Sand";
        text-transform: capitalize;
        color: #d20b10;
        text-align: center;

        a {
            color: #d20b10;
        }

        font-size: 25px;
        padding: 30px 0;
    }

    .sub-content {
        margin-top: 70px;
    }


</style>


