# Encrypted Storage at Scale

I treat every system design session like a tide chart: know when to lean on theory, and when to let pragmatism guide the build. At MongoDB, that means turning cryptographic protocols into operational defaults, not bolt-on features.

## Designing for durability and privacy
- Map the data flows first, then decide which operations deserve end-to-end guarantees.
- Make failure modes explicit; encrypted systems need graceful degradation rather than silent drops.
- Measure user friction—if the protocol is too heavy, the feature will be bypassed.

## Field notes from the coast
I keep a running list of "storm drills" for our services. Once a quarter we:
1. Rehearse a controlled key-rotation across shards.
2. Simulate a byzantine node and verify audit trails stay intact.
3. Benchmark the overhead of new primitives against real traffic traces.

> Security isn’t a sprint; it’s a tide that reshapes the shoreline every day.
