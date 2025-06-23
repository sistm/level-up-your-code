# 🧪 Workshop 1: Reproducible Environments with `renv`

> “Reproducibility is the first step toward trustworthy science.”  
> — <i>Level UP your Code! – Workshop 1</i>

---

## 🎯 Workshop Goal

Enable your R project to be **portable** and **reproducible** using [`renv`](https://rstudio.github.io/renv/).  
You’ll isolate dependencies and share environments effortlessly.

---

## 📦 What You’ll Learn

- 🔒 How to create an isolated and reproducible R project environment
- 🧪 Use of `renv::snapshot()` to lock dependencies
- ♻️ Use of `renv::restore()` to recreate environments
- 📤 Share and reuse `renv.lock` for collaboration

---

## 🧰 Resources & Links

- 📘 Official [`renv` documentation](https://rstudio.github.io/renv/)
- 🗂️ Example GitHub repo: [jadelkarchi/renv-workshop](https://github.com/jadelkarchi/renv-workshop)
- 📎 Download sample lock file: [`renv.lock`](./assets/renv.lock)

---

## 🧭 Quick Commands

```r
# Initialize renv in your R project
renv::init()

# Save current packages
renv::snapshot()

# Restore packages from renv.lock
renv::restore()
```

⏭️ Next Workshop : [Build Your R Package](./ws2-rpackage.md)