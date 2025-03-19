# Next step of AI for network operations, Daniel King @Lancaster University
Daniel Huang @ZTE: How can we ensure the reliability of the LLM model output for some critical action such as network deployment? There is not enough high quality data from the network area, unlike the general language.

Reza : Not all usecases use generative AI. Some are using traditional rule based learning algorithm. How do you use the LLM depend on the usecase. Each usecase may have different remedy solution. 

Daniel King: For generative AI, the output needs to be verified first. There are some open source guardrail solutions. Back when neural net is popular, operators have some doubts. They find that the solution proposed by neural net are not repeatable. Thus they were skeptical. 

xxx: Sometimes AI is used for better performance. We already have testing suite for this. So this is not a problem. Other usecase, not so. There is no general solution for all usecases. 

Daniel King: Operator are ultimately responsible for AI operations. A complicated system can may mistakes. Call for operator to collect and share more data to make LLM system more robust.

# A Framework for LLM-Assisted Network Management with Human-in-the-Loop, Mingzhe Xing @Beijing Zhongguancun Laboratory
No discussion.
# Broadband Network Gateways with AI, Haiyang Zhang @H3C
Boris	Khasanov @MWS: What is the hardware requirement of IBNG compared with traditional BNG? How many session does it need to serve?

Weiqiang Cheng @China mobile: We already do some trials. 1 BNG 20 K families. 20K 5% ‎ = 1 K requirement. Load is not big. Deepseek is low cost model. 

Daniel Huang @ZTE: The AI is running in the control plane or data plane?

Weiqiang Cheng @China mobile: Both. BNG is very special device, one hand you should use AI thchnology so to optimization the operation. you can detect the less quality subscriber, at that monment, it is a AI for operation. On the other hand, we introduce something AI edge computing, aside the BNG in the edge computing resource, for example deepseek servcice. it is a really good business solution.

# Model Distribution Network Considerations, Jian Song @China Mobile
Boris	Khasanov @MWS: For the distributed MDN deployment, what is the requirement of link speed between MDN nodes.

Weiqiang Cheng @China mobile: It is pretty large now, x Gbps per user. But we are exploring some improvement which will reduce the bandwidth requirment by a lot. It is really good for operators because we would like to leverage our edge computing resources.

# KVCache Distribution, Hang Shi @Huawei

Yong Cui @Tsinghua University: 
1. we need to store the KV chache, domain knowledge is very important too. And it may be larger than the user prompt. 

2. we are going store KV chche, cloud or router? we need to think the effencicy
what is the most important factor, Latency?

Hang Shi @Huawei: Agree about the domain knowledge. especially in RAG case. 

The KVCache should be put near to the user because it need to be fetch instantly to do the decode process, returnning answers to user query. Then we have a problem because edge devices is limited in terms of compute and storage. So we need a distritbuted KVCache storage system to serve the KVCache together using many edge devices.

Boris Khasanov @MWS: Is there any existing protocol for KVCache distribution?

Hang Shi @Huawei: Mostly inside datacenter and it is proprietary. To bring it into the wider internet, an open/interopable protocol is needed to do the KVCache discovery and transmission.


# Open Discussion
Weiqiang Cheng @China Mobile: We may need to pay attention to AI agent. Multiple AI agents deployed by different parties need to collaborate. Need a protocol between those agents.

Aijun Wang @China Telecom: For protocol between agents, we have a related sidemeeting called DMSC which will discuss the distributed communication between different micro services.

xxx: A lot of AI 4 netowrk ops usecases, we needs to deep dive into each of them, find out what is the gap of IETF protocol, then we dicides if new protocol is needed.

Dainiel King: May be we can start from one or two usecases.

Yong Cui @Tsinghua University: we consider the AI for net, transimit some net data, maybe we can consider some yang model
if we need other information, the yang model cannot tramsit, it is a running status/decision dispath which yang model cannot afford to dispatch.it could be a new topic

Weiqiang Cheng @China Mobile: For AI inference, some business have very stringent security requirement for deepseek model. We should think about security of AI inference service.

We also introduce deployment archi, MDN, prefill fcntion located in central data center, decode in edge. Then you have new network requriement to connect the prefill and decode.

Hang Shi @Huawei: AI inference will be the next big wave of application. IETF should pay attention. Finding out what is the new requirement for the protocol.

Now the high end AI system is mostly close source. Open and interopable standard can bring more players and reduce the cost to make AI affordable for everyone. 

