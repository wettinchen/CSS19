## Chapter 19: Pseudo
It is my coding practice with the TUTORIAL of Dave Gray. 

## Source
### Dave Gray 的 CSS 資源
https://github.com/gitdagray/css_course

### Dave Gray 的 CSS 課程
https://youtube.com/playlist?list=PL0Zuz27SZ-6Mx9fd9elt80G1bPcySmWit

### Dave Gray 的 YouTube 頻道
https://www.youtube.com/@DaveGrayTeachesCode

## Quick Concept outline
###  1. Intro
        教學影片固定的開頭

###  2. Welcome
        歡迎觀眾，說明工具與資料位置

###  3. Pseudo-Classes vs Pseudo-Elements
        將 nav a 改為 nav a:link

###  4. Starter Code
        初始設定說明

###  5. :active
        設定 nav a:active 文字為紅色。

###  6. :is
        使用 nav is() 改寫 nav a:hover, nav a:focus

###  7. :any-link
        使用 nav a:any-link 取代 nav a:link, nav a:visited

###  8. Specificity with :is and :where
        (1)設定 header, footer 改為 :is(header, footer)，選擇器特異性為(0, 0, 1)。
        (2)設定 :is(header, footer) 改為 :is(header, footer, .card)，選擇器特異性提高為(0, 1, 0)。
        (3)設定 header 文字顏色為紅色，選擇器特異性為(0, 0, 1)。
        (4)設定 :is(header, footer, .card) 改為 :is(header, footer)，選擇器特異性提高為(0, 0, 1)。
        (5)設定 :is(header, footer) 改為 :is(header, footer, .card)，選擇器特異性為(0, 0, 0)。

###  9. :target
        設定 .card:target 的 border 為 2px solid rebeccapurple，點擊名字時，對準的邊界會變為紫色。

### 10. :not
        (1)設定 .card img[alt] 中，border 為 10px solid red，選取有 alt 屬性的圖像
        (2)修改.card img[alt] 為 .card img:not([alt])，顯示沒有 alt 屬性的圖像

### 11. :nth-child
        (1)設定 .card:nth-child(2) 選取 html 的第二個元素，背景為 papayawhip。
        (2)修改 .card:nth-child(odd) 選取 html 的所有奇數元素，背景為 papayawhip。
        (3)修改 .card:nth-child(even) 選取 html 的所有偶數元素，背景為 papayawhip。

### 12. Create a pseudo-element
        設定 .card figcaption::after 在名字與職稱後添加 hello

### 13. Emoji pseudo-elements
        在名字與職稱後添加 ✨，display 為 block

### 14. Fancy quotes with ::before and ::after
        (1)使用 .card figcaption::after 改為 .card figcaption::before，修改✨在名字與職稱前
        (2)使用 .card p::before，content 為 open-quote，在文字段落前添加上引號；
         .card p::after，content 為 close-quote，在文字段落後添加下引號
        (3)使用 .card p::before，
        設定符號大小為 3em，position 為 absolute，top 為 -0.25em，left 為 -0.5em；
        設定 .card p 的 position 為 relative；
        設定 .card p::after，符號大小為 3em，position 為 absolute，top 為 -0.25em，right 為 -0.5em；刪除 q 標籤
        (4) header, footer ，
        設定 z-index 為 1，使 header, footer 在上引號和下引號上層。

### 15. ::first-letter
        (1)使用 .card figcaption::first-letter，設定第一個字母大小為 3rem，但✨不是文字，沒有變化。
        (2)將 .card figcaption::before 改為 .card figcaption::after，名字的第一個字母大小變為 3rem。

### 16. ::first-line
        使用 .card figcaption::first-line，設定第一行大小為 3rem
