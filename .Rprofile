options(repos="https://mran.revolutionanalytics.com/snapshot/2020-07-01")
previous_libpaths<-.libPaths()
r_major<-R.Version()$major
r_minor<-substr(R.Version()$minor,1,1)
desired_libpath<-file.path(tools::file_path_as_absolute("local_library"),paste0(r_major,".",r_minor))
Sys.setenv("R_LIBS_USER"=desired_libpath)
Sys.setenv("R_LIBS_SITE"=desired_libpath)
assign('.lib.loc',
       desired_libpath,
       envir = environment(.libPaths)
)
rprofile_libpath<-.libPaths()

# ## Note: uncommenting this will result in the desired behavior
# setHook("rstudio.sessionInit", function(newSession) {
#   if (newSession){
#     assign('.lib.loc',
#            desired_libpath,
#            envir = environment(.libPaths)
#     )
#   }
# }, action = "append")
# Always end with an extra newline
