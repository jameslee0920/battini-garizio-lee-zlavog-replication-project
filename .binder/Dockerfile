FROM rocker/binder:3.6.0
LABEL maintainer='Advika Battini'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/UW-MSDS-DATA-598-Reproducibility-WI20/battini-garizio-lee-zlavog-replication-project/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-03-11/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
