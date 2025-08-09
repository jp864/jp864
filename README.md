# 👋 Hello! I'm João Rodrigues

## ♾️ About Me

I'm a self-taught technologist with a lifelong passion for computers and software development:

- **Early beginnings**: Started at age 5 on a hand-me-down 2005 "Square Generic" PC, tinkering with *SuperTux*.  
- **Creative growth**: By eight, I was playing Counter-Strike, learning Photoshop to create graphics—and even monetizing my designs.  
- **Multimedia skills**: Taught myself video editing to produce content for YouTube, including video game highlight reels.  
- **AI & automation**: Recently leveraged AI-driven tools to spin up websites for dropshipping, crypto ventures, and other side projects.  
- **Current focus**: At 21, wrapping up my IT degree, diving deep into C programming and exploring low-level systems.

I love turning ideas into working software and continually expanding my toolkit.

---

## 🌐 Connect with Me

[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/jprodrigues_4)  
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/@jprodrigues_4)  

---

## 💻 Tech Stack

![C](https://img.shields.io/badge/C-%2300599C.svg?style=plastic&logo=c&logoColor=white)  
![Assembly](https://img.shields.io/badge/Assembly8086-%23000000.svg?style=plastic&logo=assemblyscript&logoColor=white)  

---

## ⚡ Side Projects (AI-Powered)

- [Casa Vender Lumiar](https://github.com/jp864/casa-vender-lumiar) — House marketing site  
- [AltCoin](https://github.com/jp864/altcoin) — AltCoin (not launched)  
- [URCR7](https://github.com/jp864/x1w1s1z) — AltCoin (launched + paid DEX)  

---

![Super Tux Snowy Questions](https://raw.githubusercontent.com/jp864/media/main/super-tux-snowy-questions.gif)

---

## 🐧 Super Tux GitHub Actions Workflow

Here’s a sample CI workflow I use to keep my projects sliding smoothly like Super Tux on ice:

```yaml
name: 🐧 Super Tux CI 🐧

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  tux-build-test:
    runs-on: ubuntu-latest
    steps:
      - name: 🐧 Checkout code
        uses: actions/checkout@v3

      - name: 🐧 Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'

      - name: 🐧 Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt

      - name: 🐧 Run lint (flake8)
        run: |
          echo "Waddling through the code..."
          pip install flake8
          flake8 .

      - name: 🐧 Run tests
        run: |
          echo "Sliding down the ice to test!"
          pip install pytest
          pytest tests/

      - name: 🐧 Celebrate success!
        if: success()
        run: echo "🎉 All tests passed! Super Tux would be proud! 🐧"

      - name: 🐧 Warning if failure
        if: failure()
        run: echo "🚨 Oh no! The ice cracked! Fix the errors! 🐧"

