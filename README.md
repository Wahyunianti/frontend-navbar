# Tampilan Halaman HTML CSS Javascript Navbar Mobile

## Preview

<img width="1056" alt="Screen Shot 2024-10-08 at 18 01 52" src="https://github.com/user-attachments/assets/5035141c-dfef-41d0-bc69-b730700eb861">

## Tech
- HTML 5
- CSS
- Javascript


## Codes

### Hightligt, decoration, & style reset
Reset anchor tag styles :

```bash
:root {
    --var-bg-light: #f6f3e8;
    --var-bg-border: #dfdcd5;
}
```

```bash
a {
    text-decoration: none;
    -webkit-tap-highlight-color: transparent;
}
```

```bash
ul {
    list-style: none;
}
```

### HTML Codes
HTML codes for navbar mobile version:

```bash
<ul>
<li class="list">
                    <a href="#">
                        <span class="icon">
                        </span>
                        <span class="text">
                            Affiliate
                        </span>
                    </a>
                </li>
                <div class="indicator"></div>
</ul>
```

### CSS Styles
CSS codes ul li and transition:

```bash
.navbar-mobile ul li.active a .icon {
    transform: translateY(-22px);
    fill: #f6f3e8;
}

.navbar-mobile ul li.active a .icon svg path{
    fill: #f6f3e8;
}

.navbar-mobile ul li a .text {
    position: absolute;
    bottom: 13px;
    color: var(--clr);
    font-weight: 400;
    font-size: 0.75em;
    letter-spacing: 0.05em;
    transition: 0.5s;
    opacity: 0;
    transform: translateY(20px);
}

.navbar-mobile ul li.active a .text {
    opacity: 1;
    transform: translateY(10px);
}

.indicator {
    position: absolute;
    top: -32%;
    width: 80px;
    left: 24px;
    height: 80px;
    background: #000000;
    border-radius: 50%;
    border: 6px solid white;
    transition: 0.5s;
    z-index: 90;
}

.indicator::before {
    content: '';
    position: absolute;
    top: 27%;
    left: -22px;
    width: 21px;
    height: 21px;
    background: transparent;
    border-top-right-radius: 30px;
    box-shadow: 1px -9px 0 0 #ffffff;
}

.indicator::after {
    content: '';
    position: absolute;
    top: 27%;
    right: -22px;
    width: 21px;
    height: 21px;
    background: transparent;
    border-top-left-radius: 30px;
    box-shadow: -1px -9px 0 0 white;
}


.navbar-mobile ul li:nth-child(1).active~.indicator {
    transform: translateX(calc(90px * 0));
}

.navbar-mobile ul li:nth-child(2).active~.indicator {
    transform: translateX(calc(90px * 1));
}

.navbar-mobile ul li:nth-child(3).active~.indicator {
    transform: translateX(calc(90px * 2));
}

.navbar-mobile ul li:nth-child(4).active~.indicator {
    transform: translateX(calc(90px * 3));
}

```

### Javascript Codes
Javascript codes for translate navbar:

Javascript
```bash
 <script>
        const list = document.querySelectorAll('.list');
        function activeLink() {
            list.forEach((item) =>
                item.classList.remove('active'));
            this.classList.add('active');
        }
        list.forEach((item) =>
            item.addEventListener('click', activeLink));
</script>
```
