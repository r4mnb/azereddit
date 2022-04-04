# Qız qalası
1-TamperMonkey uzantisini browserinize elave edin : [Tamper Monkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en) <br />
2-Uzantilar bolmesinden Tampermonkey iconuna sağ click edin. <br />
3-"Create New Script" veya "Yeni Betik ekle" <br />
4-Bu kodu kopyalayin ve açılan pəncərəyə yapışdırın: <br />
```
// ==UserScript==
// @name         r/azerbaijan qiz qalasi
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  try to take over the canvas!
// @author       r4mnb
// @match        https://hot-potato.reddit.com/embed*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=reddit.com
// @grant        none
// ==/UserScript==
if (window.top !== window.self) {
    window.addEventListener('load', () => {
            document.getElementsByTagName("mona-lisa-embed")[0].shadowRoot.children[0].getElementsByTagName("mona-lisa-canvas")[0].shadowRoot.children[0].appendChild(
        (function () {
            const i = document.createElement("img");
            i.src = "https://github.com/r4mnb/azereddit/blob/main/map.png";
            i.style = "position: absolute;left: 0;top: 0;image-rendering: pixelated;width: 2000px;height: 1000px;";
            console.log(i);
            return i;
        })())

    }, false);

}
```
5- Daha sonra r/place girin ve Azerbaycan bayrağının sağ alt hissesindeki xanaları sırası ilə rəngləyin
