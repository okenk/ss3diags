# ss3siags 2.1.1

* Added new logo. Thanks @pdimens (#76, #77)
* Added options to `SSdeltaMVLN` for Variance-Coveriance approximation and bias correction. Thanks @N-DucharmeBarth-NOAA (#64)
* Updated r4ss dependency (#84)
  * Dependency resolves r4ss function name conflicts w/ dplyr and kableExtra libraries (#83). Side effect of nmfs-fish-tools/ghactions4r#69
* Removed `dplyr` from NAMESPACE. Removed roxygen import calls from `SSplotJABBAres()` and `SSrmse()`, and appended **dplyr** function calls with the double colon operator (`dplyr::`)  (#82)
* Updated default **summaryoutput** used in `SSplotModelComp()` for `ss3diags::retroSimple` and default **ss3rep** used in `SSplotRunsTest()` for `ss3diags::simple`
* Updated ss3diags citation. 
* Minor documentation link fixes.

# ss3diags 2.1.0

* RMSE calculations are modularized as a standalone function that can be called independently from `SSplotJABBAres()` as `SSrmse()`. (#50) 
* Bugfixes with adjusting y-axis limits with SSplotRunstest and SSplotJABBAres: Use the `ylim` parameter to adjust y-axis limits. (#46)
* Added option to remove median trajectory for `SSplotKobe()` (#3)
* Added **rlang**, **dplyr**, and **magrittr** dependencies.
* SSmase and SSplotHcxval: Corrected validation messsage to clarify validation issue and to fix an issue with the code styler. (#33, #35)
* Added Date field to DESCRIPTION. DESCRIPTION metadata are now used to generate package citations. (#25)
* Package vingettes formatted to `html_vignette` to reduce file size. Removed redundant PDF and word document versions of *ss3diags_Handbook* vignette.
* Updated documentation and fixes.
  * Enabled markdown support for roxygen. 
  * Enabled Cross-reference links.

# ss3diags 2.0.3

* Changed r4ss dependency to 1.44.0 (CRAN version) and above. 
* Replaced default R CMD CHECK workflow with NOAA-fish-tools/ghactions4r's version.
* Fixed Ensemble Quantile Shading Issues (#4)
* Replaced the example datasets in the ss3diags cookbook, and the handbook with the current "simple" ensemble model.
* Fixup minor code documentation formatting issues.
* Implemented NOAA-fish-tools/ghactions4r integrated code styler and documentation for pull requests.
  * SSmase and SSplotHcxval: Fixed up code styler's dollar subset conversion issues. example:`message('x$name is 1,2,3,4')`

# ss3diags 2.0.2

* Changed r4ss CRAN version (1.36.1) dependency to development version
* Refactored common ssplot subfunctions, renamed, and used equilvants in r4ss util 
  * `legendfun` -> `r4ss::add_legend`
  * `pngfun` -> `r4ss::save_png`
  * `rc` -> `r4ss::rich_colors_short`
  * `sspar` -> `r4ss::sspar`
* Fix SSplotRetro.R indention causing issues with code styler

# ss3diags 2.0.1

* Minor README Updates and corrections
  * Change in SSplotJABBAres to show the combined seasonal data as boxplots
  * Fixup links to Cookbook sripts.
* Formatted DESCRIPTION URL and BugReports links to the PIFSCstockassessments repo too add to its R package site.

# ss3diags 2.0.0 

* ss3iags is now installed as an R-package. Package documentation is upatded to reflect these chenges. 
  * A simple, cod-like, Stock Synthesis model, simulated via ss3sim, replaces Pacific North Hake (`pac.hke`) and North Atlantic Shortfin Mako Shark (`natl.sma`) example datasets.
* SSplotRetro: fixed bug so that the shading in uncertainty area shows up when xlims are specified.
* SSplotJABBAres: added 'con' option to subplots argument so conditional age-at-length data can be plotted. Also added a seas argument so user can specify if data should be combined across seasons within a year or kept separate. 
* SScompsTA1.8: added a seas argument so users can specify if data should be combined across seasons within a year or kept separate.
* SSplot functions (SSplotModelComp, SSplotEnsemble, SSplotHCxval, SSplotJABBAres, SSplotRetro): Marked `plot`, `png`, `pdf`, `print`, and `new` as deprecated. They will be defunct in a future version.
* Added a `NEWS.md` file to track changes to the package.

# ss3diags 1.0.8

* Fixed MASE

# ss3diags 1.0.7

* Bug fixes

# ss3diags 1.0.6

* Improved SSdiagsMCMC

# ss3diags 1.0.5

* Updated SSdeltaMVLN

# ss3diags 1.0.4 

* Reference: authors changes 

# ss3diags 1.0.3

* Added annF_ quantaties

# ss3diags 1.0.2

* Added aut

# ss3diags 1.0.1

* Added SSplotH
