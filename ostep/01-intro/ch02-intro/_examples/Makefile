all: cpu mem threads io

.PHONY: clean
clean:
	rm -f cpu mem threads io

cpu: cpu.c common.h
	gcc -o cpu cpu.c -Wall

mem: mem.c common.h
	gcc -o mem mem.c -Wall

threads: threads.c common.h common_threads.h
	gcc -o threads threads.c -Wall -pthread

io: io.c common.h
	gcc -o io io.c -Wall

# Invoker Targets -------------------------------------------------------------

# Demonstrate cpu virtualisation.
.PHONY: run-cpu
run-cpu:
	./cpu A

# Demonstrate cpu virtualisation by running a program mulitple times at the same time.
# killall -9 cpu
.PHONY: run-cpu-2
run-cpu-2:
	./cpu A & ./cpu B & ./cpu C & ./cpu D 

# Demonstrate memory virtualisation.
.PHONY: run-mem
run-mem:
	./mem 1

# Demonstrate memory virtualisation by running a program mulitple times at the same time.
# Both processes appear to run in the same address space
#  killall -9 mem
.PHONY: run-mem-2
run-mem-2:
	./mem 100 & ./mem 200

# Demonstrate concurrency failure.
.PHONY: run-threads
run-threads:
	./threads 10000

# Demonstrate io.
.PHONY: run-io
run-io:
	./io


