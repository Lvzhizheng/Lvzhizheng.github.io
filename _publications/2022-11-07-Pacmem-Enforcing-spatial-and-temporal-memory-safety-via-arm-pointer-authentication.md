---
title: "Pacmem: Enforcing spatial and temporal memory safety via arm pointer authentication"
collection: publications
permalink: /publication/2022-11-07-Pacmem-Enforcing-spatial-and-temporal-memory-safety-via-arm-pointer-authentication
excerpt: 'This paper is about a novel sanitizer PACMem to efficiently catch spatial and temporal memory safety bugs.'
date: 2022-11-07
venue: 'CCS'
slidesurl: 'http://academicpages.github.io/files/slides2.pdf'
paperurl: 'https://dl.acm.org/doi/pdf/10.1145/3548606.3560598'
citation: 'Yuan Li, Wende Tan, Zhizheng Lv, Songtao Yang, Mathias Payer, Ying Liu, and Chao Zhang. 2022. PACMem: Enforcing Spatial and Temporal Memory Safety via ARM Pointer Authentication. In Proceedings of the 2022 ACM SIGSAC Conference on Computer and Communications Security (CCS22). Association for Computing Machinery, New York, NY, USA, 1901–1915. https://doi.org/10.1145/3548606.3560598.'
---

Memory safety is a key security property that stops memory corruption vulnerabilities. Different types of memory safety enforcement solutions have been proposed and adopted by sanitizers or mitigations to catch and stop such bugs, at the development or deployment phase. However, existing solutions either provide partial memory safety or have overwhelmingly high performance overheads.
In this paper, we present a novel sanitizer PACMem to efficiently catch spatial and temporal memory safety bugs. PACMem removes the majority of the overheads by sealing metadata in pointers through the COTS hardware feature -- ARM PA (Pointer Authentication) and saving the overhead of pointer metadata tracking. We have developed a prototype of PACMem and systematically evaluated its security and performance on the Magma, Juliet, Nginx, and SPEC CPU2017 test suites. In our evaluation, PACMem shows no false positives together with negligible false negatives, while introducing stronger bug detection capabilities and lower performance overheads than state-of-the-art sanitizers, including HWASan, ASan, SoftBound+CETS, Memcheck, LowFat, and PTAuth. Compared to the widely deployed ASan, PACMem has no false positives and much fewer false negatives and reduces the runtime overheads by 15.80% and the memory overheads by 71.58%.