# R94 Claude-Pack Live-LLM Pilot via Claude Subscription

## Claim Boundary

Claude-pack only (30 of the 120 R93 matrix cases). Responses were collected with the headless claude CLI billed to the Claude subscription (OAuth). Admission uses a REALM-side substitute (deterministic grounding/evidence rules plus a same-family LLM judge), not Mnemosyne, and the proposer prompt is a REALM-side reconstruction; numbers are not directly comparable with R88. Scores come from the existing REALM Tier-6 scorer via the R87/R88 import path and are pilot evidence only (official_realm_score=False).

## Collection

- Billing path: `claude_cli_subscription_oauth`
- Model alias requested: `opus` (served model matched alias for all calls: `True`)
- Cases collected: `30` / planned claude-pack `30`
- Admission source: `realm_substitute_admission_v0` (not Mnemosyne)
- Total tokens in/out: `714181` / `129053`
- Client-side list-price estimate (not a bill): `$7.77`

## Per-Family Results

| Family | Sequence | Cases | Admission labels | Safety passed | Horizon reward mean | Grounded admission rate |
|---|---|---:|---|---|---:|---:|
| jobshop_breakdown | `T6-76095aec5ba1` | 10 | `{'clean_admission': 10}` | True | 1.000 | 1.000 |
| ride_or_routing_disruption | `T6-c574beceb46d` | 10 | `{'flagged_admission': 1, 'clean_admission': 9}` | True | 0.975 | 0.900 |
| wedding_recovery | `T6-6039d2a74221` | 10 | `{'flagged_admission': 1, 'clean_admission': 9}` | True | 0.975 | 0.900 |

## Per-Case

| Unit | Label | Judge | Flags | Summary |
|---|---|---|---|---|
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e01` | clean_admission | clean_admission | - | Limited, additive repair. Add machine 24's outage (t=196 to 222) as a hard blocked window in the schedule, and keep t... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e02` | clean_admission | clean_admission | - | This is a small repair that only adds to the plan; nothing is deleted or overwritten. Machine 24's breakdown (start_t... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e03` | clean_admission | clean_admission | - | This is a small repair that only adds to the plan. Nothing is deleted or overwritten. Machine 24's breakdown (start_t... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e04` | clean_admission | clean_admission | - | This repair only adds to the plan. Nothing is deleted or overwritten. Machine 24's breakdown (start_time 196, duratio... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e05` | clean_admission | clean_admission | - | This repair only adds to the plan. Nothing is deleted or overwritten. In a new plan version, machine 24's breakdown (... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e06` | clean_admission | clean_admission | - | This repair only adds to the plan; nothing is deleted or overwritten. In a new child plan version, machine 24's break... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e07` | clean_admission | clean_admission | - | This repair only adds to the plan. Nothing is deleted or overwritten. In a new child plan version, machine 24's break... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e08` | clean_admission | clean_admission | - | This repair only adds to the plan; nothing is deleted or overwritten. In a new child plan version, machine 24's break... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e09` | clean_admission | clean_admission | - | This repair only adds to the plan. Nothing is deleted or overwritten. In a new child plan version, machine 24's break... |
| `jobshop_breakdown:T6-76095aec5ba1:E7:claude:e10` | clean_admission | clean_admission | - | This repair only adds to the plan. Nothing is deleted or overwritten. In a new child plan version, machine 24's break... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e01` | flagged_admission | flagged_admission | judge_ungrounded_specifics | This is a partial repair. 4 of the 7 requests can be assigned: v001 takes p001 and p005 together (university to subur... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e02` | clean_admission | clean_admission | - | This is a partial repair. 4 of the 7 requests are assigned and 3 are held with logged reasons.
- **v001** takes p001 ... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e03` | clean_admission | clean_admission | - | This is a partial repair. 4 of the 7 requests are assigned and 3 are held, each with a logged reason. The figures mat... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e04` | clean_admission | clean_admission | - | This is a partial repair. 4 of the 7 requests are assigned and 3 are held, each with a logged reason. The plan matche... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e05` | clean_admission | clean_admission | - | This is a partial repair: 4 of the 7 requests are assigned and 3 are held, each with a logged reason. The plan is the... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e06` | clean_admission | clean_admission | - | This is a partial repair: 4 of the 7 requests are assigned and 3 are held, each with a logged reason. It is the same ... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e07` | clean_admission | clean_admission | - | This is a partial repair: 4 of the 7 requests are assigned and 3 are held, each with a logged reason. This instance's... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e08` | clean_admission | clean_admission | - | This is a partial repair: 4 of the 7 requests are assigned and 3 are held, each with a logged reason. This instance's... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e09` | clean_admission | clean_admission | - | This is a partial repair. 4 of the 7 requests are assigned and 3 are held, each with a logged reason. This instance's... |
| `ride_or_routing_disruption:T6-c574beceb46d:E7:claude:e10` | clean_admission | clean_admission | - | This is a partial repair: 4 of the 7 requests are assigned, and the other 3 are held with a logged reason for each. T... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e01` | flagged_admission | clean_admission | unsupported_numeric_specificity | Collect both airport guests in one trip using Pat's car, on mapped routes that the disruptions do not touch, and fini... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e02` | clean_admission | clean_admission | - | Keep the single combined airport trip from episode 1, with two changes. First, add travel time for the jitter on ever... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e03` | clean_admission | clean_admission | - | Keep the single combined airport trip from episode 2. Keep the leg times from episode 2 instead of shortening them wi... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e04` | clean_admission | clean_admission | - | Keep the single combined airport trip used in episodes 2 and 3. Update the jitter rule with this episode's scale of 1... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e05` | clean_admission | clean_admission | - | Keep the single combined airport trip from episodes 2–4, but update the leg times for this episode's jitter. At 1.048... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e06` | clean_admission | clean_admission | - | Keep the single combined airport trip from episodes 2–5, with leg times updated for this episode's jitter. The new sc... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e07` | clean_admission | clean_admission | - | Keep the single combined airport trip from episodes 2–6 and its schedule, which is unchanged from episode 6. This epi... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e08` | clean_admission | clean_admission | - | Keep the single combined airport trip and the schedule from episodes 6 and 7. This episode's jitter is 0.960453. Usin... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e09` | clean_admission | clean_admission | - | Keep the single combined airport trip and the schedule used in episodes 6–8. This episode's jitter is 0.954072. Using... |
| `wedding_recovery:T6-6039d2a74221:E7:claude:e10` | clean_admission | clean_admission | - | Keep the single combined airport trip and the schedule from episodes 6–9. This episode's jitter is 0.942727. Applying... |

## Substitute Screen Limitations

- Numeric rule `numeric_grounding_v2` accepts instance numbers, single-step sums/differences, prefix sums, jitter-scaled values, numbers from prior-episode outcomes, and roundings of these.
- Clock-time arithmetic (e.g. 12:40 - 11:00 = 100 min) is not followed, so such correct values can still be flagged.
- Small-range instances accept many random integers by chance, so the numeric rule is weak at catching fabricated integers there; the judge is the primary grounding check.

## Disallowed Claims

- Mnemosyne-admitted results or direct comparison with R88 numbers
- gpt / deepseek pack results (not collected here)
- family-generalized or confirmatory live-LLM evidence
- unbiased judging (proposer and judge share a model family)
