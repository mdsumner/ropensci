## Antarctic and Southern Ocean Science

<div>

This article is about R packages that are relevant to Antarctic and
Southern Ocean science. It includes packages in various states of
maturity, including some in planning or very early stages of
development.

Antarctic and Southern Ocean science covers a diverse range of topics
within the geosciences, life sciences, physical sciences, and humanities
and social sciences. This article is not intended to be an exhaustive
list of packages that are relevant to all of those fields, but rather a
synopsis of packages that are for one reason or another of particular
interest to Antarctic and Southern Ocean researchers. The definition of
“particular interest” is of course largely arbitrary. Packages listed
here are generally expected to be at a useful stage of development, or
if not, are seeking engagement/input from the wider community.

Contributions are welcome\! Please [submit an
issue](https://github.com/SCAR/ropensci/issues), or make a contribution
(see the [contribution guidelines](CONTRIBUTING.md)). If you have an
issue with one of the packages discussed below, please contact the
maintainer of that package.

Many thanks to contributors, including Scott Chamberlain, Michael
Sumner, Grant Humphries, Hsun-yi Hsieh, and Anton Van de Putte.

### Taxonomic Data

The Register of Antarctic Marine Species (RAMS) is the authoritative
taxonomic database for Antarctic marine organisms. RAMS is part of the
World Register of Marine Species (WoRMS).

  - [worrms](https://cran.rstudio.com/web/packages/worrms/index.html) client for the
    [WoRMS](http://www.marinespecies.org/) API. Contains mostly
    taxonomic data, but also trait data.
  - [taxize](https://cran.rstudio.com/web/packages/taxize/index.html) provides access to 20ish
    sources of taxonomic data sources, including WoRMS. It has
    consistent data outputs and function interfaces across the different
    data sources so that you don’t need to tailor your code to different
    taxonomic data providers.

RAMS is currently being extended to cover non-marine taxa, which will
become the Register of Antarctic Species (RAS). Hopefully this will
remain covered by `worrms` and the server-side infrastructure hosted by
VLIZ. There is also the
[biotaxa](https://github.com/hhsieh/biotaxa_Rpackage) package in
development for working with RAS (visualising and predicting the growth
in taxonomic diversity over time).

For more detail on R packages dealing with taxonomy in general, see the
[rOpenSci taxonomy task view](https://github.com/ropensci/taxonomy).

### Mapping

Mapping is a very common task, and in an Antarctic/Southern Ocean
context brings with it particular issues including dealing with
projection properties at high latitudes, coping with data that crosses
the 180°E line, adding commonly-desired features such as ocean fronts,
management boundaries, sea ice extent, stations and other geographic
features, and common contextual layers such as bathymetry.

  - [SOmap](https://github.com/AustralianAntarcticDivision/SOmap) is in
    development, but aims to provide straightforward mapping functions
    for Southern Ocean (polar stereographic) maps, along with
    commonly-used management and contextual layers such as MPA
    boundaries and ocean fronts.

  - [antanym](https://github.com/SCAR/antanym) provides geographic place
    name data from the SCAR Composite Gazetteer of Antarctica, with
    plans to extend the coverage to subantarctic and informal gazetteers
    at a later date.

  - [orsifronts](https://cran.rstudio.com/web/packages/orsifronts/index.html) provides the
    commonly-used Orsi et al. (1995) definitions of the major Southern
    Ocean fronts.

  - [graticule](https://cran.rstudio.com/web/packages/graticule/index.html) creates graticule
    lines (lines of longitude and latitude) and labels for maps.

  - [palr](https://cran.rstudio.com/web/packages/palr/index.html) provides colour palettes for
    data, based on some well known remotely sensed data sets for sea ice
    concentration, sea surface temperature and chlorophyll- *a* .

  - there is some Antarctic-related mapping functionality in
    [prtools](https://github.com/pierreroudier/prtools),
    [atlasr](https://github.com/jiho/atlasr),
    [CCAMLRGIS](https://github.com/ccamlr/CCAMLRGIS), and
    [sospatial](https://github.com/AustralianAntarcticDivision/sospatial).

### Environmental Data

  - [blueant](https://github.com/AustralianAntarcticDivision/blueant)
    and its companion package
    [bowerbird](https://github.com/AustralianAntarcticDivision/bowerbird)
    provide a mechanism to download a range of environmental data
    including satellite-derived sea ice, sea surface temperature,
    topography, ocean colour (chlorophyll- *a* ), and meteorological
    data from various providers. Many of these data sets can be read and
    manipulated with [raster](https://cran.rstudio.com/web/packages/raster/index.html) and similar
    packages: the [spatial task
    view](https://cran.r-project.org/web/views/Spatial.html) is a good
    resource here.

  - the [PolarWatch](https://polarwatch.noaa.gov/) project aims to
    enable data discovery and broader use of high-latitude ocean remote
    sensing data sets. The dedicated ERDDAP server
    (https://polarwatch.noaa.gov/erddap) is accessible to R users with
    [rerddap](https://cran.rstudio.com/web/packages/rerddap/index.html).

  - [rsoi](https://cran.rstudio.com/web/packages/rsoi/index.html) downloads the most up to date
    Southern Oscillation Index, Oceanic Nino Index, and North Pacific
    Gyre Oscillation data.

### Oceanography

  - satellite reflectance data are a common basis for estimating
    chlorophyll- *a* and other phytoplankton parameters at ocean-basin
    scales. Global products are widely available; however,
    Southern-Ocean specific algorithms are likely to provide better
    estimates in these regions. [croc](https://github.com/sosoc/croc)
    implements the Johnson et al. (2013) Southern Ocean algorithm.

  - more broadly, [oce](https://cran.rstudio.com/web/packages/oce/index.html) provides a wide
    range of tools for reading, processing, and displaying oceanographic
    data, including measurements from Argo floats and CTD casts,
    sectional data, sea-level time series, and coastline and topographic
    data.

  - [fda.oce](https://github.com/EPauthenet/fda.oce) provides functional
    data analysis of oceanographic profiles for front detection, water
    mass identification, unsupervised or supervised classification,
    model comparison, data calibration, and more.

### Biodiversity data

  - [robis](https://cran.rstudio.com/web/packages/robis/index.html) for marine data,
    [rgbif](https://cran.rstudio.com/web/packages/rgbif/index.html) for global biodiversity data.
    [spocc](https://cran.rstudio.com/web/packages/spocc/index.html) wraps these and other
    occurrence data providers with a consistent interface (but not
    necessarily the full functionality of provider-specific packages,
    where they exist).

  - [obistools](https://github.com/iobis/obistools) and
    [scrubr](https://cran.rstudio.com/web/packages/scrubr/index.html) for quality-checking
    occurrence data.

  - a package for the data behind the [Mapping Application for Penguin
    Populations and Projected Dynamics
    (MAPPPD)](http://www.penguinmap.com/) is in planning: contact [Grant
    Humphries](mailto:grwhumphries@blackbawks.net).

  - diet data [sohungry](https://github.com/SCAR/sohungry) and
    allometric equations [solong](https://github.com/SCAR/solong)

### Animal tracking

Tracking of animals using satellite, GPS, or light-level geolocation
tags is common, and there are many R packages that can help with this.
See the [spatiotemporal task
view](https://cloud.r-project.org/web/views/SpatioTemporal.html) for a
more complete list. Of particular interest may be:

  - [TwilightFree](https://github.com/ABindoff/TwilightFree) provides a
    method for processing light-level geolocation data that is robust to
    noise (sensor shading and obscuration) and may be particularly
    suitable for Southern Ocean applications.

### Miscellaneous

Packages that may be of interest but don’t yet fit neatly into another
category.

  - [distancetocoast](https://github.com/mdsumner/distancetocoast)
    provides “distance to coastline” data for longitude and latitude
    coordinates.

</div>

### CRAN packages:

  - [graticule](https://cran.rstudio.com/web/packages/graticule/index.html)
  - [oce](https://cran.rstudio.com/web/packages/oce/index.html)
  - [orsifronts](https://cran.rstudio.com/web/packages/orsifronts/index.html)
  - [palr](https://cran.rstudio.com/web/packages/palr/index.html)
  - [raster](https://cran.rstudio.com/web/packages/raster/index.html)
  - [rerddap](https://cran.rstudio.com/web/packages/rerddap/index.html)
  - [rgbif](https://cran.rstudio.com/web/packages/rgbif/index.html)
  - [robis](https://cran.rstudio.com/web/packages/robis/index.html)
  - [rsoi](https://cran.rstudio.com/web/packages/rsoi/index.html)
  - [scrubr](https://cran.rstudio.com/web/packages/scrubr/index.html)
  - [spocc](https://cran.rstudio.com/web/packages/spocc/index.html)
  - [taxize](https://cran.rstudio.com/web/packages/taxize/index.html)
  - [worrms](https://cran.rstudio.com/web/packages/worrms/index.html)

### Related links:

  - [taxonomy task view](https://github.com/ropensci/taxonomy)
  - [spatial task
    view](https://cran.r-project.org/web/views/Spatial.html)
  - [spatiotemporal task
    view](https://cloud.r-project.org/web/views/SpatioTemporal.html)
