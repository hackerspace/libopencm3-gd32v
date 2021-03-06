##
## This file is part of the libopencm3 project.
##
## Copyright (C) 2019 Brian Viele <vielster@allocor.tech>
##
## This library is free software: you can redistribute it and/or modify
## it under the terms of the GNU Lesser General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later version.
##
## This library is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU Lesser General Public License for more details.
##
## You should have received a copy of the GNU Lesser General Public License
## along with this library.  If not, see <http://www.gnu.org/licenses/>.
##
## The PAC55xx by Qorvo (formerly ActiveSemi) is a Cortex-M4F based device
## which is specialized for motor control and PSC applications. 

LIBNAME		= libopencm3_pac55xx
SRCLIBDIR	?= ..
FP_FLAGS	?= -mfloat-abi=hard -mfpu=fpv4-sp-d16
CC		= $(PREFIX)gcc
AR		= $(PREFIX)ar
TGT_CFLAGS	= -Os \
		  -Wall -Wextra -Wimplicit-function-declaration \
		  -Wredundant-decls -Wmissing-prototypes -Wstrict-prototypes \
		  -Wundef -Wshadow \
		  -I../../include -fno-common \
		  -mcpu=cortex-m4 -mthumb $(FP_FLAGS) -Wstrict-prototypes \
		  -ffunction-sections -fdata-sections -MD -DPAC55XX
TGT_CFLAGS  += $(DEBUG_FLAGS)
TGT_CFLAGS  += $(STANDARD_FLAGS)
ARFLAGS		= rcs

OBJS += can.o
OBJS += ccs.o
OBJS += gpio.o
OBJS += memctl.o
OBJS += usart.o

vpath %.c ../cm3


include ../Makefile.include
