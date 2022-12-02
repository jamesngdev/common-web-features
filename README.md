// ==UserScript==
// @name         Cheat TLU
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://itest.tlu.edu.vn
// @icon         https://www.google.com/s2/favicons?sz=64&domain=facebook.com
// @grant        none
// ==/UserScript==

(function () {
    'use strict';
    const chatboxElement = document.createElement('div');
    chatboxElement[removed] = `
    <div xss=removed id="cheat_chatbox">
        &lt;iframe src="https://minnit.chat/itesttlu?embed&&nickname=" width='1000' height='500' style="border:none;"
                allowTransparency="true"&gt;&lt;/iframe&gt;
        <br>
    </div>`;
    document.body.appendChild(chatboxElement);

    const toggleChatbox = () => {
        const cheatFrame = document.getElementById('cheat_chatbox');
        console.log("cheat frame", cheatFrame)
        const visibility = cheatFrame.style.visibility;
        if (visibility === 'visible') {
            cheatFrame.style.visibility = 'hidden';
        } else {
            cheatFrame.style.visibility = 'visible';
        }
    }

    [removed] = function (e) {
        e = e || window.event;
        // use e.keyCode
        console.log(e);
        if (e.code === 'Space') {
            toggleChatbox();
        }

    };

})();



https://www.tampermonkey.net/
