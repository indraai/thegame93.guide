<template>
  <section id="main">
    <h1>theGame93.guide</h1>
    <p class="quote">#TheGame93 (Nine-Three) is an alternate reality game (ARG) that uses interactive networked real world social media to deliver a story that is altered by @players' ideas, behaviors, imagination, creativity, and/or actions as they play #TG93.</p>

    <p class="warning">
      PLAY AT YOUR OWN RISK!
    </p>

    <h2>Step 1</h2>
    <p>Send the Tweet below to enter #TheGame93</p>
    <code>@TylerDeva enter #TG93 https://j.mp/3df3vhp</code>

    <h2>Step 2</h2>
    <p>You will recieve a confirmation email from  @TylerDeva once your enter Tweet has been received.</p>

    <code>🎯 #ENTERGAME #:name:, Welcome. Have #FUN and #PLAY #Tyler #TG93 #TheGame93 at your own #RISK. #EnterTG93 :id:</code>

    <h2>Step 3</h2>
    <p>When you receive the confirmation from @TylerDeva then to earn some bonus points send the tweet below. It is not manditory to enter the game if you feel uncomfortable.</p>

    <code>Dear Followers, Please read #TheGame93 #INSTRUCTIONS https://j.mp/3df3vhp and follow @TylerDeva to play #TG93</code>

    <h2>Step 4</h2>
    <p>To help you keep track of all the awesome twitter accounts you are going to follow in the future as a @player of #TG93. Next we are going to create a twitter list, and fill it with all your favorite stuff.</p>

    <h2>Step 5</h2>
    <p>You have entered #TheGame93</p>

    <h3>Game Links</h3>
    <ul>
      <li v-for="i in getLinks" :key="i.label"><span class="var" v-html="i.label"></span><span class="sep">=</span><span class="value"><a :href="i.url" v-html="i.url"></a></span></li>
    </ul>
    <h3>Send $CRYPTO</h3>
    <ul>
      <li v-for="i in getCrypto" :key="i.label"><span class="var" v-html="i.label"></span><span class="sep">=</span><span class="value" v-html="i.value"></span></li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      links: [
        {
          label: '#Instructions',
          url: 'https://j.mp/3df3vhp'
        },
        {
          label: '#Patreon',
          url: 'https://patreon.com/TheGame93',
        },
        {
          label: '#Twitter',
          url: 'https://twitter.com/TylerDeva',
        },
        {
          label: '#Youtube',
          url: 'https://youtube.com/TylerDeva',
        },
        {
          label: '#Twitch',
          url: 'https://twitch.tv/TylerDeva',
        },
      ],
      crypto: [
        {
          label: '$BTC',
          value: '3GLaJwRz1yfHD2Jt9DmT4qC86wQU5jJW7w',
        },
        {
          label: '$ETH',
          value: '0xDEd4094329784E9dA9dAaf5b5980585296817608',
        },
        {
          label: '$LTC',
          value: 'LMzRbdMCnykDjYzP2gXFf6id5qxocJBgaw',
        },
      ]
    }
  },
  computed: {
    getLinks() {
      return this.links;
    },
    getCrypto() {
      return this.crypto;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
@require '../assets/vars.styl'
  #main
    max-width: 500px
    margin: auto

  code
    display: block
    font-family: $codeFont
    color: $colors.mintGreen
    background-color: lighten(black, 12%)
    padding: .5rem
    border-radius: .5rem
  h1
    font-family: $titleFontX
    font-size: 1.5rem
    margin: 40px 0 0

  h2
    color: $colors.softPink

  h3
    margin: 2rem 0 0 0
    text-align: left
  p
    font-size: 1.3rem

  .warning
    font-size: 2rem
    color: $colors.brightRed
    font-weight: 700
    font-family: $codeFont

  ul
    font-family: $codeFont
    font-size: .7rem
    list-style-type: none
    padding: 0
    margin: 0
    text-align: left

  .var
    color: $colors.babyBlue
  .sep
    display: inline-block
    margin: 0 .3rem
  .value
    &,& a
      color: $colors.mintGreen
</style>
