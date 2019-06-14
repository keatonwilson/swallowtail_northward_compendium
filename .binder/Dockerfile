FROM rocker/binder:3.6.0
LABEL maintainer='karthik'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/keatonwilson/swallowtail_northward_compendium/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/18061/')); devtools::install_deps()"
