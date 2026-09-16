# Verifiable Sources for All Claims

Every claim and figure in this Shorts kit is traceable directly to the public RustChain codebase:

1. **Multiplier Table (0.8x modern vs 2.5x G4 vs 4.0x Apple II)**:
   - Source: `node/rustchain_v2_integrated_v2.2.1_rip200.py` lines 780-820 (`HARDWARE_WEIGHTS`) and `rip_200_round_robin_1cpu1vote.py` lines 42-65.
   - Values: Modern x86-64 = `0.8`, PowerPC G4 = `2.5`, Apple II (6502) = `4.0`.

2. **1 CPU = 1 Vote Consensus Principle**:
   - Source: `CPU_ANTIQUITY_SYSTEM.md` and `README.md` lines 12-40.

3. **6 Physical Hardware Fingerprint Checks**:
   - Source: `miners/linux/fingerprint_checks.py` lines 150-510:
     - `check_clock_drift()`: Quartz oscillator nanosecond skew
     - `check_cache_timing()`: L1/L2/L3 step-function latency hierarchy
     - `check_simd_identity()`: Architecture-specific vector unit instruction flags
     - `check_thermal_drift()`: Silicon junction temperature entropy
     - `check_instruction_jitter()`: Execution jitter
     - `check_anti_emulation()`: Hypervisor DMI / CPUID / device vendor checks

4. **VM Penalty Factor (1-Billionth)**:
   - Source: `miners/linux/rustchain_linux_miner.py` lines 790-805:
     `VMs/containers receive minimal rewards (1 billionth of real hardware)`.
