<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-12">
        <nav-header @pageWasChanged="currentPage = $event"></nav-header>
        <keep-alive>
          <component :is="currentPage"></component>
        </keep-alive>
        <cc-footer>
          <p class="text-center" slot="app-name">&copy; {{ appName }}</p>
          <nav>
            <ul class="nav justify-content-center">
              <li class="nav-item"><a class="nav-link">Home</a></li>
              <li class="nav-item"><a class="nav-link">About Us</a></li>
              <li class="nav-item"><a class="nav-link">Contact Us</a></li>
            </ul>
          </nav>
        </cc-footer>
      </div>
    </div>
  </div>
</template>

<script>
import FirebaseConfig from './firebaseConfig.js';
import Header from './components/Header.vue';
import CardFront from './components/card/CardFront.vue';
import CardBack from './components/card/CardBack.vue';
import CardInsideLeft from './components/card/CardInsideLeft.vue';
import CardInsideLeftRight from './components/card/CardInsideRight.vue';
import Footer from './components/Footer.vue';

export default {
  data: function() {
    return {
      currentPage: 'cardFront',
      appName: 'Creative Cards'
    }
  },
  components: {
    navHeader: Header,
    cardFront: CardFront,
    cardBack: CardBack,
    cardInsideLeft: CardInsideLeft,
    cardInsideRight: CardInsideLeftRight,
    ccFooter: Footer
  }
}
</script>

<style>
  body {
    font-family: Verdana, Geneva, sans-serif;
    color: #333;
  }

  a {
    cursor: pointer;
  }
</style>
