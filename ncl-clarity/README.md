# NCL, Epoch Timing, and Constitutional Enforcement  
### Under the Cardano Constitution and CIP-1694

## 1. Introduction

The **Net Change Limit (NCL)** is a mandatory constitutional safeguard that restricts how much ada may be withdrawn from the Cardano Treasury within a defined period. Although the NCL appears in the Guardrails Appendix of the Constitution, its enforcement power derives from **Article IV**, which governs treasury withdrawals.

Because NCLs are defined using **Info actions**, and because CIP-1694 clarifies that the Constitution “cannot be enforced on-chain,” the ledger has **no ability** to enforce NCL requirements.  
Therefore, enforcement depends entirely on **Delegated Representatives (DReps)** and the **Constitutional Committee (CC)**.

This report explains the NCL, its timing requirements, and a generalized enforcement rule.  
It concludes with an example using the **current 2025 NCL**.

*Sources:*  
- Cardano Constitution - ipfs://bafkreiazhhawe7sjwuthcfgl3mmv2swec7sukvclu3oli7qdyz4uhhuvmy  
- CIP-1694 - https://github.com/cardano-foundation/CIPs/tree/f4f6d499ff030c5eed1e53174f8a7c2fba326829/CIP-1694  
- Current 2025 NCL Governance Action - ipfs://bafkreiaqno22swabd3kcqt2awtgwaucdzaagacoemxwadm3exrchhnfite

---

## 2. Constitutional Basis of the NCL

### 2.1 A Net Change Limit must exist

The Constitution states:

> “A net change limit for the Cardano treasury’s balance **per period of time must** be agreed by the DReps…”  
> *(TREASURY-01a)*

If no NCL exists for a given period, **no treasury withdrawal is constitutionally possible** in that period.

---

### **2.1.1 The Constitution does not require an NCL to have a fixed end-date**

A key detail often misunderstood is that the Constitution **does not require an NCL to specify a hard end-epoch**.

TREASURY-01a only requires:

- a **net change limit**,  
- defined **per period**,  
- agreed by the **DReps**.

It does *not* require:

- an explicit end-date,  
- an explicit epoch boundary, or  
- a fixed termination point.

This means:

> **A valid NCL period may begin at a defined epoch and continue indefinitely until the DReps approve a new NCL that supersedes it.**

In other words:

- The “period” may be **open-ended**,  
- Its end is implicitly the moment a new NCL is approved,  
- A rolling or continuous NCL is fully constitutional.

Nothing in the Constitution prevents an NCL from being defined as:  
**“Starting at epoch X and remaining in force until replaced.”**

This is important because:

- DReps control spending capacity  
- The Constitution allows them flexibility in defining periods  
- Open-ended NCL periods reduce governance gaps and timing risks

This flexibility is built directly into the constitutional text.

---

### 2.2 Withdrawals must respect the “then applicable” NCL

Article IV, § 3 contains the central rule:

> “Withdrawals… that would cause the Cardano Blockchain treasury balance to violate the **then applicable net change limit** shall not be permitted.”

Key implications:

- The NCL that matters is the one **in effect at the moment the withdrawal enacts**.  
- If no NCL exists at enactment time → the withdrawal **cannot be permitted**.  
- Ratification must evaluate the future NCL, not just the current one.

---

### 2.3 Ratification requires all prerequisites to exist

Guardrail TREASURY-04a states:

> “Withdrawals… must not be ratified until there is a Cardano Community approved… budget then in effect…”

Since Article IV § 3 binds withdrawals to the “then applicable” NCL:

> A withdrawal must not be ratified unless the NCL for the *enactment epoch* is known and already established.

---

## 3. Timing of Ratification and Enactment (CIP-1694)

CIP-1694 defines the timing of governance actions:

> “Governance actions are enacted at the epoch boundary **after their ratification**.”

Thus:

- Ratification occurs in epoch **N**  
- Enactment occurs automatically in epoch **N+1**

Therefore:

> **The CC must evaluate the NCL for epoch N+1, not epoch N.**

If the NCL does not cover epoch N+1, the withdrawal must not be ratified.

---

## 4. Why the Ledger Cannot Enforce the NCL

### 4.1 Info actions have no on-chain effect

The Constitution states:

> “‘Info’ actions have **no on-chain effect** other than to record such actions…”

And CIP-1694 reiterates:

> “The Constitution… cannot be enforced on-chain.”

Therefore:

- The ledger cannot read or validate the NCL  
- The Guardrail Script does not enforce TREASURY-01a or TREASURY-02a  
- If CC ratifies a withdrawal that violates the NCL, **the ledger will still execute it**

This makes enforcement a **human governance responsibility**, not a machine rule.

---

## 5. Enforcement Responsibilities

### 5.1 The Constitutional Committee

Article VII, § 1 states:

> “The Constitutional Committee… ensures governance actions… are consistent with this Constitution.”

Thus the CC must refuse to ratify any withdrawal that:

- Exhibits no NCL coverage at enactment time  
- Exceeds the upcoming NCL  
- Fails to satisfy Articles IV.1–IV.5  

This is a **mandatory constitutional obligation**.

---

### 5.2 Delegated Representatives (DReps)

DReps are explicitly responsible for defining the NCL:

> “A net change limit… must be agreed by the DReps…”

If DReps fail to establish an NCL for a future epoch, they effectively prevent any constitutional withdrawal from occurring in that epoch.

DReps govern the **spending capacity** of the treasury.

---

## 6. Universal Rule for All Withdrawals

From the Constitution and CIP-1694, we derive the following universal principle:

---

## **A treasury withdrawal may only be ratified if an NCL will be in effect during the epoch in which the withdrawal enacts, and the withdrawal amount does not exceed that limit. Because the NCL is off-chain and unenforced by the ledger, DReps and the Constitutional Committee must enforce this requirement.**

---

This rule applies to:

- all withdrawals  
- all budgets  
- all epochs  
- all governance cycles  

It is never optional.

---

## 7. Example Using the Current Net Change Limit (2025 NCL)

The uploaded NCL governance action establishes the following parameters:

- **Coverage period:** From the start of epoch *532* through the end of epoch *604*  
- **Duration:** 72 epochs  
- **Limit:** 350,000,000,000,000 lovelace (350M ada)

From the proposal:

> “The 2025 Net Change Limit will begin at the start of Epoch 532 and continue for 72 epochs, finishing at the conclusion of Epoch 604.”

Therefore:

> **Any withdrawal enacting after epoch 604 must not be ratified unless a new NCL has been defined for the subsequent period.**

If no new NCL is established, the CC must treat the withdrawal as unconstitutional to ratify, because:

- Article IV § 3 requires an NCL at enactment  
- TREASURY-01a requires that an NCL exist  
- TREASURY-02a prohibits withdrawals exceeding the NCL  
- The ledger cannot enforce compliance  

Thus, **the CC becomes the active enforcement mechanism**.

---

## 8. Final Conclusions

1. The NCL is a mandatory constitutional safeguard established by DReps.  
2. Withdrawals must comply with the NCL **at enactment**, not merely at ratification.  
3. The Constitution does **not** require NCLs to have fixed end-dates; periods may be open-ended.  
4. Because the NCL is defined via an Info action, the ledger **does not** enforce it.  
5. Therefore, **DReps and the CC must enforce NCL compliance** manually.  
6. A withdrawal must not be ratified unless an NCL exists for the enactment epoch.  
7. Under the current 2025 NCL, no withdrawal may constitutionally enact after epoch 604 without a new NCL in place.

---
