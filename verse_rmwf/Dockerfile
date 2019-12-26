FROM rocker/verse:3.6.1
MAINTAINER "@cgpu"

RUN apt update \
  && apt install -y --no-install-recommends \
    ## {r-quantities/units} dependency
    apt-utils \
  && apt install -y --no-install-recommends \
    libgdal-dev \
    ## {r-spatial/sf} dependency
    libgeos-dev \
    libproj-dev \
    libudunits2-dev \
    libnetcdf-dev \
    ## rgl support
    libgl1-mesa-dev \
    libglu1-mesa-dev \
    ## tcl tk support
    tcl8.6-dev \
    tk8.6-dev \
  && R -e "BiocManager::install(c('annotate','igraph','RBGL','bitops','preprocessCore','impute','GO.db','pcaMethods','xcms','IPO','sva','WGCNA', 'KEGGREST', 'KEGGgraph', 'SSPA','Rdisop', 'qvalue', 'GlobalAncova', 'globaltest', 'siggenes', 'Rgraphviz','ChemmineR','metaMS', 'msPurity', 'mixOmics', 'fgsea', 'Rita','Autotuner'), update = FALSE)" \
  && install2.r --error \
    nontarget \
    ChemoSpec \
    webchem \
    InterpretMSSpectrum \
    tcltk2 \
    ROCS \
    plotly \
  && install2.r --error \
    --deps TRUE \
    qgraph \
    bookdown \
    blogdown \
    xaringan \
    pkgdown \
    xfun \
    liftr \
    radix \
    citr \
    scifigure \
  && installGithub.r \
    omegahat/XMLSchema \
    cran/SSOAP \
    cran/VennDiagram \
    xia-lab/MetaboAnalystR \
    yufree/apLCMS \
    yufree/xMSanalyzer \
    yufree/xMSannotator \
    yufree/x13cms \
    nathaniel-mahieu/warpgroup \
    yufree/mz.unity \
    cbroeckl/RAMClustR \
    rwehrens/BatchCorrMetabolomics \
    yufree/decoMS2 \
    KechrisLab/MSPrep \
    yufree/xsetplus \
    yufree/MetDIA \
    WMBEdmands/MetMSLine \
    WMBEdmands/compMS2Miner \
    yufree/rmwf \
    c-ruttkies/MetFragR/metfRag \
    yufree/rfigshare \
    yufree/enviGCMS \
    yufree/pmd \
    yufree/MetaboDIA 