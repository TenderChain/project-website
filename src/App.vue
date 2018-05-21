<template>
  <div id="app">
    <landing-page/>
    <feed-page/>
    <contact-page/>
  </div>
</template>

<script>
import LandingPage from './components/Landing'
import FeedPage from './components/Feed'
import ContactPage from './components/Contact'

import ScrollMagic from "scrollmagic"

export default {
  name: 'App',
  components: {
    LandingPage,
    FeedPage,
    ContactPage
  },
  mounted () {
		var controller = new ScrollMagic.Controller({
			globalSceneOptions: {
				triggerHook: 'onLeave'
			}
		});

		// get all slides
		var slides = document.querySelectorAll(".view");

		// create scene for every slide
		for (var i=0; i<slides.length; i++) {
			new ScrollMagic.Scene({
					triggerElement: slides[i]
				})
				.setPin(slides[i])
				.addTo(controller);
		}
  }
}
</script>

<style lang="scss">
  .view{
    height: 100vh;
    width: 100%;
    h1{
      text-align: center;
      padding-top: 35vh;
    }
  }
  html, body {
    height: 100%;
    margin: 0;
    padding: 0;
  }
</style>
