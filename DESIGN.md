ParcelCraft — Design Overview (Phase‑1)

> Status: Frozen for Phase‑1



This document describes the minimum complete design required to ship ParcelCraft Phase‑1. It is intentionally concise, technical‑friendly, and scope‑locked.


---

Core Idea

Land is not a blank canvas. Every map starts with pre‑defined land parcels that have owners, values, resistance, and restrictions. Players must acquire land before building.

This layer sits between terrain and construction and does not rewrite the base economy.


---

Phase‑1 Goals

Introduce meaningful friction to expansion

Make every city layout feel intentional

Avoid micromanagement and heavy simulation

Maintain strong performance



---

Systems Included (Phase‑1)

1. Parcel Generation

Runs once at map start

Generates non‑uniform parcels

Influenced by terrain, water, fertility, legacy paths

Parcel data persists for entire save


Parcel attributes:

Owner type

Base value

Resistance level (low / medium / high)

Restriction flags



---

2. Ownership Types

Government

Private

Agricultural

Forest / Protected

Industrial legacy


Ownership affects acquisition cost, availability, and restrictions.


---

3. Acquisition Methods

Players must acquire parcels before building.

Purchase: High cost, immediate ownership

Lease: Low cost, time‑bound, build limits

Eminent Domain: Forced, policy‑locked, happiness penalty

PPP: Shared control, limited zoning


Each method has cost, delay, and soft consequence.


---

4. Hard Restrictions

Some parcels:

Cannot be built on

Require specific policies

Allow only limited infrastructure


Restriction violations result in construction denial or permanent penalties.


---

5. UI / UX

Toggleable parcel overlay

Single land panel

No popup spam

Clear preview of cost and consequence



---

What Phase‑1 Is NOT

These are explicitly excluded from Phase‑1:

Protest crowds or AI movements

Political or election systems

Economy rebalance

Courts, litigation, or lawsuits

Private developer AI


These are Phase‑2+ considerations only.


---

Technical Constraints (Intent)

No per‑citizen simulation

Event‑based logic only

Lightweight data structures

Minimal update frequency

Optional per save, safe removal



---

Success Criteria

Phase‑1 is successful if:

Players must rethink expansion

Cities stop being perfect grids

The system is noticeable within 30 minutes

No major performance complaints appear



---

Ownership & Direction

Design direction and scope control are centralized to avoid feature creep. Expansion beyond Phase‑1 requires explicit scope review.
