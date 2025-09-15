---
marp: true
theme: default
paginate: true
title: Creating Scalable and Shareable R Packages with `devtools`
description: A hands-on guide for researchers
class: lead
---

# 📦 R Package Development with `devtools`

### A practical guide to building, testing, archiving, and sharing R packages for research

---

# 🧭 Objectives

By the end of this session, you'll know how to:

- Structure an R package using `devtools`
- Write clean, testable, scalable code
- Archive and share your package
- Collaborate with others effectively

---

# 💡 Why Create an R Package?

- Encapsulate reusable code
- Standardize structure for long-term maintenance
- Facilitate collaboration
- Share with the community (CRAN, GitHub, etc.)
- Improve reproducibility in research

---

# 🔧 Tools You'll Use

- `devtools`: for package development
- `usethis`: for automation and structure
- `roxygen2`: for documentation
- `testthat`: for testing
- `pkgdown`: for documentation websites
- `GitHub` or `GitLab`: for versioning 

---

# 🛠️ Step 1: Set Up Your Package

```r
library(devtools)
create("mypackage")
```

Creates:

```r
|mypackage/
|── DESCRIPTION
|── NAMESPACE
|── R/
|── man/
|── tests/
```

---

## Use usethis to add structure:

```r
usethis::use_description()
usethis::use_git()
usethis::use_readme_rmd()
```
---

# ✍️ Step 2: Write Functions
Put your R functions in the R/ directory.

```r
# R/hello.R
hello <- function(name) {
  paste("Hello", name)
}
```
---

## Document them with roxygen2:

```r
#' Say Hello
#'
#' @param name A character string
#' @return A greeting
#' @export
hello <- function(name) {
  paste("Hello", name)
}
```

---

# 🔬 Step 3: Testing with testthat

```r
usethis::use_testthat()
usethis::use_test("hello")
```

```r
# tests/testthat/test-hello.R
test_that("hello works", {
  expect_equal(hello("World"), "Hello World")
})
```
## Run tests with:

```r
devtools::test()
```
---

# 📦 Step 4: Install & Load

```r
devtools::load_all()  # for development
devtools::install()   # install to your R library
```

---

# 🌐 Step 5: Versioning & GitHub

```r
usethis::use_github()
usethis::use_github_action("check-standard")
```

## Tag versions:

```r
usethis::use_version("minor") # bump version
usethis::use_release_issue()
```

---

# 🧪 Continuous Integration (Optional)

```r
devtools::check() for CRAN compliance
```

### rcmdcheck for diagnostics:

---

# 🗂️ Step 6: Archive Your Package

- CRAN: Standard, but strict

- GitHub/GitLab: Easy to use

- Zenodo: Generates DOI for publications

- Use `usethis::use_mit_license()` or `use_gpl3_license()`

---

#  🌍 Step 7: Make It Shareable

### Use pkgdown for docs:

```r
usethis::use_pkgdown()
pkgdown::build_site()
```

- Add a `README.md`, `LICENSE`, `NEWS.md`

### Good examples and vignettes:

```r
usethis::use_vignette("intro")
```

---

# 📐 Best Practices for Scalability

- Use clear, modular functions

- Follow a naming convention

- Separate data from logic

- Write unit tests early

- Document every function

- Use namespaces smartly

---
# 🙋 Q&A
Any questions?

---

# 🧠 Further Reading

`r-pkgs.org`

`GitHub Actions`

`usethis`

`pkgdown`

