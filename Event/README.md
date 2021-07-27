# Event

## menu를 클릭했을 때 클릭한 메뉴의 색깔이 바뀌는 기능

### Code
```javascript
<body>
    <h1 id="main-title">Event</h1>
    <nav class="menu">
      <a href="#" class="menu-link" data-menu="1">menu 1</a>
      <a href="#" class="menu-link" data-menu="2">menu 2</a>
      <a href="#" class="menu-link" data-menu="3">menu 3</a>
    </nav>
    <script>
      let currentMenu; // 현재 활성화된 메뉴를 담을 변수
      let menuLinks = document.querySelectorAll(".menu-link");

      function clickMenuHandeler() {
        if (currentMenu) {
          currentMenu.classList.remove("menu-active");
        }
        this.classList.add("menu-active");
        currentMenu = this;
        console.log(currentMenu);
      }
      for (let i = 0; i < menuLinks.length; i++) {
        menuLinks[i].addEventListener("click", clickMenuHandeler);
      }
    </script>
</body>
```
### CSS
```javascript
<style>
  body {
    font-size: 3rem;
  }
  h1 {
    background: #fff000;
  }
  .menu {
    display: flex;
  }
  .menu-link {
    margin: 0.1em;
    padding: 0.3em;
    text-decoration: none;
    background: dodgerblue;
    color: #ffffff;
    list-style: none;
  }
  .menu-active {
    background: orange;
  }
</style>
```
### Demo
<img src="https://user-images.githubusercontent.com/60775453/127089572-df722da6-94bb-4d5d-a071-5862f1e971a6.gif" width="50%" height="50%">
