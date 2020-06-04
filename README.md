
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ipa <img src="man/figures/logo.png?raw=TRUE" align="right" height="138" />

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![License:
MIT](https://img.shields.io/badge/license-MIT-blueviolet.svg)](https://opensource.org/licenses/MIT)
[![R build
status](https://github.com/rossellhayes/ipa/workflows/R-CMD-check/badge.svg)](https://github.com/rossellhayes/ipa/actions)
[![Codecov test
coverage](https://codecov.io/gh/rossellhayes/ipa/branch/master/graph/badge.svg)](https://codecov.io/gh/rossellhayes/ipa?branch=master)
<!-- badges: end -->

Convert character vectors between phonetic representations. Supports
[IPA](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet),
[X-SAMPA](https://en.wikipedia.org/wiki/X-SAMPA) and
[ARPABET](https://en.wikipedia.org/wiki/ARPABET) (used by the [CMU
Pronouncing
Dictionary](https://en.wikipedia.org/wiki/CMU_Pronouncing_Dictionary)).

## Installation

You can install the development version of **ipa** from GitHub with:

``` r
install_github("rossellhayes/ipa")
```

## Usage

My main use case for **ipa** is including phonetic representations in R
markdown files. You can enter phonetic information as plain-text X-SAMPA
and have it rendered as IPA.

``` r
`r sampa('/aI pi: "eI/')`
```

/aɪ piː ˈeɪ/

``` r
`r sampa(c('/"nom.b4e/', '/nO~bR/'))`
```

/ˈnom.bɾe/, /nɔ̃bʁ/

You can also get the X-SAMPA representation of IPA strings.

``` r
ipa("/aɪ piː ˈeɪ/")
```

`/aI pi: "eI/`

``` r
ipa(c("/ˈnom.bɾe/", "/nɔ̃bʁ/"))
```

`/nom.b4e/`, `/nO~bR/`

<!-- `ipa()` does not work in Rmarkdown, but does work in the console -->

ARPABET support allows **ipa** to automatically convert results from the
[**phon**](https://github.com/coolbutuseless/phon) package.

``` r
# remotes::install_github("coolbutuseless/phon")
arpa(phon::phonemes("pronounce"))
```

pɹʌnaʊns

-----

Please note that **ipa** is released with a [Contributor Code of
Conduct](https://contributor-covenant.org/version/2/0/CODE_OF_CONDUCT.html).
By contributing to this project, you agree to abide by its terms.
