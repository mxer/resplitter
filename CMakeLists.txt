add_executable (resplitter resplitter.c) 

# Link the executable to the Hello library. 
target_link_libraries (resplitter sndfile m) 

install_targets(/bin resplitter)

