# Copyright 2018-present Facebook. All Rights Reserved.
#
# This program file is free software; you can redistribute it and/or modify it
# under the terms of the GNU General Public License as published by the
# Free Software Foundation; version 2 of the License.
#
# This program is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
# FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License
# for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program in a file named COPYING; if not, write to the
# Free Software Foundation, Inc.,
# 51 Franklin Street, Fifth Floor,
# Boston, MA 02110-1301 USA

lib: libmisc-utils.so

C_SRCS := $(wildcard *.c)
C_OBJS := ${C_SRCS:.c=.o}
TEST_C_SRCS := $(wildcard test/*.c)
TEST_C_OBJS := ${TEST_C_SRCS:.c=.o}

CFLAGS += -Wall -Werror -fPIC

libmisc-utils.so: $(C_OBJS)
	$(CC) -shared -o libmisc-utils.so $^ -lc $(LDFLAGS)

test-libmisc-utils: $(C_OBJS) $(TEST_C_OBJS)
	$(CC) $(CFLAGS) -std=c99 -o $@ $^ $(LDFLAGS)

$(C_SRCS:.c=.d):%.d:%.c
	$(CC) $(CFLAGS) $< >$@

.PHONY: clean

clean:
	rm -rf *.o test/*.o libmisc-utils.so test-libmisc-utils
