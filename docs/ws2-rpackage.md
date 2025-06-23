# 📦 Workshop 2: Package Your Code

[![R Package](https://img.shields.io/badge/Workshop-R_Package-green?style=for-the-badge&logo=r)](https://sistm.github.io/level-up-your-code/ws2-rpackage.html)

> “Turn your R scripts into shareable, installable, and testable tools.”  
> — <i>Level UP your Code! – Workshop 2</i>

---

## 🎯 Workshop Goal

Learn how to **transform your R code into a proper R package** so that it can be reused, installed, tested, and shared easily.

---

## 🧠 Key Concepts

- 📁 Understand package structure: `DESCRIPTION`, `NAMESPACE`, `R/`
- ⚙️ Automate setup with `usethis`
- 🧪 Document functions with `roxygen2`
- 🧪 Test code using built-in testing structure
- 🧩 Build and install packages locally or via GitHub

---

## ⚙️ Tools You’ll Use

- 📦 [`devtools`](https://devtools.r-lib.org/)
- 🧰 [`usethis`](https://usethis.r-lib.org/)
- 📝 [`roxygen2`](https://roxygen2.r-lib.org/)

---

## 🧰 Starter Resources

- 🧪 GitHub Template Repository: [rpackage-template](https://github.com/jadelkarchi/rpackage-template)

---

## 🛠️ Quick Workflow

```r
# Set up your package structure
usethis::create_package("mypackage")

# Add and document a function
usethis::use_r("myfunction")
usethis::use_roxygen_md()
devtools::document()

# Add tests
usethis::use_testthat()
usethis::use_test("myfunction")

# Install locally
devtools::install()
```


⏭️ Next Workshop : [GitHub – Save & Deploy Your Code](./ws3-github.md)