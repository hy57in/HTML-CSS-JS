# Event

## menu를 클릭했을 때 클릭한 메뉴의 색깔이 바뀌는 기능

### Code
```javascript
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
```
### Demo
<img src="https://user-images.githubusercontent.com/60775453/127089572-df722da6-94bb-4d5d-a071-5862f1e971a6.gif" width="50%" height="50%">
