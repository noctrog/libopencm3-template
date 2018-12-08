PROJECT = awesomesauce
BUILD_DIR = bin

SHARED_DIR = ../my-common-code
FREERTOS_DIR = ../FreeRTOS
CFILES = my-project.c
CFILES += $(notdir $(wildcard $(SHARED_DIR)/*.c))
CFILES += $(notdir $(wildcard $(FREERTOS_DIR)/*.c))

# TODO - you will need to edit these two lines!
DEVICE=stm32f103c8t6
OOCD_FILE = /usr/share/openocd/scripts/target/stm32f1x_stlink.cfg

# You shouldn't have to edit anything below here.
VPATH += $(SHARED_DIR) $(FREERTOS_DIR)
INCLUDES += $(patsubst %,-I%, . $(SHARED_DIR))
INCLUDES += $(patsubst %,-I%, . $(FREERTOS_DIR))
OPENCM3_DIR=../libopencm3

include $(OPENCM3_DIR)/mk/genlink-config.mk
include ../rules.mk
include $(OPENCM3_DIR)/mk/genlink-rules.mk
