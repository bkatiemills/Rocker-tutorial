# the basic OS + core dependencies; this has the hadleyverse + all rOpenSci packages on CRAN: 
FROM rocker/ropensci:latest

# but, I also want a custom R dependency:
RUN wget https://cran.r-project.org/src/contrib/gapminder_0.1.0.tar.gz
RUN R CMD INSTALL gapminder_0.1.0.tar.gz

# let's wrap some files up in our docker image, too:
ADD gapminder-plot.R /home/rstudio/
