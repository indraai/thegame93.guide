<template>
  <div id="app">
    <img alt="#TheGame93 logo" src="./assets/logo.png">
    <HelloWorld msg="TheGame93.guide"/>
  </div>
</template>

<script>

  window.watsonAssistantChatOptions = {
    integrationID: "ead378d0-eaca-4fe2-bc42-1d87237f69bd", // The ID of this integration.
    region: "us-south", // The region your integration is hosted in.
    serviceInstanceID: "9adf5250-d2d1-450c-a115-6c9b3cb786ed", // The ID of your service instance.
    carbonTheme: 'g90',
    onLoad: function(instance) {
      instance.on({type:'receive', handler: obj => {
        console.log('RECEIVE FROM WATSON: ', obj);
      }}).on({type:'send', handler: obj => {
        console.log('SEND TO WATSON: ', obj);
      }});

      instance.updateCSSVariables({
        'BASE-z-index': '8000',
        'BASE-font-family': '"Source Code Pro", monospace',
        'BASE-header-font-family': '"Neuropol X", sans-serif',
        'HOME_SCREEN-greeting-font-family': '"Source Code Pro", sans-serif',
        '$focus': '#ff0000'
      });

      instance.render();
    }
  };
  setTimeout(function(){
    const t=document.createElement('script');
    t.src="https://web-chat.global.assistant.watson.appdomain.cloud/loadWatsonAssistantChat.js";
    document.head.appendChild(t);
  });


import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="stylus">
// import adobe fonts
@require './assets/vars.styl'

body
  background-color: lighten(black, 5%)
  color: $colors.lightYellow
  font-size: 14px

footer
  display: block
  text-align: center
  margin: 3rem
  font-family: $textFont

  a
    color: $colors.babyBlue;
#app
  font-family: $textFont;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;

#WACContainer
  &.WACContainer
    .WAC__sent
      box-shadow: 0 3px 9px rgba(0,0,0,.5)
    .WACLauncher__ButtonContainer
      transition: all .3s ease
      border-radius: 50% !important
      box-shadow: 0 3px 9px rgba(0,0,0,.5) !important
      overflow: hidden

      &:enabled:active
        box-shadow: inset 0 0 9px rgba(255,255,255,.5) !important
    button
      &.WAC__button--primary
        border-radius: 50%
        transition: all .3s ease
        overflow: hidden
        border-radius: 50% !important

        &:enabled:active
        &:focus
          box-shadow: 0 1px 3px rgba(0,0,0,.5) !important
          border: none !important


    .WACWidget
      &.WACWidget
        box-shadow: none !important
      &.WACWidget--launched
        &.WACWidget--defaultElement
          box-shadow: 0 3px 9px rgba(0,0,0, .5) !important
          overflow: hidden
    .WAC__inputContainer
      .WAC__TextArea
        textarea.WAC__TextArea-textarea
          transition: all .3s ease
          color: $colors.mintGreen
          &:focus
            border: none !important
</style>
