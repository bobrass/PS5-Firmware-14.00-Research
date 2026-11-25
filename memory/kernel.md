# PS5 Research - Kernel Team Memory

Team members: Kernel Analyst, WebKit Analyst
Specialty: Linux kernel analysis, WebKit security, system-level vulnerabilities

Recent facts:
- 2026-11-25: FW 14.23 exploit mission assigned
- AIO Subsystem (Finding 13 → Finding 91): Probe syscalls 586 (thr_new), 611 (aio_*) on 14.23 - evidence: sysret return codes, thread handles, kernel panics
- W^X Bypass (Findings 1,44,50 → Finding 28): Test syscall 585 (mtypeprotect) with all argument patterns - check memory protection flags  
- Thread Races (Finding 2 Corrected): thr_create(430), thr_new(455) on 14.23 - TOCTOU, UAF races via timing measurements
- WebKit Canvas2D UAF: CVE-2026-43720 UNEXPLOITABLE on 14.x (OOM trigger), check for new vectors in 14.23 branch