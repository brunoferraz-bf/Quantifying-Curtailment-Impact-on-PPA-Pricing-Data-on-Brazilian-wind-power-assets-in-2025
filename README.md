# Quantifying Curtailment Impact on PPA Pricing Data on Brazilian wind power assets in 2025
Exploratory analysis of the economic impact of curtailment on a 688 MW wind complex (2025). The study evaluates physical restriction patterns and financial exposure to PPA contracts and spot prices (PLD), using public data from ONS, EPE and CCEE to quantify risk and implied contract price adjustments.

# Overview

This study quantifies the economic impact of energy-related curtailment on a Brazilian wind generation asset in 2025 and estimates its implied effect on long-term PPA pricing.

The objective is not to advocate cost transfer to consumers, but to measure economic exposure associated with non-controllable operational restrictions and translate it into a risk premium framework.

# Data Sources

The analysis is based on publicly available 2025 operational and market data from:

ONS – semi-hourly wind generation and restriction data

CCEE – hourly PLD (spot price) data

Wind asset analyzed: "Conjunto Eólico Campo Largo e Conjunto Eólico Campo Largo II"

Installed capacity: 688 MW

Firm Energy (Garantia Física): 359 MWmed

Submarket: Northeast (NE)

PLD hourly prices were converted to 30-minute resolution assuming constant price within each hour.

# Key Modeling Assumptions
#### 1. Curtailment Definition

Curtailment is defined as:

reference_generation − actual_generation

when a restriction is binding and the reference generation exceeds the realized generation.

Only energy-related restrictions ("ENE") are considered.

#### 2. Firm Energy Framework

The PPA is assumed to be structured over Firm Energy (359 MWmed).

Exposure occurs when realized energy is insufficient to meet the contracted level, requiring settlement at PLD.

#### 3. Cost Decomposition

Curtailment impact is decomposed into two components:

### Causal Curtailment Cost
When sufficient wind was available to meet firm energy, but restriction caused deficit and PLD exposure.

### Incremental Risk Cost
When structural generation deficit already existed and curtailment further increased exposure.

This separation allows identification of direct restriction impact versus marginal risk amplification.

#### 4. Energy Conversion

All calculations are performed at 30-minute resolution.
MWmed values are converted to MWh by dividing by 2.

#### 5. Risk Premium Estimation

The annual curtailment cost is divided by total contracted annual energy:

Firm Energy × 8760 hours

This results in an implied PPA premium (R$/MWh) required to compensate for observed curtailment risk in 2025.

Risk Metrics

Event-level impacts are expressed as a percentage of the estimated annual premium.

The study computes:

Mean event impact

Historical VaR (95%)

Historical CVaR (95%)

No parametric distributional assumption is imposed.
Risk metrics are fully empirical.

Scope and Limitations

Analysis is historical (2025 observed data).

No forward-looking simulation is applied.

No correlation modeling between PLD and curtailment is assumed.

Turbines are assumed fully available (100% nominal availability).

Results reflect observed exposure, not regulatory or contractual mitigation mechanisms.

This is a risk measurement exercise, not a regulatory or pricing recommendation.

# Objective

The central question addressed:

How much can curtailment increase the implied PPA price when evaluated from a risk perspective?

The study translates operational restriction into financial exposure and provides a structured framework to quantify its economic significance.
