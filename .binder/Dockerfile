FROM mathesong/kinfitr_binderdocker:latest
LABEL maintainer='mathesong'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}


RUN wget https://github.com/mathesong/kinfitr_vignette_basics/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-02-20/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
