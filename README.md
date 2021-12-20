
# hermitage

<!-- badges: start -->
<!-- badges: end -->

This is a palette package inspired by package{wesanderson}, collection of art of Hermitage museum in Saint Petersburg (Russia), and by a fantastic book "The anatomy of colour" by Patrick Baty.

The package offers 27 palettes with distinct colour combinations. The largest palettes are parsons_1 and parsons_2 inspired by Thomas Parsons's colour samples from the book "A Tint Of Historical colours" (1934) and include 87 colours and 120 colours, respectively. Other palettes offer 4 to 14 colours.

## Installation

You can install the development version of hermitage like so:

``` r
install.packages("devtools") 
devtools::install_github("evpatora/hermitage")
```
## Example of included palettes
### Les toits de Collioure, Henri Matisse, [1905](https://www.hermitagemuseum.org/wps/portal/hermitage/digital-collection/!ut/p/z0/Zc69boMwFAXgV6EDW1zfa2yHjBaVqkSiVAwV9RI5xFAXYhNwfx6_ZKwy3OFIV-d8VNOGam--XW-iC96Ma37X8lgpJTEr4FAV4glUVb-Kunh5BuT0QPW_ByEVKKgzLt9K4Ht-a2BzWZQ91ZOJH8T5LtDmy52RoYR8J7YkA5bngsgdMkF4TjgHgsgJAsP18k3oTGtPIQybEGfjl8nM1scijKNtb9A7xR1zVbjP61Urqtvgo_2NtBnMxS1H61P4CfOwJKFLzBxTAHxMJuN8dL5f0nU_2yKdBn0SY__wByXuvmc!/)
The [painting](https://en.wikipedia.org/wiki/Les_toits_de_Collioure) has been in the collection of The Hermitage, St. Petersburg, Russia since 1948.

## Use example

``` r
library(hermitage)
hermitage_palette("du_barry", type = "discrete"))
```

``` r
ggplot(data = penguins, aes(x = species, y = flipper_length_mm, fill = species, color = species)) +
  geom_violin() +
  theme_light(base_size = 12, base_family = "Varela Round") +
  theme(panel.grid = element_blank()) +
  scale_fill_manual(values = hermitage_palette("parsons_2")) +
  scale_color_manual(values = hermitage_palette("parsons_2"))
```
