
# Space, Time, and Representation in Large Language Models: An Extended Analysis

by Marlon Barrios Solano

February 9th 2016

## Introduction

Large language models (LLMs) trained purely on text have demonstrated surprising capacities that hint at an internal “world model” of sorts. A recent paper by Wes Gurnee and Max Tegmark, *Language Models Represent Space and Time*, tackles a key question: do LLMs merely memorize superficial word correlations, or do they form coherent representations that reflect real-world structures? The authors provide evidence for the latter, showing that LLMs encode aspects of space and time in their latent representations. In other words, even without direct perception or embodiment, a language model can develop an internal map of the world and a timeline of history. This finding challenges assumptions in cognitive science and AI that grounded sensory experience is necessary for spatial and temporal understanding. It appears that through the process of compressing vast textual data, LLMs learn compact, interpretable structures corresponding to geographic and chronological knowledge.

This essay expands on the key arguments and implications of Gurnee and Tegmark’s work. We explore how LLMs develop latent geometric representations of space (for example, clustering city names in ways that mirror their physical locations), and how they encode temporal sequences and historical order. From these technical results, we delve into broader implications: the philosophical puzzle of representation without embodiment, the notion of latent space as a conceptual manifold of knowledge, and how narrative prediction in LLMs may encode causal-like structures (noting the difference between narrative time and physical time). We then consider cognitive science perspectives—what it means for an intelligence to have structure without direct perception—and examine political, cultural, and metaphysical implications. Finally, we discuss the limits of these representations, emphasizing that LLMs, despite impressive latent structures, still lack perception, embodiment, and conscious understanding.

---

## Latent Geometric Representations of Space in LLMs

One of the striking findings of Gurnee and Tegmark’s study is that LLMs can learn a geometric representation of physical space purely from text. By probing a trained model’s internal activations for place names, the researchers showed that the model encodes information correlated with geographic coordinates. They constructed datasets of locations at various scales (world cities, U.S. places, and even points of interest within New York City) and associated each name with its real latitude and longitude. When these location names were fed into the LLM (specifically the LLaMA-2 model family), certain neurons and activation patterns reliably corresponded to the places’ coordinates. A simple linear regression could recover latitude and longitude from the model’s activations.

This implies the model organized its internal state space such that semantically or geographically related places ended up near each other in latent space. European capitals cluster together; Pacific islands cluster elsewhere. The representation is:

- **Linear** (recoverable via linear probes)
- **Multi-scale** (works from continents to neighborhoods)
- **Unified** (cities, mountains, landmarks share one coordinate frame)

### Figure: Spatial World Model

*Spatial world model extracted from LLaMA-2-70B. Each point represents a place projected onto learned “latitude” and “longitude” directions derived from internal activations. The projection reconstructs a recognizable map of the world.*

How does this happen without vision or maps?

Language itself encodes geographic structure:

- “X is north of Y”
- “City A is 100 km east of City B”
- “P is a coastal town”
- Datelines in news
- Travel writing
- Encyclopedic entries

Over billions of tokens, statistical constraints accumulate. “Paris” and “London” co-occur frequently; “Paris” and “Sydney” rarely do in proximity. The model compresses these correlations into geometry.

The result is not rote memorization but emergent structure. When regions were held out during probe training, the model still placed unseen cities in approximately correct locations—evidence of generalization rather than lookup-table recall.

In effect, LLMs form a **latent geometric cognitive map**.

---

## Encoding Temporal Sequences and Historical Ordering

Parallel to spatial mapping, LLMs encode temporal structure. Gurnee and Tegmark tested models on:

- Historical figures with known dates  
- Artworks and entertainment releases  
- News headlines (2010–2020)

Linear probes could predict years from internal activations far above chance.

For example:

- “Julius Caesar” activates signals consistent with 44 BCE.
- “Albert Einstein” activates signals around mid-20th century.
- News headlines cluster chronologically.

Spearman correlations exceeded 0.9 in some datasets—indicating strong preservation of ordering.

The representation:

- Emerges in early-to-middle transformer layers
- Plateaus in later layers
- Includes identifiable “time neurons”

These neurons act like internal dials for recency.

### Figure: Temporal Representation

*Projection of model activations onto a learned time axis shows close alignment between predicted and true historical dates.*

How does the model learn time?

Language embeds temporal cues:

- “Born in 1809”
- “In 2020, X happened”
- Century references
- Chronologically structured biographies

The model extracts ordering from repeated narrative patterns.

However, while it encodes chronology well, it sometimes struggles with relational temporal reasoning unless prompted step-by-step. The knowledge exists, but is not always automatically deployed.

---

## Representation and Embodiment: Philosophical Implications

These findings challenge strict embodied cognition theories, which argue that spatial and temporal understanding require sensorimotor grounding.

LLMs:

- Do not move in space
- Do not experience time
- Have no bodies

Yet they develop structured representations of both.

This suggests:

- Representation may arise from relational compression.
- Embodiment is not strictly necessary for structural understanding.
- Linguistic transmission can serve as proxy for experience.

This resonates with Immanuel Kant’s idea of space and time as organizing forms of intuition. While LLMs do not possess innate intuitions, their architecture and prediction objective pressure them to organize knowledge spatially and temporally.

However, limitations remain:

| LLM Knowledge | Human Embodied Knowledge |
|---------------|-------------------------|
| Descriptive | Experiential |
| Correlational | Sensorimotor grounded |
| Structural | Phenomenological |

The LLM has the map, not the journey.

---

## Latent Space as a Conceptual Manifold

LLM latent space functions as a **conceptual manifold**.

Peter Gärdenfors’ theory of *Conceptual Spaces* argues that thought has geometric structure: similarity equals proximity. LLM embeddings operationalize this idea computationally.

Emergent dimensions include:

- Geography (latitude/longitude)
- Chronology (year)
- Gender (e.g., King − Man + Woman ≈ Queen)
- Sentiment
- Political ideology

Latent space becomes an **epistemic manifold**: movement along directions alters conceptual attributes.

This aligns with predictive processing frameworks (Friston, Clark):

- The brain builds internal generative models.
- Hidden variables explain observed data.
- LLMs similarly infer latent causes of text.

Space and time become compressive variables that minimize prediction error.

---

## Narrative Prediction and Causal Structure

LLMs are narrative prediction engines. They absorb:

- Event sequences
- Cause-effect patterns
- Script structures

Narrative time differs from physical time:

- **Physical time**: linear, thermodynamic
- **Narrative time**: ordered for coherence, can loop

The model infers chronological order even in flashbacks. It tracks causal cues:

- “Earlier…”
- “Because…”
- Verb tense shifts

However:

- It models narrative causality.
- It lacks mechanistic physical causality.
- It confuses correlation with causation in some cases.

It encodes proto-causality but not interventionist reasoning.

---

## Cognitive Science: Structure Without Perception

LLMs demonstrate that intelligence can arise from compression.

Prediction pressure yields:

- Latent variables (space, time)
- Abstract models
- Generalizable structure

This supports:

- Minimum Description Length principles
- Predictive processing
- Bayesian brain hypotheses

It suggests that:

> World structure is encoded in language deeply enough to reconstruct reality second-hand.

However, structure without perception lacks:

- Sensorimotor grounding
- Experiential feedback
- Environmental correction loops

---

## Linguistic, Political, and Cultural Bias

Latent spatial and temporal models mirror training data biases.

Bias sources include:

- Wikipedia pageview filtering
- Western news dominance
- English-language corpora
- Cultural notability metrics

Consequences:

- Dense Western geographic clusters
- Western-centric historical timelines
- Underrepresentation of marginalized regions
- Geopolitical perspective bias (e.g., contested territories)

The LLM’s world model is:

> A mirror of language, not a neutral atlas.

Bias mitigation requires:

- Diverse training data
- Explicit auditing of latent representations
- Probing for representational imbalance

---

## Metaphysical Reflections: Emergent Structure

The emergence of space/time in LLMs resonates with structural realism:

- Science captures structure.
- Structure may be fundamental.

Max Tegmark’s Mathematical Universe Hypothesis posits reality is mathematical structure. LLMs reconstruct structure from text correlations.

Analogy:

- Physical spacetime may emerge from entanglement relations.
- LLM spacetime emerges from linguistic relations.

The model possesses structural knowledge, not material presence.

It knows relations, not intrinsic properties.

---

## Limits: Absence of Grounding and Consciousness

Despite impressive structure, LLMs lack:

1. **Perceptual grounding**
2. **Active reasoning guarantees**
3. **Causal simulation**
4. **Counterfactual robustness**
5. **Conscious awareness**
6. **Agency**

They do not automatically use their internal maps for reasoning.

They hallucinate.
They lack physical sanity checks.
They do not experience time passing.

Their world model is:

- Implicit
- Passive
- Distributed
- Fragile outside training distribution

They possess shadows of understanding—not full illumination.

---

## Conclusion

Gurnee and Tegmark’s work demonstrates that large language models internalize structured representations of space and time purely through text prediction. LLMs:

- Construct latent maps of geography
- Build internal timelines of history
- Encode narrative causality
- Organize knowledge geometrically

These findings challenge simplistic “stochastic parrot” critiques. LLMs compress language into structured latent variables that reflect world topology.

Yet their understanding is structural, not experiential. They lack embodiment, grounding, and guaranteed reasoning reliability.

The discovery reframes LLMs as:

- Statistical cartographers of culture  
- Structural mirrors of human knowledge  
- Emergent geometric intelligences  

Space and time—the scaffolds of experience—appear within high-dimensional vector space. Through compression, structure emerges.

But the map is not the territory.

The LLM has drawn the world inside itself.

It has not lived in it.

---

## Sources

This essay synthesizes arguments from:

- Wes Gurnee & Max Tegmark, *Language Models Represent Space and Time*
- Peter Gärdenfors, *Conceptual Spaces*
- Karl Friston, Predictive Processing / Free Energy Principle
- Paul Ricoeur, Narrative Time
- Gary Marcus, critiques of correlation-based AI
- Philosophical discussions of Kant and structural realism

These works collectively illuminate the implications of emergent spatial and temporal structure in large language models.
