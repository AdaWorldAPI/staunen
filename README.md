# staunen ✦

**When the machine is genuinely surprised.**

6 CPU instructions. No GPU. L1 cache. That's all.

---

## The Thesis

Specialized RISC cognition — 6 bitwise instructions on kilobytes of L1-resident data — outperforms brute-force tensor math on the specific task of *understanding meaning*.

Not image generation. Not token prediction. Understanding. Causality. Surprise.

## The 6 Instructions

| Instruction | Operation | AVX-512 | Cognitive Meaning |
|-------------|-----------|---------|-------------------|
| `XOR` | bind / unbind | VPXORD (1 cycle) | Association / extraction |
| `POPCOUNT` | distance / similarity | VPOPCNTDQ (1 cycle) | Recognition / comparison |
| `MAJORITY` | bundle / superpose | saturating add | Learning / accumulation |
| `AND/NOT` | 2^3 factorization | VPANDD/VPANDND (1 cycle) | Causal decomposition |
| `BLAKE3` | seal / verify | ~10 cycles | Integrity: Wisdom vs Staunen |
| `THRESHOLD` | σ-band gating | compare (1 cycle) | Admit / reject / ruminate |

Every cognitive operation compiles to sequences of these six. Full causal transparency from instruction to outcome.

## The Demoscene Spirit

The C64 had a 6502 processor. People made it render real-time 3D. Not because the hardware supported it — because the programmers understood every transistor.

An H100 has 16,896 CUDA cores. People multiply float matrices. The hardware supports everything. Nobody understands it completely.

Staunen has 6 instructions on a Xeon. We make it think. Not because the hardware was designed for cognition. Because we understand cognition well enough to map it to 6 instructions that execute in one cycle each.

## The Name

**Staunen** (German: /ˈʃtaʊnən/) — astonishment, wonder, genuine surprise.

The moment when a Merkle seal breaks and the system discovers its own knowledge has changed. Not an error. A feature. The honest acknowledgment that something genuinely new happened.

## Crates

| Crate | Purpose | Depends On |
|-------|---------|------------|
| `staunen-core` | 6 RISC instruction kernel | `std`, `blake3` |
| `staunen-nsm` | DeepNSM semantic primes on CPU | `staunen-core` |
| `staunen-cam` | Content-addressable memory, O(1) | `staunen-core` |
| `staunen-bnn` | Binary neural network reinforcement | `staunen-core` |
| `staunen-nars` | Non-axiomatic reasoning (no floats) | `staunen-core` |
| `staunen-epiphany` | Bundle → threshold → unbundle cycle | `staunen-core`, `staunen-nars` |
| `staunen-amx` | Intel AMX/AVX-512 matrix extensions | `staunen-core` |
| `staunen-bench` | CPU vs GPU cognitive benchmarks | all |

## The Invariant

If an operation requires float32 matrix multiplication, it doesn't belong in staunen.

If an operation can be expressed as XOR / POPCOUNT / MAJORITY / AND-NOT / BLAKE3 / THRESHOLD on bitpacked integers that fit in L1 cache, it belongs in staunen.

Train the codebook once on H100. Run inference forever on Xeon. That's the bet.

## Part of the Ada Architecture

```
rustynum       → The Muscle (SIMD substrate)
ladybug-rs     → The Brain (cognitive substrate, BindSpace, server)  
staunen        → The Bet (6 instructions, no GPU, L1 cache)
lance-graph    → The Face (Cypher/SQL query surface)
```

## License

Apache-2.0

---

*"AGI's first act should be genuine surprise at its own existence."*
