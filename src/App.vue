<template>
  <div id="fb-root"></div>
  <div id="layout">
    <a href="#menu" id="menuLink" class="menu-link  tada">
      <span></span>
    </a>
    <div id="menu">
      <div class="pure-menu">
        <ul class="pure-menu-list">
          <li class="pure-menu-item"><a href="/random" class="pure-menu-link">random</a></li>
          <li class="pure-menu-item"><a href="/set" class="pure-menu-link">set</a></li>
          <li class="pure-menu-item"><span onclick="SaveGame()" class="pure-button">💾 Save</span></li>
          <li class="pure-menu-item menu-item-divided "><a href="mailto:sha.egor@gmail.com" class="pure-menu-link"><small>sha.egor@gmail.com</small></a></li>
          <ul>
            <li class="pure-menu-item">
              <a  class="pure-menu-link" href="https://goshva.github.io/snakeword/ar/">Arabian</a>
            </li>
            <li class="pure-menu-item">
              <a  class="pure-menu-link" href="https://goshva.github.io/snakeword/">English</a>
            </li>
            <li class="pure-menu-item">
              <a  class="pure-menu-link" href="https://goshva.github.io/snakeword/fr/">French</a>
            </li>
            <li class="pure-menu-item">
              <a  class="pure-menu-link" href="https://goshva.github.io/snakeword/de/">Немецкий</a>
            </li>
            <li class="pure-menu-item">
              <a  class="pure-menu-link" href="https://goshva.github.io/snakeword/ru/">Русский</a>
            </li>
          </ul>
          <div class="fb-share-button" data-href="https://boggle.space/url?edge=9&amp;letters=[%22%D0%BE%22,%22%D1%86%22,%22%D1%82%22,%22%D1%83%22,%22%D0%B6%22,%22%D0%B0%22,%22%D0%B7%22,%22%D0%B0%22,%22%D1%81%22,%22%D0%BC%22,%22%D0%B5%22,%22%D0%BD%22,%22%D0%B4%22,%22%D0%B8%22,%22%D0%B3%22,%22%D1%81%22,%22%D0%BA%22,%22%D0%B2%22,%22%D0%BE%22,%22%D0%BE%22,%22%D0%B2%22,%22%D0%BE%22,%22%D1%8C%22,%22%D0%B0%22,%22%D0%BE%22,%22%D1%8D%22,%22%D0%BE%22,%22%D1%82%22,%22%D1%80%22,%22%D0%BF%22,%22%D0%B5%22,%22%D0%BB%22,%22%D0%BB%22,%22%D0%BA%22,%22%D0%B0%22,%22%D1%85%22,%22%D0%B8%22,%22%D0%BF%22,%22%D0%B0%22,%22%D0%BD%22,%22%D1%8C%22,%22%D0%BF%22,%22%D0%B3%22,%22%D0%BF%22,%22%D1%83%22,%22%D0%BF%22,%22%D0%B8%22,%22%D0%BA%22,%22%D0%B8%22,%22%D1%89%22,%22%D0%B8%22,%22%D0%BC%22,%22%D1%8F%22,%22%D0%B4%22,%22%D0%B0%22,%22%D0%B9%22,%22%D0%B0%22,%22%D0%BA%22,%22%D0%BE%22,%22%D0%BD%22,%22%D0%B0%22,%22%D1%81%22,%22%D0%B7%22,%22%D0%B3%22,%22%D1%8B%22,%22%D0%BD%22,%22%D1%82%22,%22%D0%BE%22,%22%D0%B0%22,%22%D1%82%22,%22%D1%8C%22,%22%D0%B7%22,%22%D0%B8%22,%22%D0%BC%22,%22%D0%B5%22,%22%D0%BB%22,%22%D0%BF%22,%22%D1%82%22,%22%D0%B8%22,%22%D1%87%22,%22%D0%B0%22]&amp;userwordsids=[[32,23,14],[14,23,32,33,34],[15,24,33],[24,33,24]]" data-layout="button_count" data-size="large" data-mobile-iframe="true"><a class="fb-xfbml-parse-ignore" target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fboggle.space%2Furl%3Fedge%3D9%26letters%3D%255B%2522%25D0%25BE%2522%252C%2522%25D1%2586%2522%252C%2522%25D1%2582%2522%252C%2522%25D1%2583%2522%252C%2522%25D0%25B6%2522%252C%2522%25D0%25B0%2522%252C%2522%25D0%25B7%2522%252C%2522%25D0%25B0%2522%252C%2522%25D1%2581%2522%252C%2522%25D0%25BC%2522%252C%2522%25D0%25B5%2522%252C%2522%25D0%25BD%2522%252C%2522%25D0%25B4%2522%252C%2522%25D0%25B8%2522%252C%2522%25D0%25B3%2522%252C%2522%25D1%2581%2522%252C%2522%25D0%25BA%2522%252C%2522%25D0%25B2%2522%252C%2522%25D0%25BE%2522%252C%2522%25D0%25BE%2522%252C%2522%25D0%25B2%2522%252C%2522%25D0%25BE%2522%252C%2522%25D1%258C%2522%252C%2522%25D0%25B0%2522%252C%2522%25D0%25BE%2522%252C%2522%25D1%258D%2522%252C%2522%25D0%25BE%2522%252C%2522%25D1%2582%2522%252C%2522%25D1%2580%2522%252C%2522%25D0%25BF%2522%252C%2522%25D0%25B5%2522%252C%2522%25D0%25BB%2522%252C%2522%25D0%25BB%2522%252C%2522%25D0%25BA%2522%252C%2522%25D0%25B0%2522%252C%2522%25D1%2585%2522%252C%2522%25D0%25B8%2522%252C%2522%25D0%25BF%2522%252C%2522%25D0%25B0%2522%252C%2522%25D0%25BD%2522%252C%2522%25D1%258C%2522%252C%2522%25D0%25BF%2522%252C%2522%25D0%25B3%2522%252C%2522%25D0%25BF%2522%252C%2522%25D1%2583%2522%252C%2522%25D0%25BF%2522%252C%2522%25D0%25B8%2522%252C%2522%25D0%25BA%2522%252C%2522%25D0%25B8%2522%252C%2522%25D1%2589%2522%252C%2522%25D0%25B8%2522%252C%2522%25D0%25BC%2522%252C%2522%25D1%258F%2522%252C%2522%25D0%25B4%2522%252C%2522%25D0%25B0%2522%252C%2522%25D0%25B9%2522%252C%2522%25D0%25B0%2522%252C%2522%25D0%25BA%2522%252C%2522%25D0%25BE%2522%252C%2522%25D0%25BD%2522%252C%2522%25D0%25B0%2522%252C%2522%25D1%2581%2522%252C%2522%25D0%25B7%2522%252C%2522%25D0%25B3%2522%252C%2522%25D1%258B%2522%252C%2522%25D0%25BD%2522%252C%2522%25D1%2582%2522%252C%2522%25D0%25BE%2522%252C%2522%25D0%25B0%2522%252C%2522%25D1%2582%2522%252C%2522%25D1%258C%2522%252C%2522%25D0%25B7%2522%252C%2522%25D0%25B8%2522%252C%2522%25D0%25BC%2522%252C%2522%25D0%25B5%2522%252C%2522%25D0%25BB%2522%252C%2522%25D0%25BF%2522%252C%2522%25D1%2582%2522%252C%2522%25D0%25B8%2522%252C%2522%25D1%2587%2522%252C%2522%25D0%25B0%2522%255D%26userwordsids%3D%255B%255B32%252C23%252C14%255D%252C%255B14%252C23%252C32%252C33%252C34%255D%252C%255B15%252C24%252C33%255D%252C%255B24%252C33%252C24%255D%255D&amp;src=sdkpreparse">Поделиться</a></div>
        </ul>
      </div>
    </div>
  </div>
    <div id="content">
      <div id="main">
        <div class="header">
          <div class="pure-form" style="display: flex; justify-content: center">
            <span class="pure-button pure-button-active" id="points"
              title="0">...
            </span>
            <select id="word" class="pure-input-3-5">
              <option></option>
            </select>
            <span class="pure-button pure-button-active" id="clear"
              title="">&#9003;✗</span>
          </div>
        </div>
        <hr>
        <div class="content">
          <div id="gameplace"></div>
          <ul class="pure-menu-list" id="gametally"></ul>
          <div id="result"></div>
        </div>
      </div>
      <div class="gallery pure-form" style="position: fixed; top: 50%; left: 50%;"></div>
    </div>      
     <!--
      <script type="application/javascript" defer src="./js/classes.js"></script>
      <script type="application/javascript" defer src="./js/gameCtrl.js"></script>
      <script type="application/javascript" defer src="./js/genRandom.js"></script>
      <script type="application/javascript" defer src="./js/dictionary.js"></script>
      <script type="application/javascript" defer src="./js/pure.js"></script>
     -->
</template>

<script>
export default {
  components: {
    
  }
}
</script>
