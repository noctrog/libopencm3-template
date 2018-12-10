Easy "clone and go" repository for a libopencm3 and FreeRTOS (v10.0.1) based project.

# Instructions
 1. git clone https://github.com/noctrog/libopencm3-template.git your-project
 2. cd your-project
 3. git submodule update --init # (Only needed once)
 4. make -C libopencm3 # (Only needed once)
 5. Edit FreeRTOSConfig.h to fit your needs and select one of the heap_x.c files
 6. make -C my-project

# Directories
* my-project contains your application
* my-common-code contains something shared.
* FreeRTOS contains the FreeRTOS headers and source.
