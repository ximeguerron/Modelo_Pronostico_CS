* * *
  * # Modelos de Pronóstico para la Monitorización de la Calidad de Servicios Cloud
* * *

## Indice {#Home}
**1. Taxonomía de métricas para servicios cloud** (#tax)
PLANNING
1.1. [Search Protocol](#Protocolo)
1.2. [Search Strings](#busqueda)
CONDUCTING
1.3. [Primary Studies](#estudios)
1.4. [Quality Assessment](#qa)
REPORTING
1.5. [Taxonomy of QoS metrics for cloud services](#clasificacion)

**2. Modelo de Calidad para servicios cloud** (#qmodel)
2.1. [Quality model metamodel](#metamodel)
2.2. [Method](#method)
2.3. [Building the quality model](#building)
2.4. [Quality model for cloud services](#model)

**3. Aplicación del Modelo en un Entorno Industrial**(#qcaso)

**4. Procesos de Modelado para el Pronóstico de QoS**

**5. Modelos de Pronóstico de QoS para servicios cloud**
5.1. [Dataset](#datos)
5.2. [Jupiter Notebooks](#notebook)
5.3. [BI-GRU Accuracy Metrics](#MetricBiGru)
5.4. [LSTM Accuracy Metrics](#MetricLSTM)
5.5. [BI-GRU model predictions](#BiGru)
5.6. [LSTM model predictions](#LSTM)
5.7. [ARIMA model predictions](#ARIMA)
5.8. [AUTO ARIMA model predictions](#AUTOARIMA) 

* * *


## 1. Taxonomía de métricas para servicios cloud {#tax}
En esta sección puede encontrar información relevante relacionada con la **Taxonomía de métricas para servicios clou**. 
La metodología y los resultados de la investigación se detallan a continuación.

### Planning 
### 1.1. Search Protocol {#Protocolo}
Defining the objective:
```markdown
This research aims to systematically identify and taxonomically classify 
available evidence on quality metrics for cloud services and provide a 
holistic comparison to analyze potential limitations of existing research
```

The main research question addressed is:
```markdown
What metrics have been used to evaluate the internal and external 
quality of cloud services and how are they measured and used?
```

The resulting subquestions are: 

```markdown
•	RQ1: What quality characteristics and attributes were evaluated?
•	RQ2: What type of metrics were they?
  ─	RQ2.1: If the metric is base, what unit was used to calculate it?
  ─	RQ2.2: If the metric is derived, what measurement function and unit were used to calculate it?
•	RQ3: Are there tools to support the measurement process, and, if so, which ones?
•	RQ4: What type of measurement results from the metrics provided?
•	RQ5: During which phases of the cloud service lifecycle were these metrics used?
•	 RQ6: For which type of stakeholders (cloud roles) are these metrics relevant?
•	RQ7: To what type of cloud service (i.e., SaaS, PaaS, IaaS) were these metrics applied?
•	RQ8: What cloud artifacts or resources were measured?
•	RQ9: Which validation method was used to provide evidence about the metrics’ usefulness?
```

### 1.2. Search Strings {#busqueda}

The search string selected is shown below:

Concept	| Alternative Terms or Synonyms
------------ | -------------
Measure	| ((metric* OR measur*) AND
Quality 	| (QoS OR "quality of service" OR "quality model" OR "evaluation model" OR "assessment model" OR "quality in cloud" OR "quality of cloud") AND
Cloud	| (cloud*))

The search string applied to the same metadata (_title, abstract and keyword_) of the articles. 
The period or search dated from _2006_ to _November 2018_. 

The search string was adapted to each digital library (IEEE Xplore, ACM Digital Library, ScienceDirect y Springer Link) and listed below: 

Digital Libray| Search String | Search Metadata |Constraints
------------ | ------------- |------------ | ------------- 
IEEE Xplore |((("Publication Title":attribute OR "Publication Title":characteristic OR "Abstract":attribute OR "Abstract":characteristic OR "IEEE Terms":attribute OR "IEEE Terms":characteristic OR "Author Keywords":attribute OR "Author Keywords":characteristic) OR ("Publication Title":metric OR "Publication Title":measur OR "Abstract":metric* OR "Abstract":measur* OR "IEEE Terms":metric* OR "IEEE Terms":measur* OR "Author Keywords":metric* OR "Author Keywords":measur*)) AND ("Publication Title":QoS OR "Publication Title":"quality of service" OR "Publication Title":"quality model" OR "Publication Title":"evaluation model" OR "Publication Title":"assessment model" OR "Publication Title":"quality in cloud" OR "Publication Title":"quality of cloud" OR "Abstract":QoS OR "Abstract":"quality of service" OR "Abstract":"quality model" OR "Abstract":"evaluation model" OR "Abstract":"assessment model" OR "Abstract":"quality in cloud" OR "Abstract":"quality of cloud" OR "IEEE Terms":QoS OR "IEEE Terms":"quality of service" OR "IEEE Terms":"quality model" OR "IEEE Terms":"evaluation model" OR "IEEE Terms":"assessment model" OR "IEEE Terms":"quality in cloud" OR "IEEE Terms":"quality of cloud" OR "Author Keywords":QoS OR "Author Keywords":"quality of service" OR "Author Keywords":"quality model" OR "Author Keywords":"evaluation model" OR "Author Keywords":"assessment model" OR "Author Keywords":"quality in cloud" OR "Author Keywords":"quality of cloud") AND ("Publication Title":cloud OR "Abstract":cloud OR "IEEE Terms":cloud OR "Author Keywords":cloud))|Title, abstract and keywords|Content Type: Conference Publications and Journals & Magazines. Year: 2006-2018
ACM Digital Library|(Title:((attribute OR characteristic) OR (metric* OR measur*)) OR Abstract:((attribute OR characteristic) OR (metric* OR measur*))  OR Keyword:((attribute OR characteristic) OR (metric* OR measur*))) AND (Title:(QoS "quality of service" "quality model" "evaluation model" "assessment model" "quality in cloud" "quality of cloud") OR Abstract:(QoS "quality of service" "quality model" "evaluation model" "assessment model" "quality in cloud" "quality of cloud") OR Keyword:(QoS "quality of service" "quality model" "evaluation model" "assessment model" "quality in cloud" "quality of cloud")) AND (Title:(cloud) OR Abstract:(cloud) OR Keyword:(cloud))|Title, abstract and keywords |Published since: 2006
ScienceDirect|TITLE-ABSTR-KEY(cloud ((attribute OR characteristic) OR (metric OR measur)) AND (QoS OR "quality of service" OR "quality model" OR "evaluation model" OR "assessment model" OR "quality in cloud" OR "quality of cloud")) |Title, abstract and keywords|Pub-date > 2005. Content type: Journal.
SpringerLink| cloud* AND (attribute* OR characteristic* OR measur* OR metric*) AND (QoS OR "quality of service" OR "quality model" OR "evaluation model" OR "assessment model" OR "quality in cloud" OR "quality of cloud")|Full text 	|Content Type: Article. Discipline: Computer Science Language: English.

### Conducting
### 1.3. Primary Studies {#estudios}
In this subsection, we present the list of papers selected. 

Code | Primary Studies 
------------ | ------------- 
S01 | Abd, S. K., Al-Haddad, S. A. R., Hashim, F., Abdullah, A. B. H. J., & Yussof, S. (2017). An effective approach for managing power consumption in cloud computing infrastructure. Journal of Computational Science, 21, 349–360. https://doi.org/https://doi.org/10.1016/j.jocs.2016.11.007
S02 | Abdeladim, A., Baina, S., & Baina, K. (2014). Elasticity and scalability centric quality model for the cloud. In 2014 Third IEEE International Colloquium in Information Science and Technology (CIST) (pp. 135–140). http://doi.org/10.1109/CIST.2014.7016607
S03 | Abrahão, S., & Insfran, E. (2017). Models@runtime for Monitoring Cloud Services in Google App Engine. In 2017 IEEE World Congress on Services (SERVICES) (pp. 30–35). https://doi.org/10.1109/SERVICES.2017.14
S04 | Alam, A. F. B., Soltanian, A., Yangui, S., Salahuddin, M. A., Glitho, R., & Elbiaze, H. (2016). A Cloud Platform-as-a-Service for multimedia conferencing service provisioning. In 2016 IEEE Symposium on Computers and Communication (ISCC) (pp. 289–294). https://doi.org/10.1109/ISCC.2016.7543756
S05 | Al-Jawad, A., Trestian, R., Shah, P., & Gemikonakli, O. (2015). BaProbSDN: A probabilistic-based QoS routing mechanism for Software Defined Networks. In Network Softwarization (NetSoft), 2015 1st IEEE Conference on (pp. 1–5). http://doi.org/10.1109/NETSOFT.2015.7116128
S06 | de Oliveira Jr., F. A., & Ledoux, T. (2011). Self-management of Applications QoS for Energy Optimization in Datacenters. In Green Computing Middleware on Proceedings of the 2Nd International Workshop (pp. 3:1–3:6). New York, NY, USA: ACM. doi:10.1145/2088996.2088999
S07 | Arumugam, K., & Sumathi, P. (2017). Secure and QoS guaranteed selection resource for storing health care information of cloud users. In 2017 International Conference on Computing Methodologies and Communication (ICCMC) (pp. 1165–1170). https://doi.org/10.1109/ICCMC.2017.8282657
S08 | Bao, D., Xiao, Z., Sun, Y., & Zhao, J. (2010). A method and framework for quality of cloud services measurement. In 2010 3rd International Conference on Advanced Computer Theory and Engineering(ICACTE) (Vol. 5, pp. V5–358–V5–362). http://doi.org/10.1109/ICACTE.2010.5579535
S09 | Baranwal, G., & Vidyarthi, D. P. (2014). A framework for selection of best cloud service provider using ranked voting method. In Advance Computing Conference (IACC), 2014 IEEE International (pp. 831–837). http://doi.org/10.1109/IAdCC.2014.6779430
S10 | Baranwal, G., & Vidyarthi, D. P. (2016). A cloud service selection model using improved ranked voting method. Concurrency and Computation: Practice and Experience, 28(13), 3540–3567. https://doi.org/10.1002/cpe.3740
S11 | Barba-Jimenez, C., Ramirez-Velarde, R., Tchernykh, A., Rodríguez-Dagnino, R., Nolazco-Flores, J., & Perez-Cazares, R. (2016). Cloud based Video-on-Demand service model ensuring quality of service and scalability. Journal of Network and Computer Applications, 70, 102–113. https://doi.org/10.1016/j.jnca.2016.05.007
S12 | Bardhan, S., & Milojicic, D. (2012). A Mechanism to Measure Quality-of-service in a Federated Cloud Environment. In Proceedings of the 2012 Workshop on Cloud Services, Federation, and the 8th Open Cirrus Summit (pp. 19–24). New York, NY, USA: ACM. doi:10.1145/2378975.2378981
S13 | Bousselmi, K., Brahmi, Z., & Gammoudi, M. M. (2016). QoS-Aware Scheduling of Workflows in Cloud Computing Environments. In 2016 IEEE 30th International Conference on Advanced Information Networking and Applications (AINA) (pp. 737–745). http://doi.org/10.1109/AINA.2016.72
S14 | Bruneo, D. (2014). A Stochastic Model to Investigate Data Center Performance and QoS in IaaS Cloud Computing Systems. IEEE Transactions on Parallel and Distributed Systems, 25(3), 560–569. http://doi.org/10.1109/TPDS.2013.67
S15 | Cedillo, P., Jimenez-Gomez, J., Abrahao, S., & Insfran, E. (2015). Towards a Monitoring Middleware for Cloud Services. In Services Computing (SCC), 2015 IEEE International Conference on (pp. 451–458). http://doi.org/10.1109/SCC.2015.68
S16 | Cervino, J., Rodriguez, P., Trajkovska, I., Mozo, A., & Salvachua, J. (2011). Testing a Cloud Provider Network for Hybrid P2P and Cloud Streaming Architectures. In Cloud Computing (CLOUD), 2011 IEEE International Conference on (pp. 356–363). http://doi.org/10.1109/CLOUD.2011.52
S17 | Costa, C. M., Leite, C. R. M., & Sousa, A. L. (2015). Service Response Time Measurement Model of Service Level Agreements in Cloud Environment. In 2015 IEEE International Conference on Smart City/SocialCom/SustainCom (SmartCity) (pp. 969–974). http://doi.org/10.1109/SmartCity.2015.196
S18 | de Assunção, M. D., Cardonha, C. H., Netto, M. A. S., & Cunha, R. L. F. (2016). Impact of user patience on auto-scaling resource capacity for cloud services. Future Generation Computer Systems, 55, 41–50. http://doi.org/http://dx.doi.org/10.1016/j.future.2015.09.001
S19 | Dou, W., Xu, X., Meng, S., & Yu, S. (2015). An Energy-Aware QoS Enhanced Method for Service Computing across Clouds and Data Centers. In 2015 Third International Conference on Advanced Cloud and Big Data (pp. 80–87). http://doi.org/10.1109/CBD.2015.23
S20 | Duggan, J., Cetintemel, U., Papaemmanouil, O., & Upfal, E. (2011). Performance Prediction for Concurrent Database Workloads. In Proceedings of the 2011 ACM SIGMOD International Conference on Management of Data (pp. 337–348). New York, NY, USA: ACM. doi:10.1145/1989323.1989359
S21 | Ezenwoke, A., Daramola, O., & Adigun, M. (2018). QoS-based ranking and selection of SaaS applications using heterogeneous similarity metrics. Journal of Cloud Computing, 7(1), 15. https://doi.org/10.1186/s13677-018-0117-4
S22 | Faragardi, H. R., Shojaee, R., Tabani, H., & Rajabi, A. (2013). An analytical model to evaluate reliability of cloud computing systems in the presence of QoS requirements. In Computer and Information Science (ICIS), 2013 IEEE/ACIS 12th International Conference on (pp. 315–321). http://doi.org/10.1109/ICIS.2013.6607860
S23 | Garcia-Pineda, M., Segura-Garcia, J., & Felici-Castell, S. (2018). Estimation techniques to measure subjective quality on live video streaming in Cloud Mobile Media services. Computer Communications, 118, 27–39. https://doi.org/10.1016/j.comcom.2017.08.009
S24 | Garg, S. K., Versteeg, S., & Buyya, R. (2013). A framework for ranking of cloud computing services. Future Generation Computer Systems, 29(4), 1012–1023. http://doi.org/http://dx.doi.org/10.1016/j.future.2012.06.006
S25 | Ghafari, S. M., Fazeli, M., Patooghy, A., & Rikhtechi, L. (2013). Bee-MMT: A load balancing method for power consumption management in cloud computing. In Contemporary Computing (IC3), 2013 Sixth International Conference on (pp. 76–80). http://doi.org/10.1109/IC3.2013.6612165
S26 | Ghahramani, M. H., Zhou, M., & Hon, C. T. (2017). Toward cloud computing QoS architecture: analysis of cloud systems and cloud services. IEEE/CAA Journal of Automatica Sinica, 4(1), 6–18. https://doi.org/10.1109/JAS.2017.7510313
S27 | Gholami, A., & Arani, M. G. (2015). A trust model for resource selection in cloud computing environment. In 2015 2nd International Conference on Knowledge-Based Engineering and Innovation (KBEI) (pp. 144–151). http://doi.org/10.1109/KBEI.2015.7436036
S28 | Ghosh, R., Longo, F., Naik, V. K., & Trivedi, K. S. (2010). Quantifying Resiliency of IaaS Cloud. In Reliable Distributed Systems, 2010 29th IEEE Symposium on (pp. 343–347). http://doi.org/10.1109/SRDS.2010.49
S29 | Gonzales, D., Kaplan, J. M., Saltzman, E., Winkelman, Z., & Woods, D. (2017). Cloud-Trust—a Security Assessment Model for Infrastructure as a Service (IaaS) Clouds. IEEE Transactions on Cloud Computing, 5(3), 523–536. https://doi.org/10.1109/TCC.2015.2415794
S30 | Guérout, T., Medjiah, S., Costa, G. Da, & Monteil, T. (2014). Quality of service modeling for green scheduling in Clouds. Sustainable Computing: Informatics and Systems, 4(4), 225–240. http://doi.org/http://dx.doi.org/10.1016/j.suscom.2014.08.006
S31 | Hasan, M. S., Alvares, F., Ledoux, T., & Pazat, J. (2017). Investigating Energy Consumption and Performance Trade-Off for Interactive Cloud Application. IEEE Transactions on Sustainable Computing, 2(2), 113–126. https://doi.org/10.1109/TSUSC.2017.2714959
S32 | Hassam, M., Kara, N., Belqasmi, F., & Glitho, R. (2014). Virtualized Infrastructure for Video Game Applications in Cloud Environments. In Proceedings of the 12th ACM International Symposium on Mobility Management and Wireless Access (pp. 109–114). New York, NY, USA: ACM. doi:10.1145/2642668.2642679
S33 | Hecht, G., Jose-Scheidt, B., Figueiredo, C. D., Moha, N., & Khomh, F. (2014). An Empirical Study of the Impact of Cloud Patterns on Quality of Service (QoS). In Cloud Computing Technology and Science (CloudCom), 2014 IEEE 6th International Conference on (pp. 278–283). http://doi.org/10.1109/CloudCom.2014.141
S34 | Heidari, P., Boucheneb, H., & Shami, A. (2015). A Formal Approach for QoS Assurance in the Cloud. In 2015 IEEE 7th International Conference on Cloud Computing Technology and Science (CloudCom) (pp. 629–634). http://doi.org/10.1109/CloudCom.2015.36
S35 | Hu, Y., Deng, B., Yang, Y., & Wang, D. (2017). Elasticity evaluation of IaaS cloud based on mixed workloads. In Proceedings - 15th International Symposium on Parallel and Distributed Computing, ISPDC 2016 (pp. 157–164). Beijing Institute of System Engineering, Beijing, China. https://doi.org/10.1109/ISPDC.2016.28
S36 | Hwang, K., Bai, X., Shi, Y., Li, M., Chen, W.-G., & Wu, Y. (2016). Cloud Performance Modeling with Benchmark Evaluation of Elastic Scaling Strategies. IEEE Transactions on Parallel and Distributed Systems, 27(1), 130–143. https://doi.org/10.1109/TPDS.2015.2398438
S37 | Ibrahim, A. A. Z. A., Wasim, M. U., Varrette, S., & Bouvry, P. (2018). PRESEnCE: Performance Metrics Models for Cloud SaaS Web Services. In 2018 IEEE 11th International Conference on Cloud Computing (CLOUD) (pp. 936–940). https://doi.org/10.1109/CLOUD.2018.00140
S38 | Joy, N., Chandrasekaran, K., & Binu, A. (2015). A study on energy efficient cloud computing. In 2015 IEEE International Conference on Computational Intelligence and Computing Research (ICCIC) (pp. 1–6). http://doi.org/10.1109/ICCIC.2015.7435661
S39 | Kaaniche, N., Mohamed, M., Laurent, M., & Ludwig, H. (2017). Security SLA Based Monitoring in Clouds. In 2017 IEEE International Conference on Edge Computing (EDGE) (pp. 90–97). https://doi.org/10.1109/IEEE.EDGE.2017.20
S40 | Karim, R., Ding, C., & Miri, A. (2015). End-to-End Performance Prediction for Selecting Cloud Services Solutions. In Service-Oriented System Engineering (SOSE), 2015 IEEE Symposium on (pp. 69–77). http://doi.org/10.1109/SOSE.2015.11
S41 | Katsaros, G., Subirats, J., Fitó, J. O., Guitart, J., Gilet, P., & Espling, D. (2013). A service framework for energy-aware monitoring and VM management in Clouds. Future Generation Computer Systems, 29(8), 2077–2091. http://doi.org/http://dx.doi.org/10.1016/j.future.2012.12.006
S42 | Kaur, P. D., & Chana, I. (2014). A resource elasticity framework for QoS-aware execution of cloud applications. Future Generation Computer Systems, 37, 14–25. http://doi.org/http://dx.doi.org/10.1016/j.future.2014.02.018
S43 | Kirsal, Y., Ever, Y. K., Mostarda, L., & Gemikonakli, O. (2015). Analytical Modelling and Performability Analysis for Cloud Computing Using Queuing System. In 2015 IEEE/ACM 8th International Conference on Utility and Cloud Computing (UCC) (pp. 643–647). http://doi.org/10.1109/UCC.2015.115
S44 | Lee, J. Y., Lee, J. W., Cheun, D. W., & Kim, S. D. (2009). A Quality Model for Evaluating Software-as-a-Service in Cloud Computing. In Software Engineering Research, Management and Applications, 2009. SERA ’09. 7th ACIS International Conference on (pp. 261–266). http://doi.org/10.1109/SERA.2009.43
S45 | Lim, E., & Thiran, P. (2014). Communication of Technical QoS among Cloud Brokers. In Cloud Engineering (IC2E), 2014 IEEE International Conference on (pp. 403–409). http://doi.org/10.1109/IC2E.2014.92
S46 | Lin, Y.-K., & Chang, P.-C. (2011). Maintenance reliability estimation for a cloud computing network with nodes failure. Expert Systems with Applications, 38(11), 14185–14189. http://doi.org/http://dx.doi.org/10.1016/j.eswa.2011.04.230
S47 | Liu, M., Dou, W., Yu, S., & Zhang, Z. (2014). A clusterized firewall framework for cloud computing. In 2014 IEEE International Conference on Communications (ICC) (pp. 3788–3793). http://doi.org/10.1109/ICC.2014.6883911
S48 | Liu, X., Xia, C., Wang, T., & Zhong, L. (2017). CloudSec: A Novel Approach to Verifying Security Conformance at the Bottom of the Cloud. In 2017 IEEE International Congress on Big Data (BigData Congress) (pp. 569–576). https://doi.org/10.1109/BigDataCongress.2017.87
S49 | Lu, L., & Yuan, Y. (2018). A novel TOPSIS evaluation scheme for cloud service trustworthiness combining objective and subjective aspects. Journal of Systems and Software, 143, 71–86. https://doi.org/10.1016/j.jss.2018.05.004
S50 | Manuel, P. (2015). A trust model of cloud computing based on Quality of Service. Annals of Operations Research, 233(1), 281–292. http://doi.org/10.1007/s10479-013-1380-x
S51 | Mastelic, T., Brandic, I., & Jaarevic, J. (2014). CPU Performance Coefficient (CPU-PC): A Novel Performance Metric Based on Real-Time CPU Resource Provisioning in Time-Shared Cloud Environments. In Cloud Computing Technology and Science (CloudCom), 2014 IEEE 6th International Conference on (pp. 408–415). http://doi.org/10.1109/CloudCom.2014.13
S52 | Mesbahi, M. R., Rahmani, A. M., & Hosseinzadeh, M. (2018). Reliability and high availability in cloud computing environments: a reference roadmap. Human-Centric Computing and Information Sciences, 8(1), 20. https://doi.org/10.1186/s13673-018-0143-8
S53 | Nadanam, P., & Rajmohan, R. (2012). QoS evaluation for web services in cloud computing. In Computing Communication Networking Technologies (ICCCNT), 2012 Third International Conference on (pp. 1–8). http://doi.org/10.1109/ICCCNT.2012.6395991
S54 | Pedersen, J. M., Riaz, M. T., Junior, J. C., Dubalski, B., Ledzinski, D., & Patel, A. (2011). Assessing Measurements of QoS for Global Cloud Computing Services. In Dependable, Autonomic and Secure Computing (DASC), 2011 IEEE Ninth International Conference on (pp. 682–689). http://doi.org/10.1109/DASC.2011.120
S55 | Preuveneers, D., Heyman, T., Berbers, Y., & Joosen, W. (2016). Systematic scalability assessment for feature oriented multi-tenant services. Journal of Systems and Software, 116, 162–176. https://doi.org/10.1016/j.jss.2015.12.024
S56 | Qian, S., Cao, J., Le Mouël, F., Li, M., & Wang, J. (2015). Towards Prioritized Event Matching in a Content-based Publish/Subscribe System. In Proceedings of the 9th ACM International Conference on Distributed Event-Based Systems (pp. 116–127). New York, NY, USA: ACM. doi:10.1145/2675743.2771823
S57 | Ran, Y., Shi, Y., Yang, E., Chen, S., & Yang, J. (2014). Dynamic resource allocation for video transcoding with QoS guaranteeing in cloud-based DASH system. In 2014 IEEE Globecom Workshops (GC Wkshps) (pp. 144–149). http://doi.org/10.1109/GLOCOMW.2014.7063421
S58 | Ravindhren, V. G., & Ravimaran, S. (2017). CCMA—cloud critical metric assessment framework for scientific computing. Cluster Computing. https://doi.org/10.1007/s10586-017-1384-4
S59 | Ravindran, K. (2013). Self-Assessment and Reconfiguration Methods for Autonomous Cloud-based Network Systems. In Distributed Simulation and Real Time Applications (DS-RT), 2013 IEEE/ACM 17th International Symposium on (pp. 87–94). http://doi.org/10.1109/DS-RT.2013.37
S60 | Rizvi, S., Ryoo, J., Kissell, J., & Aiken, B. (2015). A Stakeholder-oriented Assessment Index for Cloud Security Auditing. In Proceedings of the 9th International Conference on Ubiquitous Information Management and Communication (pp. 55:1–55:7). New York, NY, USA: ACM. doi:10.1145/2701126.2701226
S61 | Rizvi, S., Roddy, H., Gualdoni, J., & Myzyri, I. (2017). Three-Step Approach to QoS Maintenance in Cloud Computing Using a Third-Party Auditor. Procedia Computer Science, 114, 83–92. https://doi.org/10.1016/j.procs.2017.09.014
S62 | Roohitavaf, M., Entezari-Maleki, R., & Movaghar, A. (2013). Availability Modeling and Evaluation of Cloud Virtual Data Centers. In Parallel and Distributed Systems (ICPADS), 2013 International Conference on (pp. 675–680). http://doi.org/10.1109/ICPADS.2013.120
S63 | Saiz, E., Ibarrola, E., Cristobo, L., & Taboada, I. (2014). A cloud platform for QoE evaluation: QoXcloud. In ITU Kaleidoscope Academic Conference: Living in a converged world - Impossible without standards?, Proceedings of the 2014 (pp. 241–247). http://doi.org/10.1109/Kaleidoscope.2014.6858471
S64 | Samet, N., Letaïfa, A. Ben, Hamdi, M., & Tabbane, S. (2016). Real-Time User Experience Evaluation for Cloud-Based Mobile Video. In 2016 30th International Conference on Advanced Information Networking and Applications Workshops (WAINA) (pp. 204–208). http://doi.org/10.1109/WAINA.2016.120
S65 | Singh, S., & Chana, I. (2015). Q-aware: Quality of service based cloud resource provisioning. Computers & Electrical Engineering, 47, 138–160. http://doi.org/http://dx.doi.org/10.1016/j.compeleceng.2015.02.003
S66 | Slivar, I., Skorin-Kapov, L., & Suznjevic, M. (2016). Cloud Gaming QoE Models for Deriving Video Encoding Adaptation Strategies. In Proceedings of the 7th International Conference on Multimedia Systems (pp. 18:1–18:12). New York, NY, USA: ACM. doi:10.1145/2910017.2910602
S67 | Son, S., & Sim, K. M. (2015). Adaptive and similarity-based tradeoff algorithms in a price-timeslot-QoS negotiation system to establish cloud SLAs. Information Systems Frontiers, 17(3), 565–589. http://doi.org/10.1007/s10796-013-9432-y
S68 | Sousa, F. R. C., & Machado, J. C. (2012). Towards Elastic Multi-Tenant Database Replication with Quality of Service. In Utility and Cloud Computing (UCC), 2012 IEEE Fifth International Conference on (pp. 168–175). http://doi.org/10.1109/UCC.2012.36
S69 | Souza, R. H. de, Flores, P. A., Dantas, M. A. R., & Siqueira, F. (2016). Architectural recovering model for Distributed Databases: A reliability, availability and serviceability approach. In 2016 IEEE Symposium on Computers and Communication (ISCC) (pp. 575–580). https://doi.org/10.1109/ISCC.2016.7543799
S70 | Taherizadeh, S., & Stankovski, V. (2017). Incremental Learning from Multi-level Monitoring Data and Its Application to Component Based Software Engineering. In 2017 IEEE 41st Annual Computer Software and Applications Conference (COMPSAC) (Vol. 2, pp. 378–383). https://doi.org/10.1109/COMPSAC.2017.148
S71 | Vedam, V., & Vemulapati, J. (2012). Demystifying Cloud Benchmarking Paradigm - An in Depth View. In 2012 IEEE 36th Annual Computer Software and Applications Conference (pp. 416–421). http://doi.org/10.1109/COMPSAC.2012.61
S72 | Wagle, S. S., Guzek, M., Bouvry, P., & Bisdorff, R. (2015). An Evaluation Model for Selecting Cloud Services from Commercially Available Cloud Providers. In 2015 IEEE 7th International Conference on Cloud Computing Technology and Science (CloudCom) (pp. 107–114). http://doi.org/10.1109/CloudCom.2015.94
S73 | Wang, S., & Dey, S. (2012). Cloud Mobile Gaming: Modeling and Measuring User Experience in Mobile Wireless Networks. SIGMOBILE Mob. Comput. Commun. Rev., 16(1), 10–21. doi:10.1145/2331675.2331679
S74 | Wen, Z. Y., & Hsiao, H. F. (2014). QoE-driven performance analysis of cloud gaming services. In Multimedia Signal Processing (MMSP), 2014 IEEE 16th International Workshop on (pp. 1–6). http://doi.org/10.1109/MMSP.2014.6958835
S75 | Wu, X., Liu, G., & Xu, J. (2015). A QoS-constrained scheduling for access requests in cloud storage. In Industrial Electronics and Applications (ICIEA), 2015 IEEE 10th Conference on (pp. 155–160). http://doi.org/10.1109/ICIEA.2015.7334102
S76 | Xia, Y., Zhou, M., Luo, X., Zhu, Q., Li, J., & Huang, Y. (2015). Stochastic Modeling and Quality Evaluation of Infrastructure-as-a-Service Clouds. IEEE Transactions on Automation Science and Engineering, 12(1), 162–170. http://doi.org/10.1109/TASE.2013.2276477
S77 | Xiao, Y., Lin, C., Jiang, Y., Chu, X., & Shen, X. (2010). Reputation-Based QoS Provisioning in Cloud Computing via Dirichlet Multinomial Model. In Communications (ICC), 2010 IEEE International Conference on (pp. 1–5). http://doi.org/10.1109/ICC.2010.5502407
S78 | Xiong, K., & Chen, X. (2015). Ensuring Cloud Service Guarantees via Service Level Agreement (SLA)-Based Resource Allocation. In 2015 IEEE 35th International Conference on Distributed Computing Systems Workshops (pp. 35–41). http://doi.org/10.1109/ICDCSW.2015.18
S79 | Xu, H., Qiu, X., Sheng, Y., Luo, L., & Xiang, Y. (2018). A Qos-Driven Approach to the Cloud Service Addressing Attributes of Security. IEEE Access, 6, 34477–34487. https://doi.org/10.1109/ACCESS.2018.2849594
S80 | Yu, N., Gu, F., Guo, X., & He, Z. (2015). A Fine-grained Flow Control Model for Cloud-assisted Data Broadcasting. In Proceedings of the 18th Symposium on Communications {&} Networking (pp. 24–31). San Diego, CA, USA: Society for Computer Simulation International. Retrieved from http://dl.acm.org/citation.cfm?id=2872550.2872554
S81 | Zant, B. El, & Gagnaire, M. (2015). Towards a unified customer aware figure of merit for CSP selection. Journal of Cloud Computing, 4(1), 1–23. http://doi.org/10.1186/s13677-015-0049-1
S82 | Zheng, X., Martin, P., & Brohman, K. (2013). Cloud Service Negotiation: A Research Roadmap. In Services Computing (SCC), 2013 IEEE International Conference on (pp. 627–634). http://doi.org/10.1109/SCC.2013.93
S83 | Zheng, X., Martin, P., Brohman, K., & Xu, L. D. (2014). CLOUDQUAL: A Quality Model for Cloud Services. IEEE Transactions on Industrial Informatics, 10(2), 1527–1536. http://doi.org/10.1109/TII.2014.2306329
S84 | Zhou, P., Wang, Z., Li, W., & Jiang, N. (2015). Quality Model of Cloud Service. In High Performance Computing and Communications (HPCC), 2015 IEEE 7th International Symposium on Cyberspace Safety and Security (CSS), 2015 IEEE 12th International Conferen on Embedded Software and Systems (ICESS), 2015 IEEE 17th International Conference on (pp. 1418–1423). http://doi.org/10.1109/HPCC-CSS-ICESS.2015.134
S85 | Feng, J., & Kong, L. (2015). A Fuzzy Multi-objective Genetic Algorithm for QoS-based Cloud Service Composition. In 2015 11th International Conference on Semantics, Knowledge and Grids (SKG) (pp. 202–206). http://doi.org/10.1109/SKG.2015.23
S86 | Khan, H. M., Chan, G. Y., & Chua, F. F. (2016). An adaptive monitoring framework for ensuring accountability and quality of services in cloud computing. In 2016 International Conference on Information Networking (ICOIN) (pp. 249–253). http://doi.org/10.1109/ICOIN.2016.7427071
S87 | Khurana, R., & Bawa, R. K. (2016). QoS based Cloud Service Selection paradigms. In 2016 6th International Conference - Cloud System and Big Data Engineering (Confluence) (pp. 174–179). https://doi.org/10.1109/CONFLUENCE.2016.7508109
S88 | Klymash, M., Beshley, M., Strykhalyuk, B., & Maksymyuk, T. (2014). Research and development the methods of quality of service provision in Mobile Cloud systems. In Communications and Networking (BlackSeaCom), 2014 IEEE International Black Sea Conference on (pp. 160–164). http://doi.org/10.1109/BlackSeaCom.2014.6849030

### 1.4. Evaluación de la calidad {#qa}
Para evaluar la calidad de los estudios, diseñamos las siguientes preguntas de calidad.

**QUALITY QUESTIONS** |
------------ |
Q1. (Motivation) Is the research problem clearly specified? |
Q2. (Aim)Are the research aim(s)/objective(s) clearly established? |
Q3. (Context) Is the context of the study clearly specified? |
Q4. (Data) Are the metrics for assessing the quality of cloud services clearly defined? |
Q5. (Data) Are the measurement functions for calculating the metrics clearly defined? |
Q6. (Design) Are the metric(s) empirically validated? | 
Q7. (Usefulness) Is there enough evidence that shows how the metrics can be used in practice? |
Q8. (Contributions/results) Are the contributions/results of the paper discussed? |
Q9. (Insights) Are the insights/lessons learned of the study reported? |
Q10. (Limitations) Are the limitations of the study discussed? |


**QUALITY ASSESSMENT**

The primary studies' quality was scored based on how well they satisfied the ten quality questions.  Be clear that we do not evaluate the quality of the paper itself with these criteria, but only its contributions’ alignment with our research questions. Then the scores less than five were removed (S85,S86, S87,S88).

Code | Q1 | Q2 | Q3 | Q4 | Q5 | Q6 | Q7 | Q8 | Q9 | Q10 | Total

--- | ----- | ---------| ------- | --------- | -------- | ---------- | ------- | -------- | --------- | -------
S01 | Y | P | Y | Y | Y | P | Y | Y | N | N | 7
S02 | Y | P | Y | Y | Y | P | Y | Y | P | P | 8
S03 | Y | P | Y | Y | Y | Y | Y | Y | N | P | 8
S04 | Y | Y | Y | Y | Y | P | Y | P | N | N | 7
S05 | P | P | P | Y | Y | P | N | Y | N | N | 5
S06 | Y | Y | N | P | P | P | Y | Y | N | Y | 6,5
S07 | Y | P | P | Y | Y | P | N | P | N | N | 5
S08 | P | P | Y | Y | Y | P | N | P | N | N | 5
S09 | P | Y | Y | Y | Y | N | P | N | N | N | 5
S10 | P | Y | Y | Y | Y | N | Y | Y | N | N | 6,5
S11 | P | Y | Y | Y | Y | P | Y | Y | N | N | 7
S12 | Y | Y | Y | Y | Y | P | Y | Y | P | N | 8
S13 | Y | Y | P | Y | Y | P | Y | Y | N | N | 7
S14 | Y | Y | P | Y | Y | P | N | Y | P | N | 6,5
S15 | Y | Y | Y | Y | Y | N | Y | P | P | N | 7
S16 | Y | Y | Y | Y | Y | N | Y | Y | P | N | 7,5
S17 | P | P | P | Y | Y | P | Y | P | N | N | 5,5
S18 | Y | Y | P | Y | Y | P | P | Y | P | N | 7
S19 | P | Y | Y | Y | Y | P | P | Y | P | N | 7
S20 | Y | Y | Y | Y | Y | P | Y | Y | N | Y | 8,5
S21 | Y | N | Y | Y | Y | P | N | Y | P | N | 6
S22 | Y | Y | Y | P | P | N | P | P | P | Y | 6,5
S23 | P | P | Y | Y | Y | Y | N | Y | N | N | 6
S24 | Y | Y | Y | Y | Y | N | Y | Y | P | P | 8
S25 | P | P | Y | Y | Y | P | N | Y | N | N | 5,5
S26 | Y | P | Y | Y | Y | N | N | Y | Y | N | 6,5
S27 | Y | P | Y | Y | Y | P | N | Y | P | N | 6,5
S28 | Y | P | Y | Y | Y | P | N | P | N | N | 5,5
S29 | Y | Y | Y | P | P | P | P | Y | Y | Y | 8
S30 | Y | P | Y | Y | Y | P | P | Y | Y | N | 7,5
S31 | P | P | Y | Y | Y | P | N | Y | N | Y | 6,5
S32 | P | P | Y | Y | Y | N | N | Y | N | N | 5
S33 | P | P | Y | P | P | Y | N | Y | P | N | 5,5
S34 | P | Y | Y | Y | Y | N | N | P | P | N | 5,5
S35 | P | P | Y | Y | Y | P | N | Y | N | N | 5,5
S36 | Y | P | Y | Y | Y | Y | Y | Y | Y | N | 8,5
S37 | P | P | Y | Y | Y | P | N | Y | P | N | 6
S38 | Y | N | Y | Y | Y | N | N | Y | N | N | 5
S39 | Y | N | Y | P | P | P | P | Y | N | N | 5
S40 | Y | P | Y | Y | Y | N | N | Y | N | N | 5,5
S41 | Y | P | Y | Y | Y | P | N | Y | N | N | 6
S42 | Y | P | Y | Y | Y | N | P | Y | N | N | 6
S43 | P | P | Y | P | P | P | P | Y | N | N | 5
S44 | Y | P | Y | Y | Y | N | P | Y | N | N | 6
S45 | P | P | Y | Y | Y | N | N | Y | N | N | 5
S46 | Y | N | Y | Y | Y | P | P | P | N | N | 5,5
S47 | Y | N | Y | Y | Y | P | P | Y | N | N | 6
S48 | Y | Y | Y | Y | Y | P | N | P | N | N | 6
S49 | Y | Y | Y | Y | Y | Y | N | P | N | N | 6,5
S50 | P | Y | Y | Y | Y | N | P | N | N | N | 5
S51 | Y | N | Y | Y | Y | P | P | Y | N | N | 6
S52 | Y | P | Y | Y | Y | N | N | Y | Y | P | 7
S53 | Y | N | Y | Y | Y | N | N | Y | N | N | 5
S54 | P | P | Y | Y | Y | N | N | Y | P | N | 5,5
S55 | Y | P | Y | P | P | P | Y | Y | Y | N | 7
S56 | Y | N | Y | Y | Y | P | N | Y | Y | P | 7
S57 | Y | N | Y | Y | Y | N | N | Y | N | N | 5
S58 | P | N | Y | Y | Y | P | N | Y | P | N | 5,5
S59 | Y | Y | Y | P | P | N | P | Y | N | N | 5,5
S60 | Y | N | Y | Y | Y | P | N | Y | N | N | 5,5
S61 | Y | P | Y | Y | Y | N | N | P | N | N | 5
S62 | Y | N | Y | Y | Y | N | N | Y | N | P | 5,5
S63 | Y | Y | Y | P | P | N | N | Y | N | N | 5
S64 | Y | P | Y | Y | Y | N | N | P | N | N | 5
S65 | P | N | Y | Y | Y | P | Y | Y | Y | N | 7
S66 | P | N | Y | Y | Y | P | N | Y | P | P | 6
S67 | P | Y | Y | P | P | N | N | Y | Y | N | 5,5
S68 | Y | N | Y | Y | Y | N | N | Y | P | N | 5,5
S69 | P | Y | P | Y | Y | N | P | P | N | N | 5
S70 | P | Y | P | Y | Y | P | N | P | N | N | 5
S71 | N | N | Y | Y | Y | N | P | P | Y | N | 5
S72 | P | Y | Y | Y | Y | N | N | Y | Y | N | 6,5
S73 | P | N | Y | Y | Y | P | Y | Y | Y | N | 7
S74 | P | N | Y | Y | Y | P | N | Y | P | N | 5,5
S75 | Y | N | Y | Y | Y | N | N | Y | P | N | 5,5
S76 | Y | N | Y | Y | Y | N | N | Y | Y | Y | 7
S77 | P | P | P | Y | Y | N | P | Y | N | N | 5
S78 | Y | P | Y | Y | Y | P | N | P | N | N | 5,5
S79 | Y | Y | Y | Y | Y | P | N | Y | Y | N | 7,5
S80 | Y | Y | Y | Y | Y | P | N | P | N | N | 6
S81 | Y | Y | Y | Y | Y | P | N | Y | N | N | 6,5
S82 | Y | Y | Y | Y | Y | N | N | Y | P | N | 6,5
S83 | P | Y | Y | Y | Y | Y | Y | Y | N | Y | 8,5
S84 | N | Y | Y | Y | Y | P | N | Y | N | N | 5,5
S85 | P | P | P | Y | Y | N | N | P | N | N | 4
S86 | P | N | Y | P | P | N | P | P | N | N | 3,5
S87 | P | N | P | Y | P | N | N | P | N | N | 3
S88 | P | P | Y | Y | Y | N | N | P | N | N | 4,5

Y: Fully compliance, P: Partially comply, N: Do not comply

**RELEVANCE OF PRIMARY STUDIES**

In order to know the impact and influence of the papers. We used two criteria: 

•	The relevance of the journal or conference where the paper was published (CORE-ERA ranking for conference papers and the impact factor in Journal Citations Reports(JCR) for journal papers).  
•	The number of citations of the paper, collected from Google Scholar . 

Code | Type conference /journal | Relevant publication | Citations | Year | Rate Citation Value | Library
------------ | -------------  | ------------- | ------------- | ------------- | ------------- | -------------
S01 | J | 10 | 12 | 2017 | 10 | ScienceDirect
S02 | C | 5 | 5 | 2014 | 0 | IEEE Xplore
S03 | C | 0 | 3 | 2017 | 10 | IEEE Xplore
S04 | C | 5 | 5 | 2016 | 0 | IEEE Xplore
S05 | C | 0 | 16 | 2015 | 5 | IEEE Xplore
S06 | C | 0 | 5 | 2011 | 0 | ACM
S07 | C | 0 | 0 | 2017 | 5 | IEEE Xplore
S08 | C | 0 | 11 | 2010 | 5 | IEEE Xplore
S09 | C | 0 | 40 | 2014 | 5 | IEEE Xplore
S10 | J | 10 | 21 | 2016 | 5 | ACM
S11 | J | 10 | 17 | 2016 | 5 | ScienceDirect
S12 | C | 0 | 12 | 2012 | 5 | ACM
S13 | C | 5 | 11 | 2016 | 5 | IEEE Xplore
S14 | J | 10 | 160 | 2014 | 10 | IEEE Xplore
S15 | C | 10 | 12 | 2015 | 5 | IEEE Xplore
S16 | C | 5 | 30 | 2011 | 5 | IEEE Xplore
S17 | C | 0 | 2 | 2015 | 0 | IEEE Xplore
S18 | J | 10 | 24 | 2013 | 5 | ScienceDirect
S19 | C | 0 | 1 | 2015 | 0 | IEEE Xplore
S20 | C | 10 | 134 | 2011 | 10 | ACM
S21 | J | 0 | 4 | 2018 | 10 | ACM
S22 | C | 5 | 20 | 2013 | 5 | IEEE Xplore
S23 | J | 10 | 1 | 2018 | 10 | ACM
S24 | J | 10 | 702 | 2013 | 10 | ScienceDirect
S25 | C | 0 | 39 | 2013 | 5 | IEEE Xplore
S26 | J | 0 | 63 | 2017 | 10 | IEEE Xplore
S27 | C | 0 | 3 | 2015 | 0 | IEEE Xplore
S28 | C | 10 | 53 | 2010 | 10 | IEEE Xplore
S29 | J | 10 | 70 | 2017 | 10 | IEEE Xplore
S30 | J | 10 | 24 | 2014 | 5 | ScienceDirect
S31 | J | 0 | 7 | 2017 | 10 | IEEE Xplore
S32 | C | 5 | 3 | 2014 | 0 | ACM
S33 | C | 5 | 8 | 2014 | 0 | IEEE Xplore
S34 | C | 5 | 0 | 2015 | 0 | IEEE Xplore
S35 | C | 0 | 2 | 2017 | 10 | IEEE Xplore
S36 | C | 0 | 83 | 2016 | 10 | IEEE Xplore
S37 | C | 5 | 0 | 2018 | 5 | IEEE Xplore
S38 | C | 0 | 1 | 2015 | 0 | IEEE Xplore
S39 | C | 0 | 7 | 2017 | 10 | IEEE Xplore
S40 | C | 0 | 7 | 2015 | 0 | IEEE Xplore
S41 | J | 10 | 50 | 2013 | 10 | ScienceDirect
S42 | J | 10 | 56 | 2014 | 10 | ScienceDirect
S43 | C | 0 | 3 | 2015 | 0 | IEEE Xplore
S44 | C | 5 | 138 | 2009 | 10 | IEEE Xplore
S45 | C | 0 | 4 | 2014 | 0 | IEEE Xplore
S46 | J | 0 | 47 | 2011 | 5 | ScienceDirect
S47 | C | 5 | 10 | 2014 | 5 | IEEE Xplore
S48 | C | 0 | 0 | 2017 | 5 | IEEE Xplore
S49 | J | 10 | 3 | 2018 | 10 | ScienceDirect
S50 | J | 0 | 122 | 2015 | 10 | SpringerLink
S51 | C | 5 | 3 | 2014 | 0 | IEEE Xplore
S52 | J | 10 | 10 | 2018 | 10 | SpringerLink
S53 | C | 0 | 21 | 2012 | 5 | IEEE Xplore
S54 | C | 5 | 26 | 2011 | 5 | IEEE Xplore
S55 | J | 10 | 6 | 2016 | 0 | ACM
S56 | C | 0 | 1 | 2015 | 0 | ACM
S57 | C | 0 | 5 | 2014 | 0 | IEEE Xplore
S58 | J | 10 | 2 | 2017 | 10 | SpringerLink
S59 | C | 5 | 2 | 2013 | 0 | IEEE Xplore
S60 | C | 0 | 6 | 2015 | 0 | ACM
S61 | J | 0 | 3 | 2017 | 10 | ACM
S62 | C | 5 | 5 | 2013 | 0 | IEEE Xplore
S63 | C | 0 | 3 | 2014 | 0 | IEEE Xplore
S64 | C | 0 | 3 | 2016 | 0 | IEEE Xplore
S65 | J | 10 | 67 | 2015 | 10 | ScienceDirect
S66 | C | 0 | 21 | 2016 | 5 | ACM
S67 | J | 10 | 18 | 2015 | 5 | SpringerLink
S68 | C | 0 | 33 | 2012 | 5 | IEEE Xplore
S69 | C | 5 | 2 | 2016 | 0 | IEEE Xplore
S70 | C | 5 | 3 | 2017 | 10 | IEEE Xplore
S71 | C | 5 | 10 | 2012 | 5 | IEEE Xplore
S72 | C | 5 | 24 | 2015 | 5 | IEEE Xplore
S73 | J | 0 | 57 | 2012 | 10 | ACM
S74 | C | 5 | 12 | 2014 | 5 | IEEE Xplore
S75 | C | 0 | 6 | 2015 | 0 | IEEE Xplore
S76 | J | 10 | 62 | 2015 | 10 | IEEE Xplore
S77 | C | 5 | 52 | 2010 | 10 | IEEE Xplore
S78 | C | 0 | 12 | 2015 | 5 | IEEE Xplore
S79 | J | 10 | 1 | 2018 | 10 | IEEE Xplore
S80 | C | 0 | 0 | 2015 | 0 | ACM
S81 | J | 0 | 4 | 2015 | 0 | JoCCASA
S82 | C | 10 | 14 | 2013 | 5 | IEEE Xplore
S83 | J | 10 | 80 | 2014 | 10 | IEEE Xplore
S84 | C | 5 | 4 | 2015 | 0 | IEEE Xplore
S85 | C | 5 | 6 | 2015 | 0 | IEEE Xplore
S86 | C | 5 | 8 | 2016 | 0 | IEEE Xplore
S87 | C | 0 | 2 | 2016 | 0 | IEEE Xplore
S88 | C | 0 | 24 | 2014 | 5 | IEEE Xplore

J: Journal, C: Conference

CORE-ERA http://portal.core.edu.au

JCR https://www.recursoscientificos.fecyt.es/factor/

### Reporting
### 1.5. Taxonomy of QoS metrics for cloud services {#clasificacion}
In this subsection, is shown the taxonomy of metrics for cloud services. The classification was done using the data extraction criteria. 

 <p> 1.<a href ="./images/modelo.png"> Taxonomy of quality metrics metamodel </a> <br> 
 2.<a href ="./images/taxonomy.png"> Taxonomy of quality metrics for cloud services summary</a> <br> 
 3.<a href ="./files/TaxonomyQualityMetrics.xlsx"> Taxonomy of quality metrics for cloud services </a> <br> 
</p>

NOTE: In order to visualize the reports, please enable de _Power Pivot_ and _Power View_ complements of Excel.

<a href ="https://support.office.com/en-us/article/Start-the-Power-Pivot-add-in-for-Excel-a891a66d-36e3-43fc-81e8-fc4798f39ea8"> How to enable Excel complements


## 2. Modelo de Calidad para servicios cloud {#qmodel}
Puede encontrar información relevante del capítulo **_Modelo de Calidad para Servicios Cloud_**.

### 2.1 Metamodelo del modelo de calidad (#metamodel)

The quality model proposes the ISO/IEC 25010 standard as the baseline extends and decomposes into sub-characteristics adjusted to the domain, determines objectively measurable attributes, and specifies metrics for the attributes. 

<a href ="./images/modelo.png"> Figure 1 </a> provides a clear and structured representation of the metamodel of the quality model and its metaclasses that describe the relationships among cloud domain and quality model concepts.

![Metamodel](./images/modelo.png "Figure 1")

 Figure 1. <a href ="./images/modelo.png"> Metamodel of the quality model </a> <br>
  <br> 

Defining metamodel main concepts:
- Characteristics are non-measurable aspects that are used in the quality model to categorize a high-level aspect that can be
evaluated.
- Subcharacteristics specify the aspects to be evaluated but are not objectively measurable and are broken down into quality
attributes. These are contained in the characteristic metaclass with the relationship to itself.
- Attributes are objectively measurable quality aspects (i.e., physical, abstract) that are not further decomposed and can be
measured using metrics.
- Metrics define a possible way to measure an attribute. It provides a measurement scale (i.e., nominal, ordinal, interval,
ratio, or absolute) combined with a measurement approach (i.e., measurement method or measurement function)
- Operationalization is the core of the metamodel, which establishes a mapping between the generic definition of a metric and the artifact or cloud platform where the metric is measured. 

### 2.2. Method {#method}

Our proposal is a quality model for cloud services that meets the conditions for a mixed approach and has been defined based on these two resources. 
On the one hand, the quality model proposed by the ISO/IEC 25010 standard, defines the system and software quality characteristics and subcharacteristics at a high level of abstraction. The issue with this standard is that it provides a generic model that needs to be adapted to the specific context or domain of cloud services. 

On the other hand, a taxonomy of metrics for evaluating cloud services was obtained through an SLR [3]. The process followed in the SLR contains three main phases: planning to define the review protocol, conducting to collect data, and reporting to communicate and report the results. In addition, the taxonomy creation
process detailed the activities with their artifacts, inputs, and outputs for each.
As a result, 243 attributes, 407 metrics, and 468 operationalizations were obtained.


<img src="./images/Figure2.png " alt="Figure 2" width="600px" align="center">


Figure 2. <a href ="./images/Figure2.pdf">Attributes, metric, operationalizations </a> <br> 


### 2.3. Building quality model {#building}
The hierarchical decomposition of the quality model was performed using thematic analysis. This method provides a rigorous and systematic way to process qualitative information by identifying, analyzing, and eliciting patterns (themes) within the data collected [42].
Figure 3 shows the process carried out collaboratively by the team of authors, in working meetings, and consisted of the following steps:


<img src="./images/Figure3.png " alt="Figure 3" width="600px" align="center">

Figure 3. <a href ="./images/Figure3.pdf">Process for decomposition of the quality model </a> <br> 

1. Coding: we read the selected primary studies and identified the text segments that refer to quality characteristics, quality attributes, and metrics. Then, the text segments containing relevant information were coded using a labeling system developed by the authors. Mendeley has been used as a support tool.
2. Transforming codes into themes: the codes obtained were analyzed to compare them and classify them into categories
to combine them into potential themes. This process has been performed iteratively for each attribute and metric.
3. Reviewing and refining themes: the themes obtained have been reviewed and compared to detect coincidences/repetitions.
The quality attributes, the metrics, and the cloud artifacts (where the metrics are applied) were compared with each other
to understand the themes. The result was a set of themes related to quality characteristics, quality attributes, and metrics.
 


### 2.4. Quality model for cloud services {#model}
The model is organized hierarchically, from characteristics and subcharacteristics to attributes, metrics, and operationalizations. 
The proposed cloud services quality model is an adaptation and extension of the ISO/IEC 25010 SQuaRE standard to suit the cloud services domain. The process involved examining the eight characteristics of this standard and the 406 metrics from Guerron et al. [3]. The analysis and decomposition process resulted in 68 subcharacteristics that expand the subcharacteristics of the standard and 240 related attributes, which were used to build the hierarchical decomposition of the quality model. Figure 4 shows the model diagram down to the level of characteristics and subcharacteristics, including existing and adding new ones.

![Figure 4](./images/Figure4.png "Figure 4")

Figure 4.<a href ="./images/Figure4.pdf">Cloud service quality characteristics and subcharacteristics</a> <br> 

<br> 

### 2.5 Instrucciones para el modelo de calidad de PowerBI** <br> 

 - Download **PowerBI file** on Local
 <a href ="./files/modelv3.pbix"> Quality Model for Cloud Services </a> <br> 
 - Open <a href = "https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads"> Power BI application on cloud </a> <br> 
 - Open **My wokspace**
 - Import **Report, Paginated Report or Workbook**
 - Seleect **From this computer** search the local file


 For more details see the **Demo Video**

 <video width="640" height="360" controls>
  <source src="./files/demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<!--[Watch the video]<a href = "https://github.com/ximeguerron/qualityModel/files/demo.mp4" target="_blank">**Demo **</a><br/>Download and play the Demo PowerBI Project

Link to **Excel** file <a href ="https://support.office.com/en-us/article/Start-the-Power-Pivot-add-in-for-Excel-a891a66d-36e3-43fc-81e8-fc4798f39ea8"> How to enable Excel complements

NOTE: In order to visualize the reports, please enable de _Power Pivot_ and _Power View_ complements of Excel. -->


# 3. Aplicación del Modelo de Calidad en un Entorno industrial {#qmcaso}
Se presenta un estudio de caso orientado a validar empíricamente el modelo de calidad genérico propuesto. 

El objetivo del estudio de caso era demostrar la viabilidad de implementar el modelo de calidad propuesto para evaluar los servicios en la nube (por ejemplo, bases de datos, aplicaciones y microservicios).

La unidad de análisis consistió en un único caso de SaaS denominado «Social Alert» (SAlert) que se ejecutaba en un entorno operativo de prueba. Se trata de un caso real de SaaS en la industria, un sistema de ciencia de datos aplicado al análisis de redes basado en contenidos.

La Figura 6 muestra la descomposición de las características de calidad en subcaracterísticas, atributos de calidad y métricas para el estudio de caso.


![Figure 6](./images/Figure6.png "Figure 6")
 Figure 6.<a href ="./images/Figure6.pdf">SaaS Salert Quality Model</a> <br> 

We used a third-party tool called New Relic [38] to perform the measurements by gathering low-level raw data from the components of the SaaS, calculating others’ metrics, and resulting in values on the measurement scales
We present the graphical representation of some measurement results performed during a period of time for some specific metrics, and we separate them into different dashboard groupings by layers of component monitoring (e.g., host, PostgreSQL, containers, API).

<a href ="./images/Figure9.pdf"> Figure 7 </a> reports the monitored SaaS API using the throughput, response time, success, and error rate measurements.

![Figure 7](./images/Figure9.png "SaaS monitor")
 Figure 7.<a href ="./images/Figure9.pdf">SaaS monitor </a> <be> 

<a href ="./images/Figure8.a.pdf"> Figure 8.a </a>, reports the PaaS PostgreSQL instance's current state we monitored the connections, commits, and the DB operations rate as new metrics. 

Regarding the  <a href ="./images/Figure8.b.pdf"> Figure 8.b </a> PaaS containers, we represented the memory usage, and packets received and sent. Resources are shared
among all the containers.

![Figure 8.a](./images/Figure8.a.png "Figure8.a")
 Figure 8.a.<a href ="./images/Figure8.a.pdf">PaaS DB Instance monitor</a> <br> 

![Figure 8.b](./images/Figure8.b.png "PaaS Container monitor")
 Figure 8.b.<a href ="./images/Figure8.b.pdf">PaaS Container monitor</a> <be> 


<a href ="./images/Figure7.pdf"> Figure 9 </a>, reports the current IaaS state with the usage of CPU, memory, and storage measurements.

![Figure 9](./images/Figure7.png "IaaS monitor")
  Figure 9.<a href ="./images/Figure7.pdf">IaaS monitor </a> <br> 

  
<!--The tool monitor setting and   <p> 1. <a href ="https://onenr.io/02wdKxE1XQE"> IaaS monitor </a> <br>-->
  

## 4. Procesos de Modelado para el Pronóstico de QoS

## 5. Modelos de Pronóstico de QoS para servicios cloud
Esta sección gestiona los archivos utilizados en el experimento controlado, cuyo propósito es comparar el desempeño de dos modelos de aprendizaje profundo—BI-GRU y LSTM—con ARIMA, un método estadístico ampliamente utilizado en el análisis de series temporales. Los modelos fueron desarrollados con el objetivo de generar **_pronosticos sobre la calidad de un servicio cloud_** en operación en un entorno industrial.

La siguiente sección presenta los resultados obtenidos para las 16 variables utilizadas en el experimento, junto con información adicional relacionada con ellas.

### 5.1. Datasets {#Datos}
Representación de los **_conjuntos de datos_**  con las observaciones de 16 métricas de calidad de servicio extraídas de la supervisión del servicio cloud SAlert.
- <a href ="./experiment/data.csv">  Data set </a>


| Variable            | Conjunto de datos                                                                |
|---------------------|----------------------------------------------------------------------------|
| Free Memory         | ![FreeMemory_data.jpg](imgs/dataset/FreeMemory_data.jpg)               |
| Used Memory         | ![UsedMemory_data.jpg](imgs/dataset/UsedMemory_data.jpg)               |
| Free Disk           | ![Free Disk_dataset.png](imgs/dataset/FreeDisk_data.jpg)                   |
| Used Disk           | ![Used Disk_dataset.png](imgs/dataset/UsedDisk_data.jpg)                   |
| Disk read/s         | ![Disk read_s_dataset.png](imgs/dataset/Diskreads_data.jpg)               |
| Disk write/s        | ![Disk write_s_dataset.png](imgs/dataset/Diskwrites_data.jpg)             |
| NetBytes In         | ![NetBytes In_dataset.png](imgs/dataset/NetBytesIn_data.jpg)               |
| NetBytes Out        | ![NetBytes Out_dataset.png](imgs/dataset/NetBytesOut_data.jpg)             |
| NetPackets In       | ![NetPackets In_dataset.png](imgs/dataset/NetPacketsIn_data.jpg)           |
| NetPackets Out      |  ![NetPackets Out_dataset.png](imgs/dataset/NetPacketsOut_data.jpg)          |
| Rx packets          | ![Rx packets_dataset.png](imgs/dataset/Rxpackets_data.jpg)                 |
| Tx packets          | ![Tx packets_dataset.png](imgs/dataset/Txpackets_data.jpg)                 |
| CPU percent         | ![MemoryUsedpercent_dataset.png](imgs/dataset/CPUpercent_data.jpg)         |
| Memory Used percent | ![Used Memory_dataset.png](imgs/dataset/MemoryUsedpercent_data.jpg)       |
| Disk Used percent   | ![Disk Used percent_dataset.png](imgs/dataset/DiskUsedpercent_data.jpg) |
| Uptime              | ![Uptime_dataset.png](imgs/dataset/Uptime_data.jpg)                     |

[Indice](#Home)

### 5.2. Jupiter Notebooks {#notebook}
The study notebooks are available here.

#### 5.2.1 Model Development Notebook 
The notebook, which performs the models' training and validation, is available on the link, and the directories required for execution are detailed on the readme.txt file

|Action|Link |
|---------------------|-------------|
| Open in Google Colab         | <a href="https://drive.google.com/file/d/119A84lUytPZH5oi05jGiDRFsKz3wfdvK/view?usp=sharing"> <img src="./imgs/colab.png" alt="Open In Colab"/> </a>|
| Download file.ipynb |<a href="./experiment/bigru_lstm_ari_univariate_experiment.ipynb" download> <img src="./imgs/jupiter.png" alt="Jupiter Notebook"/> </a> |

#### 5.2.2 Hypotheses Testing Notebook
The notebook, which performs the hypothesis testing, is available on the link, and the dataset files required for execution are included in the statistics directory.

|Action|Link |
|---------------------|-------------|
| Open in Google Colab         | <a href="https://drive.google.com/file/d/1eJAd0O-HS4nhspPVj50LhO4X3Q-tTXUQ/view?usp=sharing"><img src="./imgs/colab.png" alt="Open In Colab"/> </a>|
| Download file.ipynb |<a href="./statistics/Permanova.ipynb" download> <img src="./imgs/jupiter.png" alt="Jupiter Notebook"/> </a> |


[Indice](#Home)

### 5.3. BI-GRU Accuracy Metrics {#MetricBiGru}
BI-GRU model performance evaluation using accuracy metrics **_RMSE, MAE, MAPE_** 

| Variable            | RMSE                                                                     | MAE                                                                     | MAPE                                                                     | 
|---------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| **_Free Memory_**        
Iteration 1| ![Free Memory_mrse.png](imgs/BiGru/metrics/iteration_0_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/BiGru/metrics/Iteration_0_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/BiGru/metrics/iteration_0_Free%20Memory_mape.png)                   | 
|Iteration 2         | ![Free Memory_mrse.png](imgs/BiGru/metrics/iteration_1_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/BiGru/metrics/Iteration_1_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/BiGru/metrics/iteration_1_Free%20Memory_mape.png)                   | 
| Iteration 3        | ![Free Memory_mrse.png](imgs/BiGru/metrics/iteration_2_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/BiGru/metrics/Iteration_2_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/BiGru/metrics/iteration_2_Free%20Memory_mape.png)                   | 
| **_Used Memory_**         
Iteration 1| ![Used Memory_rmse.png](imgs/BiGru/metrics/iteration_0_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/BiGru/metrics/Iteration_0_Used%20Memory_mae.png)                    | ![Used Memory_mape.png](imgs/BiGru/metrics/iteration_0_Used%20Memory_mape.png) | 
| Iteration 2         | ![Used Memory_rmse.png](imgs/BiGru/metrics/iteration_1_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/BiGru/metrics/Iteration_1_Used%20Memory_mae.png)                    | ![Used Memory_mape.png](imgs/BiGru/metrics/iteration_1_Used%20Memory_mape.png) | 
| Iteration 3         | ![Used Memory_rmse.png](imgs/BiGru/metrics/iteration_2_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/BiGru/metrics/Iteration_2_Used%20Memory_mae.png)   | ![Used Memory_mape.png](imgs/BiGru/metrics/iteration_2_Used%20Memory_mape.png)          | 
| **_Free Disk_**           
Iteration 1| ![FreeDisk_rmse.png](imgs/BiGru/metrics/iteration_0_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/BiGru/metrics/Iteration_0_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/BiGru/metrics/iteration_0_Free%20Disk_mape.png) | 
|Iteration 2| ![FreeDisk_rmse.png](imgs/BiGru/metrics/iteration_1_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/BiGru/metrics/Iteration_1_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/BiGru/metrics/iteration_1_Free%20Disk_mape.png) | 
|Iteration 3| ![FreeDisk_rmse.png](imgs/BiGru/metrics/iteration_2_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/BiGru/metrics/Iteration_2_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/BiGru/metrics/iteration_2_Free%20Disk_mape.png) | 
| **_Used Disk_**
Iteration 1| ![Used Disk_rmse.png](imgs/BiGru/metrics/iteration_0_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/BiGru/metrics/Iteration_0_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/BiGru/metrics/iteration_0_Used%20Disk_mape.png) | 
|Iteration 2| ![Used Disk_rmse.png](imgs/BiGru/metrics/iteration_1_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/BiGru/metrics/Iteration_1_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/BiGru/metrics/iteration_1_Used%20Disk_mape.png) | 
|Iteration 3| ![Used Disk_rmse.png](imgs/BiGru/metrics/iteration_2_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/BiGru/metrics/Iteration_2_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/BiGru/metrics/iteration_2_Used%20Disk_mape.png) | 
| **_Disk read/s_**
Iteration 1|![Disk_read_s_rmse.png](imgs/BiGru/metrics/iteration_0_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/BiGru/metrics/Iteration_0_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/BiGru/metrics/iteration_0_Disk%20read_s_mape.png) | 
|Iteration 2|![Disk_read_s_rmse.png](imgs/BiGru/metrics/iteration_1_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/BiGru/metrics/Iteration_1_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/BiGru/metrics/iteration_1_Disk%20read_s_mape.png) | 
|Iteration 3|![Disk_read_s_rmse.png](imgs/BiGru/metrics/iteration_2_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/BiGru/metrics/Iteration_2_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/BiGru/metrics/iteration_2_Disk%20read_s_mape.png) | 
| **_Disk write/s_**
Iteration 1|![Disk write_s_rmse.png](imgs/BiGru/metrics/iteration_0_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/BiGru/metrics/Iteration_0_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/BiGru/metrics/iteration_0_Disk%20write_s_mape.png) | 
|Iteration 2|![Disk write_s_rmse.png](imgs/BiGru/metrics/iteration_1_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/BiGru/metrics/Iteration_1_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/BiGru/metrics/iteration_1_Disk%20write_s_mape.png) | 
|Iteration 3|![Disk write_s_rmse.png](imgs/BiGru/metrics/iteration_2_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/BiGru/metrics/Iteration_2_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/BiGru/metrics/iteration_2_Disk%20write_s_mape.png) | 
| **_NetBytes In_**     
Iteration 1| ![NetBytes In_rmse.png](imgs/BiGru/metrics/iteration_0_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/BiGru/metrics/Iteration_0_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/BiGru/metrics/iteration_0_NetBytes%20In_mape.png) | 
|Iteration 2| ![NetBytes In_rmse.png](imgs/BiGru/metrics/iteration_1_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/BiGru/metrics/Iteration_1_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/BiGru/metrics/iteration_1_NetBytes%20In_mape.png) | 
|Iteration 3| ![NetBytes In_rmse.png](imgs/BiGru/metrics/iteration_2_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/BiGru/metrics/Iteration_2_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/BiGru/metrics/iteration_2_NetBytes%20In_mape.png) | 
| **_NetBytes Out_**  
Iteration 1 |![NetBytes Out_rmse.png](imgs/BiGru/metrics/iteration_0_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/BiGru/metrics/Iteration_0_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/BiGru/metrics/iteration_0_NetBytes%20Out_mape.png) | 
|Iteration 2 | ![NetBytes Out_rmse.png](imgs/BiGru/metrics/iteration_1_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/BiGru/metrics/Iteration_1_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/BiGru/metrics/iteration_1_NetBytes%20Out_mape.png) |
|Iteration 3 | ![NetBytes Out_rmse.png](imgs/BiGru/metrics/iteration_2_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/BiGru/metrics/Iteration_2_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/BiGru/metrics/iteration_2_NetBytes%20Out_mape.png) |
| **_NetPackets In_**   
Iteration 1| ![NetPackets In_rmse.png](imgs/BiGru/metrics/iteration_0_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/BiGru/metrics/Iteration_0_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/BiGru/metrics/iteration_0_NetPackets%20In_mape.png) | 
|Iteration 2| ![NetPackets In_rmse.png](imgs/BiGru/metrics/iteration_1_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/BiGru/metrics/Iteration_1_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/BiGru/metrics/iteration_1_NetPackets%20In_mape.png) | 
|Iteration 3| ![NetPackets In_rmse.png](imgs/BiGru/metrics/iteration_2_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/BiGru/metrics/Iteration_2_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/BiGru/metrics/iteration_2_NetPackets%20In_mape.png) | 
| **_NetPackets Out_**   
Iteration 1|![NetPackets Out_rmse.png](imgs/BiGru/metrics/iteration_0_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/BiGru/metrics/Iteration_0_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/BiGru/metrics/iteration_0_NetPackets%20Out_mape.png) | 
|Iteration 2|![NetPackets Out_rmse.png](imgs/BiGru/metrics/iteration_1_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/BiGru/metrics/Iteration_1_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/BiGru/metrics/iteration_1_NetPackets%20Out_mape.png) | 
| Iteration 3|![NetPackets Out_rmse.png](imgs/BiGru/metrics/iteration_2_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/BiGru/metrics/Iteration_2_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/BiGru/metrics/iteration_2_NetPackets%20Out_mape.png) |     
| **_Rx packets_**    
Iteration 1|![Rx packets_rmse.png](imgs/BiGru/metrics/iteration_0_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/BiGru/metrics/Iteration_0_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/BiGru/metrics/iteration_0_Rx%20packets_mape.png) | 
|Iteration 2|![Rx packets_rmse.png](imgs/BiGru/metrics/iteration_1_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/BiGru/metrics/Iteration_1_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/BiGru/metrics/iteration_1_Rx%20packets_mape.png) | 
|Iteration 3|![Rx packets_rmse.png](imgs/BiGru/metrics/iteration_2_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/BiGru/metrics/Iteration_2_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/BiGru/metrics/iteration_2_Rx%20packets_mape.png) | 
| **_Tx packets_**         
Iteration 1 |![Tx packets_rmse.png](imgs/BiGru/metrics/iteration_0_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/BiGru/metrics/Iteration_0_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/BiGru/metrics/iteration_0_Tx%20packets_mape.png) | 
|Iteration 2 |![Tx packets_rmse.png](imgs/BiGru/metrics/iteration_1_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/BiGru/metrics/Iteration_1_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/BiGru/metrics/iteration_1_Tx%20packets_mape.png) | 
|Iteration 3 |![Tx packets_rmse.png](imgs/BiGru/metrics/iteration_2_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/BiGru/metrics/Iteration_2_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/BiGru/metrics/iteration_2_Tx%20packets_mape.png) | 
| **_CPU percent_**
Iteration 1| ![CPU percent_rmse.png](imgs/BiGru/metrics/iteration_0_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/BiGru/metrics/Iteration_0_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/BiGru/metrics/iteration_0_CPU%20percent_mape.png) | 
|Iteration 2         | ![CPU percent_mrse.png](imgs/BiGru/metrics/iteration_1_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/BiGru/metrics/Iteration_1_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/BiGru/metrics/iteration_1_CPU%20percent_mape.png) | 
| Iteration 3| ![CPU percent_mrse.png](imgs/BiGru/metrics/iteration_2_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/BiGru/metrics/Iteration_2_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/BiGru/metrics/iteration_2_CPU%20percent_mape.png)  
| **_Memory Used percent_** 
Iteration 1 |![Memory Used percent_rmse.png](imgs/BiGru/metrics/iteration_0_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/BiGru/metrics/Iteration_0_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/BiGru/metrics/iteration_0_Memory%20Used%20percent_mape.png) | 
|Iteration 2 |![Memory Used percent_rmse.png](imgs/BiGru/metrics/iteration_1_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/BiGru/metrics/Iteration_1_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/BiGru/metrics/iteration_1_Memory%20Used%20percent_mape.png) |
|Iteration 3 |![Memory Used percent_rmse.png](imgs/BiGru/metrics/iteration_2_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/BiGru/metrics/Iteration_2_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/BiGru/metrics/iteration_2_Memory%20Used%20percent_mape.png) |
| **_Disk Used percent_**  
Iteration 1 |![Disk Used percent_rmse.png](imgs/BiGru/metrics/iteration_0_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/BiGru/metrics/Iteration_0_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/BiGru/metrics/iteration_0_Disk%20Used%20percent_mape.png) | 
Iteration 2 |![Disk Used percent_rmse.png](imgs/BiGru/metrics/iteration_1_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/BiGru/metrics/Iteration_1_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/BiGru/metrics/iteration_1_Disk%20Used%20percent_mape.png) |
Iteration 3 |![Disk Used percent_rmse.png](imgs/BiGru/metrics/iteration_2_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/BiGru/metrics/Iteration_2_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/BiGru/metrics/iteration_2_Disk%20Used%20percent_mape.png) |
| **_Uptime_**
Iteration 1 | ![Uptime_rmse.png](imgs/BiGru/metrics/iteration_0_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/BiGru/metrics/Iteration_0_Uptime_mae.png) | 	![Uptime_mape.png](imgs/BiGru/metrics/iteration_0_Uptime_mape.png) | 
|Iteration 2 |  ![Uptime_rmse.png](imgs/BiGru/metrics/iteration_1_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/BiGru/metrics/Iteration_1_Uptime_mae.png) | 	![Uptime_mape.png](imgs/BiGru/metrics/iteration_1_Uptime_mape.png) | 
|Iteration 3 |  ![Uptime_rmse.png](imgs/BiGru/metrics/iteration_2_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/BiGru/metrics/Iteration_2_Uptime_mae.png) | 	![Uptime_mape.png](imgs/BiGru/metrics/iteration_2_Uptime_mape.png) | 

[Indice](#Home)

### 5.4. LSTM  Metricas de precisión {#MetricLSTM}
LSTM model performance evaluation using accuracy metrics **_RMSE, MAE, MAPE_** 

| Variable            | RMSE                                                                     | MAE                                                                     | MAPE                                                                     | 
|---------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| **_Free Memory_**        
Iteration 1| ![Free Memory_mrse.png](imgs/LSTM/metrics/iteration_0_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/LSTM/metrics/iteration_0_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/LSTM/metrics/iteration_0_Free%20Memory_mape.png)                   | 
|Iteration 2         | ![Free Memory_mrse.png](imgs/LSTM/metrics/iteration_1_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/LSTM/metrics/iteration_1_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/LSTM/metrics/iteration_1_Free%20Memory_mape.png)                   | 
| Iteration 3        | ![Free Memory_mrse.png](imgs/LSTM/metrics/iteration_2_Free%20Memory_rmse.png)                   | ![Free Memory_mae.png](imgs/LSTM/metrics/iteration_2_Free%20Memory_mae.png)                    | ![Free Memory_mape.png](imgs/LSTM/metrics/iteration_2_Free%20Memory_mape.png)                   | 
| **_Used Memory_**         
Iteration 1| ![Used Memory_rmse.png](imgs/LSTM/metrics/iteration_0_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/LSTM/metrics/iteration_0_Used%20Memory_mae.png)                    | ![Used Memory_mape.png](imgs/LSTM/metrics/iteration_0_Used%20Memory_mape.png) | 
| Iteration 2         | ![Used Memory_rmse.png](imgs/LSTM/metrics/iteration_1_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/LSTM/metrics/iteration_1_Used%20Memory_mae.png)                    | ![Used Memory_mape.png](imgs/LSTM/metrics/iteration_1_Used%20Memory_mape.png) | 
| Iteration 3         | ![Used Memory_rmse.png](imgs/LSTM/metrics/iteration_2_Used%20Memory_rmse.png)                   | ![Used Memory_mae.png](imgs/LSTM/metrics/iteration_2_Used%20Memory_mae.png)   | ![Used Memory_mape.png](imgs/LSTM/metrics/iteration_2_Used%20Memory_mape.png)          | 
| **_Free Disk_**           
Iteration 1| ![FreeDisk_rmse.png](imgs/LSTM/metrics/iteration_0_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/LSTM/metrics/iteration_0_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/LSTM/metrics/iteration_0_Free%20Disk_mape.png) | 
|Iteration 2| ![FreeDisk_rmse.png](imgs/LSTM/metrics/iteration_1_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/LSTM/metrics/iteration_1_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/LSTM/metrics/iteration_1_Free%20Disk_mape.png) | 
|Iteration 3| ![FreeDisk_rmse.png](imgs/LSTM/metrics/iteration_2_Free%20Disk_rmse.png) |  ![FreeDisk_mae.png](imgs/LSTM/metrics/iteration_2_Free%20Disk_mae.png)|        ![FreeDisk_mape.png](imgs/LSTM/metrics/iteration_2_Free%20Disk_mape.png) | 
| **_Used Disk_**
Iteration 1| ![Used Disk_rmse.png](imgs/LSTM/metrics/iteration_0_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/LSTM/metrics/iteration_0_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/LSTM/metrics/iteration_0_Used%20Disk_mape.png) | 
|Iteration 2| ![Used Disk_rmse.png](imgs/LSTM/metrics/iteration_1_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/LSTM/metrics/iteration_1_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/LSTM/metrics/iteration_1_Used%20Disk_mape.png) | 
|Iteration 3| ![Used Disk_rmse.png](imgs/LSTM/metrics/iteration_2_Used%20Disk_rmse.png) | ![Used Disk_mae.png](imgs/LSTM/metrics/iteration_2_Used%20Disk_mae.png) | ![Used Disk_mape.png](imgs/LSTM/metrics/iteration_2_Used%20Disk_mape.png) | 
| **_Disk read/s_**
Iteration 1|![Disk_read_s_rmse.png](imgs/LSTM/metrics/iteration_0_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/LSTM/metrics/iteration_0_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/LSTM/metrics/iteration_0_Disk%20read_s_mape.png) | 
|Iteration 2|![Disk_read_s_rmse.png](imgs/LSTM/metrics/iteration_1_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/LSTM/metrics/iteration_1_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/LSTM/metrics/iteration_1_Disk%20read_s_mape.png) | 
|Iteration 3|![Disk_read_s_rmse.png](imgs/LSTM/metrics/iteration_2_Disk%20read_s_rmse.png) | 	![Disk_read_s_mae.png](imgs/LSTM/metrics/iteration_2_Disk%20read_s_mae.png) | 	![Disk_read_s_mape.png](imgs/LSTM/metrics/iteration_2_Disk%20read_s_mape.png) | 
| **_Disk write/s_**
Iteration 1|![Disk write_s_rmse.png](imgs/LSTM/metrics/iteration_0_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/LSTM/metrics/iteration_0_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/LSTM/metrics/iteration_0_Disk%20write_s_mape.png) | 
|Iteration 2|![Disk write_s_rmse.png](imgs/LSTM/metrics/iteration_1_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/LSTM/metrics/iteration_1_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/LSTM/metrics/iteration_1_Disk%20write_s_mape.png) | 
|Iteration 3|![Disk write_s_rmse.png](imgs/LSTM/metrics/iteration_2_Disk%20write_s_rmse.png) | 	![Disk write_s_mae.png](imgs/LSTM/metrics/iteration_2_Disk%20write_s_mae.png) | 	![Disk write_s_mape.png](imgs/LSTM/metrics/iteration_2_Disk%20write_s_mape.png) | 
| **_NetBytes In_**     
Iteration 1| ![NetBytes In_rmse.png](imgs/LSTM/metrics/iteration_0_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/LSTM/metrics/iteration_0_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/LSTM/metrics/iteration_0_NetBytes%20In_mape.png) | 
|Iteration 2| ![NetBytes In_rmse.png](imgs/LSTM/metrics/iteration_1_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/LSTM/metrics/iteration_1_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/LSTM/metrics/iteration_1_NetBytes%20In_mape.png) | 
|Iteration 3| ![NetBytes In_rmse.png](imgs/LSTM/metrics/iteration_2_NetBytes%20In_rmse.png) | 	![NetBytes In_mae.png](imgs/LSTM/metrics/iteration_2_NetBytes%20In_mae.png) | 	![NetBytes In_mape.png](imgs/LSTM/metrics/iteration_2_NetBytes%20In_mape.png) | 
| **_NetBytes Out_**  
Iteration 1 |![NetBytes Out_rmse.png](imgs/LSTM/metrics/iteration_0_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/LSTM/metrics/iteration_0_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/LSTM/metrics/iteration_0_NetBytes%20Out_mape.png) | 
|Iteration 2 | ![NetBytes Out_rmse.png](imgs/LSTM/metrics/iteration_1_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/LSTM/metrics/iteration_1_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/LSTM/metrics/iteration_1_NetBytes%20Out_mape.png) |
|Iteration 3 | ![NetBytes Out_rmse.png](imgs/LSTM/metrics/iteration_2_NetBytes%20Out_rmse.png) | 	![NetBytes Out_mae.png](imgs/LSTM/metrics/iteration_2_NetBytes%20Out_mae.png) | 	![NetBytes Out_mape.png](imgs/LSTM/metrics/iteration_2_NetBytes%20Out_mape.png) |
| **_NetPackets In_**   
Iteration 1| ![NetPackets In_rmse.png](imgs/LSTM/metrics/iteration_0_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/LSTM/metrics/iteration_0_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/LSTM/metrics/iteration_0_NetPackets%20In_mape.png) | 
|Iteration 2| ![NetPackets In_rmse.png](imgs/LSTM/metrics/iteration_1_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/LSTM/metrics/iteration_1_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/LSTM/metrics/iteration_1_NetPackets%20In_mape.png) | 
|Iteration 3| ![NetPackets In_rmse.png](imgs/LSTM/metrics/iteration_2_NetPackets%20In_rmse.png) | 	![NetPackets In_mae.png](imgs/LSTM/metrics/iteration_2_NetPackets%20In_mae.png) | 	![NetPackets In_mape.png](imgs/LSTM/metrics/iteration_2_NetPackets%20In_mape.png) | 
| **_NetPackets Out_**   
Iteration 1|![NetPackets Out_rmse.png](imgs/LSTM/metrics/iteration_0_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/LSTM/metrics/iteration_0_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/LSTM/metrics/iteration_0_NetPackets%20Out_mape.png) | 
|Iteration 2|![NetPackets Out_rmse.png](imgs/LSTM/metrics/iteration_1_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/LSTM/metrics/iteration_1_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/LSTM/metrics/iteration_1_NetPackets%20Out_mape.png) | 
| Iteration 3|![NetPackets Out_rmse.png](imgs/LSTM/metrics/iteration_2_NetPackets%20Out_rmse.png) | 	![NetPackets Out_mae.png](imgs/LSTM/metrics/iteration_2_NetPackets%20Out_mae.png) | ![NetPackets Out_mape.png](imgs/LSTM/metrics/iteration_2_NetPackets%20Out_mape.png) |     
| **_Rx packets_**    
Iteration 1|![Rx packets_rmse.png](imgs/LSTM/metrics/iteration_0_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/LSTM/metrics/iteration_0_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/LSTM/metrics/iteration_0_Rx%20packets_mape.png) | 
|Iteration 2|![Rx packets_rmse.png](imgs/LSTM/metrics/iteration_1_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/LSTM/metrics/iteration_1_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/LSTM/metrics/iteration_1_Rx%20packets_mape.png) | 
|Iteration 3|![Rx packets_rmse.png](imgs/LSTM/metrics/iteration_2_Rx%20packets_rmse.png) | 	![Rx packets_mae.png](imgs/LSTM/metrics/iteration_2_Rx%20packets_mae.png) | 	![Rx packets_mape.png](imgs/LSTM/metrics/iteration_2_Rx%20packets_mape.png) | 
| **_Tx packets_**         
Iteration 1 |![Tx packets_rmse.png](imgs/LSTM/metrics/iteration_0_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/LSTM/metrics/iteration_0_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/LSTM/metrics/iteration_0_Tx%20packets_mape.png) | 
|Iteration 2 |![Tx packets_rmse.png](imgs/LSTM/metrics/iteration_1_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/LSTM/metrics/iteration_1_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/LSTM/metrics/iteration_1_Tx%20packets_mape.png) | 
|Iteration 3 |![Tx packets_rmse.png](imgs/LSTM/metrics/iteration_2_Tx%20packets_rmse.png) | 	![Tx packets_mae.png](imgs/LSTM/metrics/iteration_2_Tx%20packets_mae.png) | 	![Tx packets_mape.png](imgs/LSTM/metrics/iteration_2_Tx%20packets_mape.png) | 
| **_CPU percent_**
Iteration 1| ![CPU percent_mrse.png](imgs/LSTM/metrics/iteration_0_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/LSTM/metrics/iteration_0_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/LSTM/metrics/iteration_0_CPU%20percent_mape.png) | 
|Iteration 2         | ![CPU percent_mrse.png](imgs/LSTM/metrics/iteration_1_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/LSTM/metrics/iteration_1_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/LSTM/metrics/iteration_1_CPU%20percent_mape.png) | 
| Iteration 3| ![CPU percent_mrse.png](imgs/LSTM/metrics/iteration_2_CPU%20percent_rmse.png)                   | ![CPU percent_mae.png](imgs/LSTM/metrics/iteration_2_CPU%20percent_mae.png)                    | ![CPU percent_mape.png](imgs/LSTM/metrics/iteration_2_CPU%20percent_mape.png)  
| **_Memory Used percent_** 
Iteration 1 |![Memory Used percent_rmse.png](imgs/LSTM/metrics/iteration_0_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/LSTM/metrics/iteration_0_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/LSTM/metrics/iteration_0_Memory%20Used%20percent_mape.png) | 
|Iteration 2 |![Memory Used percent_rmse.png](imgs/LSTM/metrics/iteration_1_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/LSTM/metrics/iteration_1_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/LSTM/metrics/iteration_1_Memory%20Used%20percent_mape.png) |
|Iteration 3 |![Memory Used percent_rmse.png](imgs/LSTM/metrics/iteration_2_Memory%20Used%20percent_rmse.png) | 	![Memory Used percent_mae.png](imgs/LSTM/metrics/iteration_2_Memory%20Used%20percent_mae.png) | 	![Memory Used percent_mape.png](imgs/LSTM/metrics/iteration_2_Memory%20Used%20percent_mape.png) |
| **_Disk Used percent_**  
Iteration 1 |![Disk Used percent_rmse.png](imgs/LSTM/metrics/iteration_0_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/LSTM/metrics/iteration_0_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/LSTM/metrics/iteration_0_Disk%20Used%20percent_mape.png) | 
Iteration 2 |![Disk Used percent_rmse.png](imgs/LSTM/metrics/iteration_1_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/LSTM/metrics/iteration_1_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/LSTM/metrics/iteration_1_Disk%20Used%20percent_mape.png) |
Iteration 3 |![Disk Used percent_rmse.png](imgs/LSTM/metrics/iteration_2_Disk%20Used%20percent_rmse.png) | 	![Disk Used percent_mae.png](imgs/LSTM/metrics/iteration_2_Disk%20Used%20percent_mae.png) | 	![Disk Used percent_mape.png](imgs/LSTM/metrics/iteration_2_Disk%20Used%20percent_mape.png) |
| **_Uptime_**
Iteration 1 | ![Uptime_rmse.png](imgs/LSTM/metrics/iteration_0_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/LSTM/metrics/iteration_0_Uptime_mae.png) | 	![Uptime_mape.png](imgs/LSTM/metrics/iteration_0_Uptime_mape.png) | 
|Iteration 2 |  ![Uptime_rmse.png](imgs/LSTM/metrics/iteration_1_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/LSTM/metrics/iteration_1_Uptime_mae.png) | 	![Uptime_mape.png](imgs/LSTM/metrics/iteration_1_Uptime_mape.png) | 
|Iteration 3 |  ![Uptime_rmse.png](imgs/LSTM/metrics/iteration_2_Uptime_rmse.png) | 	![Uptime_mae.png](imgs/LSTM/metrics/iteration_2_Uptime_mae.png) | 	![Uptime_mape.png](imgs/LSTM/metrics/iteration_2_Uptime_mape.png) | 

[Index](#Home)

### 5.5. Modelo de pronóstico BI-GRU {#BIGRU}
BI-GRU Model fitting with prequential cross-validation

| Variable            | Iteration 1                | Iteration 2              | Iteration 3  | 
|---------------------|-----------------------|--------------------------------------|-----------------------|
| Free Memory         |![Free Memory_test.png](imgs/BiGru/results/iteration_0_Free%20Memory_test_result.png) | 	![Free Memory_test.png](imgs/BiGru/results/iteration_1_Free%20Memory_test_result.png) | 	![Free Memory_test.png](imgs/BiGru/results/iteration_2_Free%20Memory_test_result.png)| 
| Used Memory         | ![Used Memory_test.png](imgs/BiGru/results/iteration_0_Used%20Memory_test_result.png) | 	![Used Memory_test.png](imgs/BiGru/results/iteration_1_Used%20Memory_test_result.png) | 	![Used Memory_test.png](imgs/BiGru/results/iteration_2_Used%20Memory_test_result.png)|
| Free Disk           | ![Free Disk_test.png](imgs/BiGru/results/iteration_0_Free%20Disk_test_result.png) | 	![Free Disk_test.png](imgs/BiGru/results/iteration_1_Free%20Disk_test_result.png) | 	![Free Disk_test.png](imgs/BiGru/results/iteration_2_Free%20Disk_test_result.png) |  
| Used Disk           | ![Used Disk_test.png](imgs/BiGru/results/iteration_0_Used%20Disk_test_result.png) | 	![Used Disk_test.png](imgs/BiGru/results/iteration_1_Used%20Disk_test_result.png) | 	![Used Disk_test.png](imgs/BiGru/results/iteration_2_Used%20Disk_test_result.png) | 
| Disk read/s         | ![Disk read_s_test.png](imgs/BiGru/results/iteration_0_Disk%20read_s_test_result.png) | 	![Disk read_s_test.png](imgs/BiGru/results/iteration_1_Disk%20read_s_test_result.png) | 	![Disk read_s_test.png](imgs/BiGru/results/iteration_2_Disk%20read_s_test_result.png) | 
| Disk write/s        | ![Disk write_s_test.png](imgs/BiGru/results/iteration_0_Disk%20write_s_test_result.png) | 	![Disk write_s_test.png](imgs/BiGru/results/iteration_1_Disk%20write_s_test_result.png) | 	![Disk write_s_test.png](imgs/BiGru/results/iteration_2_Disk%20write_s_test_result.png) | 
| NetBytes In   | ![NetBytes In_test.png](imgs/BiGru/results/iteration_0_NetBytes%20In_test_result.png) | 	![NetBytes In_test.png](imgs/BiGru/results/iteration_1_NetBytes%20In_test_result.png) | 	![NetBytes In_test.png](imgs/BiGru/results/iteration_2_NetBytes%20In_test_result.png)| 
| NetBytes Out        | ![NetBytes Out_test.png](imgs/BiGru/results/iteration_0_NetBytes%20Out_test_result.png) | 	![NetBytes Out_test.png](imgs/BiGru/results/iteration_1_NetBytes%20Out_test_result.png) | 	![NetBytes Out_test.png](imgs/BiGru/results/iteration_2_NetBytes%20Out_test_result.png) | 
| NetPackets In       | ![NetPackets In_test.png](imgs/BiGru/results/iteration_0_NetPackets%20In_test_result.png) | 	![NetPackets In_test.png](imgs/BiGru/results/iteration_1_NetPackets%20In_test_result.png) | 	![NetPackets In_test.png](imgs/BiGru/results/iteration_2_NetPackets%20In_test_result.png) |
| NetPackets Out      |   ![NetPackets Out_test.png](imgs/BiGru/results/iteration_0_NetPackets%20Out_test_result.png) | 	![NetPackets Out_test.png](imgs/BiGru/results/iteration_1_NetPackets%20Out_test_result.png) | 	![NetPackets Out_test.png](imgs/BiGru/results/iteration_2_NetPackets%20Out_test_result.png) | 
| Rx packets          | ![Rx packets_test.png](imgs/BiGru/results/iteration_0_Rx%20packets_test_result.png) | 	![Rx packets_test.png](imgs/BiGru/results/iteration_1_Rx%20packets_test_result.png) | 	![Rx packets_test.png](imgs/BiGru/results/iteration_2_Rx%20packets_test_result.png) | 
| Tx packets          | ![Tx packets_test.png](imgs/BiGru/results/iteration_0_Tx%20packets_test_result.png) | 	![Tx packets_test.png](imgs/BiGru/results/iteration_1_Tx%20packets_test_result.png) | 	![Tx packets_test.png](imgs/BiGru/results/iteration_2_Tx%20packets_test_result.png) | 
| CPU percent         | ![CPU percent_test.png](imgs/BiGru/results/iteration_0_CPU%20percent_test_result.png) | 	![CPU percent_test.png](imgs/BiGru/results/iteration_1_CPU%20percent_test_result.png) | 	![CPU percent_test.png](imgs/BiGru/results/iteration_2_CPU%20percent_test_result.png)| 
| Memory Used percent | ![Memory Used percent_test.png](imgs/BiGru/results/iteration_0_Memory%20Used%20percent_test_result.png) | 	![Memory Used percent_test.png](imgs/BiGru/results/iteration_1_Memory%20Used%20percent_test_result.png) | 	![Memory Used percent_test.png](imgs/BiGru/results/iteration_2_Memory%20Used%20percent_test_result.png) | 
| Disk Used percent   | ![Disk Used percent_test.png](imgs/BiGru/results/iteration_0_Disk%20Used%20percent_test_result.png) | 	![Disk Used percent_test.png](imgs/BiGru/results/iteration_1_Disk%20Used%20percent_test_result.png) | 	![Disk Used percent_test.png](imgs/BiGru/results/iteration_2_Disk%20Used%20percent_test_result.png) | 
| Uptime              | ![Uptime_test.png](imgs/BiGru/results/iteration_0_Uptime_test_result.png) | 	![Uptime_test.png](imgs/BiGru/results/iteration_1_Uptime_test_result.png) | 	![Uptime_test.png](imgs/BiGru/results/iteration_2_Uptime_test_result.png) | 

[Index](#Home)

### 5.6. Modelo de pronóstico LSTM {#LSTM}
LSTM Model fitting with prequential cross-validation

| Variable            | Iteration 1                | Iteration 2              | Iteration 3  | 
|---------------------|-----------------------|--------------------------------------|-----------------------|
| Free Memory         |![Free Memory_test.png](imgs/LSTM/results/iteration_0_Free%20Memory_test_result.png) | 	![Free Memory_test.png](imgs/LSTM/results/iteration_1_Free%20Memory_test_result.png) | 	![Free Memory_test.png](imgs/LSTM/results/iteration_2_Free%20Memory_test_result.png)| 
| Used Memory         | ![Used Memory_test.png](imgs/LSTM/results/iteration_0_Used%20Memory_test_result.png) | 	![Used Memory_test.png](imgs/LSTM/results/iteration_1_Used%20Memory_test_result.png) | 	![Used Memory_test.png](imgs/LSTM/results/iteration_2_Used%20Memory_test_result.png)|
| Free Disk           | ![Free Disk_test.png](imgs/LSTM/results/iteration_0_Free%20Disk_test_result.png) | 	![Free Disk_test.png](imgs/LSTM/results/iteration_1_Free%20Disk_test_result.png) | 	![Free Disk_test.png](imgs/LSTM/results/iteration_2_Free%20Disk_test_result.png) |  
| Used Disk           | ![Used Disk_test.png](imgs/LSTM/results/iteration_0_Used%20Disk_test_result.png) | 	![Used Disk_test.png](imgs/LSTM/results/iteration_1_Used%20Disk_test_result.png) | 	![Used Disk_test.png](imgs/LSTM/results/iteration_2_Used%20Disk_test_result.png) | 
| Disk read/s         | ![Disk read_s_test.png](imgs/LSTM/results/iteration_0_Disk%20read_s_test_result.png) | 	![Disk read_s_test.png](imgs/LSTM/results/iteration_1_Disk%20read_s_test_result.png) | 	![Disk read_s_test.png](imgs/LSTM/results/iteration_2_Disk%20read_s_test_result.png) | 
| Disk write/s        | ![Disk write_s_test.png](imgs/LSTM/results/iteration_0_Disk%20write_s_test_result.png) | 	![Disk write_s_test.png](imgs/LSTM/results/iteration_1_Disk%20write_s_test_result.png) | 	![Disk write_s_test.png](imgs/LSTM/results/iteration_2_Disk%20write_s_test_result.png) | 
| NetBytes In   | ![NetBytes In_test.png](imgs/LSTM/results/iteration_0_NetBytes%20In_test_result.png) | 	![NetBytes In_test.png](imgs/LSTM/results/iteration_1_NetBytes%20In_test_result.png) | 	![NetBytes In_test.png](imgs/LSTM/results/iteration_2_NetBytes%20In_test_result.png)| 
| NetBytes Out        | ![NetBytes Out_test.png](imgs/LSTM/results/iteration_0_NetBytes%20Out_test_result.png) | 	![NetBytes Out_test.png](imgs/LSTM/results/iteration_1_NetBytes%20Out_test_result.png) | 	![NetBytes Out_test.png](imgs/LSTM/results/iteration_2_NetBytes%20Out_test_result.png) | 
| NetPackets In       | ![NetPackets In_test.png](imgs/LSTM/results/iteration_0_NetPackets%20In_test_result.png) | 	![NetPackets In_test.png](imgs/LSTM/results/iteration_1_NetPackets%20In_test_result.png) | 	![NetPackets In_test.png](imgs/LSTM/results/iteration_2_NetPackets%20In_test_result.png) |
| NetPackets Out      |   ![NetPackets Out_test.png](imgs/LSTM/results/iteration_0_NetPackets%20Out_test_result.png) | 	![NetPackets Out_test.png](imgs/LSTM/results/iteration_1_NetPackets%20Out_test_result.png) | 	![NetPackets Out_test.png](imgs/LSTM/results/iteration_2_NetPackets%20Out_test_result.png) | 
| Rx packets          | ![Rx packets_test.png](imgs/LSTM/results/iteration_0_Rx%20packets_test_result.png) | 	![Rx packets_test.png](imgs/LSTM/results/iteration_1_Rx%20packets_test_result.png) | 	![Rx packets_test.png](imgs/LSTM/results/iteration_2_Rx%20packets_test_result.png) | 
| Tx packets          | ![Tx packets_test.png](imgs/LSTM/results/iteration_0_Tx%20packets_test_result.png) | 	![Tx packets_test.png](imgs/LSTM/results/iteration_1_Tx%20packets_test_result.png) | 	![Tx packets_test.png](imgs/LSTM/results/iteration_2_Tx%20packets_test_result.png) | 
| CPU percent         | ![CPU percent_test.png](imgs/LSTM/results/iteration_0_CPU%20percent_test_result.png) | 	![CPU percent_test.png](imgs/LSTM/results/iteration_1_CPU%20percent_test_result.png) | 	![CPU percent_test.png](imgs/LSTM/results/iteration_2_CPU%20percent_test_result.png)| 
| Memory Used percent | ![Memory Used percent_test.png](imgs/LSTM/results/iteration_0_Memory%20Used%20percent_test_result.png) | 	![Memory Used percent_test.png](imgs/LSTM/results/iteration_1_Memory%20Used%20percent_test_result.png) | 	![Memory Used percent_test.png](imgs/LSTM/results/iteration_2_Memory%20Used%20percent_test_result.png) | 
| Disk Used percent   | ![Disk Used percent_test.png](imgs/LSTM/results/iteration_0_Disk%20Used%20percent_test_result.png) | 	![Disk Used percent_test.png](imgs/LSTM/results/iteration_1_Disk%20Used%20percent_test_result.png) | 	![Disk Used percent_test.png](imgs/LSTM/results/iteration_2_Disk%20Used%20percent_test_result.png) | 
| Uptime              | ![Uptime_test.png](imgs/LSTM/results/iteration_0_Uptime_test_result.png) | 	![Uptime_test.png](imgs/LSTM/results/iteration_1_Uptime_test_result.png) | 	![Uptime_test.png](imgs/LSTM/results/iteration_2_Uptime_test_result.png) | 

[Index](#Home)

### 5.7. Modelo de pronóstico ARIMA {#ARIMA}
ARIMA Model fitting with prequential cross-validation

| Variable            | Iteration 1                | Iteration 2              | Iteration 3  | 
|---------------------|-----------------------|--------------------------------------|-----------------------|
| Free Memory         | ![FreeMemory_.png](imgs/Arima/Iteration-0_FreeMemory_test_result.png) | 	![FreeMemory_.png](imgs/Arima/Iteration-1_FreeMemory_test_result.png) | 	![FreeMemory_.png](imgs/Arima/Iteration-2_FreeMemory_test_result.png) | 
| Used Memory         | ![UsedMemory_.png](imgs/Arima/Iteration-0_UsedMemory_test_result.png) | 	![UsedMemory_.png](imgs/Arima/Iteration-1_UsedMemory_test_result.png) | 	![UsedMemory_.png](imgs/Arima/Iteration-2_UsedMemory_test_result.png) |   
| Free Disk           | ![FreeDisk_test.png](imgs/Arima/Iteration-0_FreeDisk_test_result.png) | 	![FreeDisk_test.png](imgs/Arima/Iteration-1_FreeDisk_test_result.png) | 	![FreeDisk_test.png](imgs/Arima/Iteration-2_FreeDisk_test_result.png) | 
| Used Disk           | ![UsedDisk_test.png](imgs/Arima/Iteration-0_UsedDisk_test_result.png) | 	![UsedDisk_test.png](imgs/Arima/Iteration-1_UsedDisk_test_result.png) | 	![UsedDisk_test.png](imgs/Arima/Iteration-2_UsedDisk_test_result.png) | 
| Disk read/s         | ![Diskreads_test.png](imgs/Arima/Iteration-0_Diskreads_test_result.png) | 	![Diskreads_test.png](imgs/Arima/Iteration-1_Diskreads_test_result.png) | 	![Diskreads_test.png](imgs/Arima/Iteration-2_Diskreads_test_result.png) | 
| Disk write/s        | ![Diskwrites_test.png](imgs/Arima/Iteration-0_Diskwrites_test_result.png) | 	![Diskwrites_test.png](imgs/Arima/Iteration-1_Diskwrites_test_result.png) | 	![Diskwrites_test.png](imgs/Arima/Iteration-2_Diskwrites_test_result.png) | 
| NetBytes In         | ![NetBytes In_test.png](imgs/Arima/Iteration-0_NetBytesIn_test_result.png) | 	![NetBytes In_test.png](imgs/Arima/Iteration-1_NetBytesIn_test_result.png) | 	![NetBytes In_test.png](imgs/Arima/Iteration-2_NetBytesIn_test_result.png) | 
| NetBytes Out        | ![NetBytesOut_test.png](imgs/Arima/Iteration-0_NetBytesOut_test_result.png) | 	![NetBytesOut_test.png](imgs/Arima/Iteration-1_NetBytesOut_test_result.png) | 	![NetBytesOut_test.png](imgs/Arima/Iteration-2_NetBytesOut_test_result.png) | 
| NetPackets In       | ![NetPacketsIn_test.png](imgs/Arima/Iteration-0_NetPacketsIn_test_result.png) | 	![NetPacketsIn_test.png](imgs/Arima/Iteration-1_NetPacketsIn_test_result.png) | 	![NetPacketsIn_test.png](imgs/Arima/Iteration-2_NetPacketsIn_test_result.png) | 
| NetPackets Out      |  ![NetPacketsOut_test.png](imgs/Arima/Iteration-0_NetPacketsOut_test_result.png) | 	![NetPacketsOut_test.png](imgs/Arima/Iteration-1_NetPacketsOut_test_result.png) | 	![NetPacketsOut_test.png](imgs/Arima/Iteration-2_NetPacketsOut_test_result.png) |
| Rx packets          | ![Rxpackets_test.png](imgs/Arima/Iteration-0_Rxpackets_test_result.png) | 	![Rxpackets_test.png](imgs/Arima/Iteration-1_Rxpackets_test_result.png) | 	![Rxpackets_test.png](imgs/Arima/Iteration-2_Rxpackets_test_result.png) | 
| Tx packets          | ![Txpackets_test.png](imgs/Arima/Iteration-0_Txpackets_test_result.png) | 	![Txpackets_test.png](imgs/Arima/Iteration-1_Txpackets_test_result.png) | 	![Txpackets_test.png](imgs/Arima/Iteration-2_Txpackets_test_result.png) | 
| CPU percent         | ![CPUpercent_test.png](imgs/Arima/Iteration-0_CPUpercent_test_result.png) | 	![CPUpercent_test.png](imgs/Arima/Iteration-1_CPUpercent_test_result.png) | 	![CPUpercent_test.png](imgs/Arima/Iteration-2_CPUpercent_test_result.png) | 
| Memory Used percent | ![MemoryUsedpercent_test.png](imgs/Arima/Iteration-0_MemoryUsedpercent_test_result.png) | 	![MemoryUsedpercent_test.png](imgs/Arima/Iteration-1_MemoryUsedpercent_test_result.png) | 	![MemoryUsedpercent_test.png](imgs/Arima/Iteration-2_MemoryUsedpercent_test_result.png) | 
| Disk Used percent   | ![DiskUsedpercent_test.png](imgs/Arima/Iteration-0_DiskUsedpercent_test_result.png) | 	![DiskUsedpercent_test.png](imgs/Arima/Iteration-1_DiskUsedpercent_test_result.png) | 	![DiskUsedpercent_test.png](imgs/Arima/Iteration-2_DiskUsedpercent_test_result.png) | 
| Uptime              |![Uptime_rmse.png](imgs/Arima/Iteration-0_Uptime_test_result.png) | 	![Uptime_mae.png](imgs/Arima/Iteration-1_Uptime_test_result.png) | 	![Uptime_mape.png](imgs/Arima/Iteration-2_Uptime_test_result.png) | 

[Index](#Home)



### 5.8. Modelo de pronóstico AUTOARIMA {#AUTOARIMA}
ARIMA Model auto fitting with prequential cross-validation

| Variable            | Iteration 1                | Iteration 2              | Iteration 3  | 
|---------------------|-----------------------|--------------------------------------|-----------------------|
| Free Memory         | ![FreeMemory_.png](imgs/AutoArima/Iteration-0_FreeMemory_test_result.jpg) | 	![FreeMemory_.png](imgs/AutoArima/Iteration-1_FreeMemory_test_result.jpg) | 	![FreeMemory_.png](imgs/AutoArima/Iteration-2_FreeMemory_test_result.jpg) | 
| Used Memory         | ![UsedMemory_.png](imgs/AutoArima/Iteration-0_UsedMemory_test_result.jpg) | 	![UsedMemory_.png](imgs/AutoArima/Iteration-1_UsedMemory_test_result.jpg) | 	![UsedMemory_.png](imgs/AutoArima/Iteration-2_UsedMemory_test_result.jpg) |   
| Free Disk           | ![FreeDisk_test.png](imgs/AutoArima/Iteration-0_FreeDisk_test_result.jpg) | 	![FreeDisk_test.png](imgs/AutoArima/Iteration-1_FreeDisk_test_result.jpg) | 	![FreeDisk_test.png](imgs/AutoArima/Iteration-2_FreeDisk_test_result.jpg) | 
| Used Disk           | ![UsedDisk_test.png](imgs/AutoArima/Iteration-0_UsedDisk_test_result.jpg) | 	![UsedDisk_test.png](imgs/AutoArima/Iteration-1_UsedDisk_test_result.jpg) | 	![UsedDisk_test.png](imgs/AutoArima/Iteration-2_UsedDisk_test_result.jpg) | 
| Disk read/s         | ![Diskreads_test.png](imgs/AutoArima/Iteration-0_Diskreads_test_result.jpg) | 	![Diskreads_test.png](imgs/AutoArima/Iteration-1_Diskreads_test_result.jpg) | 	![Diskreads_test.png](imgs/AutoArima/Iteration-2_Diskreads_test_result.jpg) | 


## Contacto o soporte

Have trouble with Pages or any questions or suggestions? Please, contact us by email 
