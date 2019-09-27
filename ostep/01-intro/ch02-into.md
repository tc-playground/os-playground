# Operating Systems - Introduction

## Introduction

* `Operating Systems` provide an abstraction over the underlying hardware.

    * `Operating Systems` provide a `virtual machine` on-top of a physical machine.

    * `Operating Systems` provide `resource management`.

* `Operating Systems` can be broken down into 3 areas:

    1. `Virtualisation`

        1. `CPU Virtualisation`

        2. `Memory Virtualisation`

    2. `Concurrency`

        1. `Multiple simultaneous programs`

        2. `Multiple simultaneous program threads`

        3. `Critical Sections`

        4. `Atomicity`

    3. `Persistence`

        1. `Filesystems`

* `Operating Systems` must also provide:

    1. `Isolation`

    2. `Security`

---

## Virtualisation

1. __Virtualizing CPUs__ - Giving the illusion of many program having their own processors.

    1. __Mechanisms__ - Rapidly, `context switching` between processors giving each program a `timeslice`.

    2. __Policies__ - How to determine what program should be given a `timeslice` next?

2. __Virtualizing Memory__ - Giving the illusion of many program having their own memory address space.

    1. __Mechanism__ - `Mapping` _physical addresses_ to _virtual addresses_  through `pages`.

    2. __Policies__ - How to determine when and how to cache, load, and save the mapped memory.
    
---

## Concurrency

1. __Critical Sections__ - Operations on a shared piece of state between concurrent processes can lead to unexpected result between `read` and `write` operations.

2. __Atomic Operations__ - Operations that `mutate state` are performed using multiple (hardware) operations and are not `atomic`. This can lead to strange errors.

---

## Persistence (and Isolation)

1. __Hardware Privilege levels__ and __System calls__

2. __IO Drivers__

3. __Shared Filesystems__


---

## References

* [Operating Systems - Chapter 2: Introduction](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf)

* [Operating Systems - Three Easy Pieces](http://pages.cs.wisc.edu/~remzi/OSTEP/)

* [OSTEP - Github](https://github.com/remzi-arpacidusseau/ostep-code)