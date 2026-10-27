---
layout: page
title: research
permalink: /research/
description: 
nav: true
nav_order: 2
---

<!-- TODO: add images -->

My main research interest is about how **opinions, beliefs, and norms spread and synchronise** within social groups, 
giving rise to different patterns of collective human behaviour such as coordination, polarisation, or collective 
intelligence. I am particularly interested in the effects of **strategic influence** (campaigning, advertising, nudging, 
or disinformation) on these dynamics.
More broadly, I am interested in how whole belief systems (ideologies, norms, cultures) emerge, compete, and evolve.

My approach is quantitative and draws on several toolboxes: **agent-based modelling** to simulate complex scenarios, 
**statistical physics** to understand models mathematically, **network science** to capture social and biological 
structure, **Bayesian statistics** to fit models to data, **game theory** to understand incentives and strategies, and 
**AI and data science** to work with large empirical datasets. 
Along the way, I have also applied the same toolbox to quite different problems, from the clustering of chronic diseases 
to the computation of political proximity for informing in party voting.
I believe these methods have the most impact when combined with the knowledge of researchers from other disciplines.
(More about that on my [interdisciplinarity](/interdisciplinarity/) page).

Below is an overview of the main topics I have worked on. You can find all related papers on the [publications](/publications/) page.

---

#### Information flow, collective intelligence, and external influence

Social groups process information collectively: through their network of interactions, individuals exchange signals and 
opinions, and from these local exchanges, self-organised collective behaviours emerge. I study how the **structure of 
social networks** and the **behaviour of individuals** shape this flow of information, and how **external 
actors** (campaigners, advertisers, propagandists, or automated agents) can steer it, for better or worse.

From the point of view of collective intelligence, on question is that of **collective sensing**.
How can a group of agents with error-prone individual perception collectively track a changing environment? We studied 
how communication among networked agents can enhance sensing, and how this depends on network 
topology, finding there is a delicate balance between increasing confidence in the solution and getting locked into a
completely wrong solution with high confiddence ([Entropy 2022](https://doi.org/10.3390/e24050738); 
[Complex Networks 2021](https://doi.org/10.1007/978-3-030-93413-2_30)).

These collective sensing perspective can be taken to the online social sphere, where individuals distribute 
information (and misinformation) and there is a collective effort to relay true information and filter out less credible
ones.
A first step for approaching this is understanding **how controversial information flows** in this specific environment; i.e.,
how agents can be influenced by the spread of fake news and, in turn, influence others. This includes understanding how 
contextual aspects shape these dynamics (e.g., the structure of online social networks or the mediation by AI algorithms), 
and how **agent-based simulations** can be used to design and test interventions that prevent the spread of disinformation.
Modelling disinformation cascades that provoke debunking, spread over heterogeneous networks, and compete for users'
limited attention, we found that debunking is double-edged (it curbs the reach of appealing content but helps unappealing
content reach new audiences) and that heterogeneous networks are easy to ignite yet hard to saturate, an effect that
limited attention cancels but recommendation algorithms may restore
([Complex Networks 2026](https://arxiv.org/abs/2610.13839)).

However, information doesn't just appear and flow but is also **steered by influential actors** who seek to advance their
own benefit (e.g., advertisement, political campaigning) or the collective benefit (e.g., public policy).
When a **strategic actor** seeks to distribute her influence over a social network, how do optimal strategies look like?
I studied this question in models of opinion dynamics, combining statistical physics, network science, optimisation, and 
game theory ([PhD thesis](https://eprints.soton.ac.uk/485922/)).
In adversarial settings with two competing influential actors, I found that optimal strategies follow two simple
heuristics: **shadowing** (targeting the same individuals as the opponent) and **shielding** (targeting 
their neighbours), while network structure plays only a secondary role ([PLOS ONE 2021](https://doi.org/10.1371/journal.pone.0252515); 
[Complex Networks 2019](https://doi.org/10.1007/978-3-030-36687-2_57); [AAMAS 2020](https://eprints.soton.ac.uk/438158/)).
In populations with biased individuals, whether to target hard-to-convince individuals depends 
strongly on the available budget ([CompleNet 2020](https://doi.org/10.1007/978-3-030-40943-2_10)).


---

#### Polarisation, party competition, and voting

Polarisation is one of the most pressing challenges for democratic societies, and I study it from several angles: how 
the strategies of political parties and the structure of individuals' belief systems drive societies towards consensus 
or division, and how tools can help voters navigate an increasingly complex political landscape.

- **Party competition and consensus.** Using agent-based simulations, I studied how parties' fight to set the political 
agenda (by changing which issues voters consider important) interferes with consensus formation in the electorate. 
Depending on party positions, competition can foster polarisation, but it can also facilitate a consensus that would 
otherwise not be reached ([ABMHuB 2021](https://eprints.soton.ac.uk/449484/)).
- **Cognitive models of belief systems.** Many opinion dynamics models favour mathematical tractability over realism. I 
am interested in models grounded in cognitive science, where beliefs are not isolated but form **structured systems**. 
We have analysed a cognitive model of structured beliefs to identify which conditions lead to consensus or polarisation 
([WIVACE 2024](https://doi.org/10.1007/978-3-031-93631-9_3)) and how cognitive coherence and social influence together 
can drive national-level polarisation across Europe.
- **Ongoing work** includes measuring elite polarisation in Argentina through legislative co-sponsorship networks and
understanding how private messages may mitigate the polarising dynamics of young users on TikTok.

---

#### Data-driven applications of network and statistical methods

Advanced methods only have impact in other fields when their results can be understood, trusted, and communicated by the 
domain experts who use them. In my work with biomedical data, I aim to apply network, statistical, and machine learning 
methods in an **interpretable and transparent** way, making their assumptions explicit and their outputs meaningful to 
clinicians, biologists, political and social scientists, etc.

**Multimorbidity networks from health records.** Working with clinicians and researchers from six disciplines, I applied 
**Bayesian inference and network science** to electronic health records covering millions of patients to uncover 
connections between long-term conditions ([eBioMedicine 2024](https://doi.org/10.1016/j.ebiom.2024.105081), [Python package](https://github.com/Juillermo/ABC)).
In our work, we also explored clustering of long-term conditions and warned against the risks of applying methods blindly.
Clustering studies of multimorbidity often report widely different clusters, partly because what counts as a "cluster" 
is vaguely defined and methodological details are left implicit. We proposed a transparent pipeline that adapts to 
different cluster definitions, together with evaluation scores that make explicit the assumptions aligned with the 
research aims. Applied to over 7 million patients in England, it shows how much clusters can change with parameter 
choices, and the risk of reporting a single clustering result ([medRxiv 2026](https://www.medrxiv.org/content/10.64898/2026.05.25.26353178v1)).
Further, how conditions cluster may strongly differ when the anlysis is stratified by age and sex, which limits 
comparison and reproducibility. We demonstrated these differences with our data and argued that researchers should 
explicitly justify their stratification choices given their study aims ([medRxiv 2025](https://www.medrxiv.org/content/10.1101/2025.02.06.25321779v1)).

**Voting advice applications.** I proposed a machine-learning method that learns how users weigh and compare policy 
issues to better match them to parties ([JEPOP 2022](https://doi.org/10.1080/17457289.2020.1760282)), argued for normative criteria to make these tools increase
voters' political competence ([IJEG 2021](https://doi.org/10.1504/IJEG.2021.116869)), and contributed to the survey design of [Aquienvoto.org](https://aquienvoto.org), used
nearly two million times in the 2019 Spanish general elections.

**Interpretability of machine learning.** Deep learning models are often black boxes to the scientists who use them. I 
applied **saliency maps** to convolutional neural networks for protein secondary structure prediction, to understand 
which parts of the input drive their predictions ([ICASSP 2019](https://doi.org/10.1109/ICASSP.2019.8683603)).