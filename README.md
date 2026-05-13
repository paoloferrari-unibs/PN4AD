# PN4AD  
## PROFINET for Automotive Dataset (PN4AD)

PN4AD, **PROFINET for Automotive Dataset**, is a dataset derived from real industrial PROFINET networks during validation activities carried out in automotive production plants.

The dataset is intended to support research on industrial communication networks, PROFINET-based automation systems, network validation procedures, and data-driven analysis of industrial Ethernet infrastructures.

This release currently includes a .csv file containing anonymized plant-level and line-level information. 

NOTE: See Data Availability section for more details about distribution policy.

---

## Repository Content

The current release contains:

```text
PN4AD/
├── README.md
└── LineInformation.csv
```

The csv file contains anonymized statistical and validation metadata extracted from PROFINET network validation procedures.

---

## Dataset Description

The current version of PN4AD contains plant- and line-level information related to PROFINET network validation tests. Each row describes a production line and summarizes relevant validation outcomes, device counts, and network traffic load indicators.

The dataset includes both technical network metrics and validation labels, enabling exploratory analysis of industrial communication infrastructures and supporting future benchmarking activities.

---

## File Description

### `LineInformation.csv`

Excel file containing the anonymized dataset.

At the current stage, the file includes the following plant- and line-level information.

| Column Name | Description |
|---|---|
| `plant*` | Plant identifier encoded in alphabetical order based on the validation date. |
| `shop` | Shop category: `BODY` or `ASSEMBLY`. |
| `date_of_validation*` | `T001` corresponds to the first year present in the dataset, `T002` to the second year, and so on. Original calendar years and dates are not released. |
| `validation_result` | Overall outcome of the line test: `PASS` or `FAIL`. |
| `visual_inspection` | Overall outcome of the visual inspection: `Yes-Pass`, `Yes-Fail`, or `NULL`. |
| `oem_checklist` | Overall outcome of the OEM checklist inspection: `Yes-Pass`, `Yes-Fail`, or `NULL`. |
| `cable_certification` | Overall outcome of the cable certification test, only for relevant cables: `Yes-Pass`, `Yes-Fail`, or `NULL`. |
| `number_of_pn_devices` | Total number of PROFINET devices. |
| `number_of_devices` | Total number of devices in the network. |
| `additional_checks_for_frame_errors` | Additional checks on raw data to detect frame errors: `Yes-Pass`, `Yes-Fail`, or `NULL`. |
| `max_traffic_load` | Maximum network traffic load, expressed in Mbit/s. |
| `max_traffic_load_percent` | Maximum network traffic load expressed as a percentage. |
| `max_pn_traffic_load` | Maximum PROFINET network traffic load, expressed in Mbit/s. |
| `max_pn_traffic_load_percent` | Maximum PROFINET network traffic load expressed as a percentage. |
| `plcs_count` | Number of PLCs inside the line. |
| `rings_count` | Number of redundancy rings inside the line. |

`*` Anonymized field.

---

## Data Anonymization

Industrial identifiers and sensitive information have been anonymized before release.

In particular:

- plant identifiers are encoded alphabetically according to the validation date;
- validation dates are anonymized;
- proprietary names, network identifiers, and raw packet captures are not included in this release.

The released data only contains derived and anonymized information suitable for research and benchmarking purposes.

---

## Suggested Use Cases

PN4AD can be used for:

- exploratory analysis of PROFINET network validation data;
- statistical characterization of industrial Ethernet infrastructures;
- analysis of traffic load indicators in automotive production networks;
- investigation of relationships between validation checks and final line outcomes;
- benchmarking of data-driven methods for industrial network assessment.

---

## Data Availability

The authors are committed to scientific transparency and collaborative research. The complete derived database, containing all anonymized statistical features and validation labels, is available upon request to facilitate benchmarking and collaborative research. Please, contact us describing the your intendend use.
Note: The full traffic captures (raw pcap files) are restricted by non-disclosure agreements due to confidenciality constrains. 

---

## License

The source specifies that the data can be used as is without any warranty. 

Current license: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
Public License

See LICENSE.txt for details.

---

## Citation

If you use PN4AD in your research, please cite this repository

```bibtex
@article{pn4ad,
  title   = {PNT4AD},
  author  = {Ferrari, Paolo and Gaffurini, Massimiliano Sisinni, Emiliano and Brandão, Dennis},
  year    = {2026},
  url = {https://github.com/paoloferrari-unibs/PN4AD}
}
```

---

## Contact

For questions, collaboration requests, or access to additional derived data, please contact:

```text
Name: Paolo Ferrari
Institution: Università di Brescia
Email: paolo.ferrari@unibs.it
```

---

## Other Related Scientific Articles

Related publications from the same reserch team that developed the PN4AD, sorted by publication year in descending order.

[1] E. Sisinni, D. Brandao, A. Flammini, M. Gaffurini, and P. Ferrari, "Clustering of Distributed Observations for Traffic Classification in Industrial Networks", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, 2025, doi: 10.1109/WFCS63373.2025.11077637.

[2] H. P. Duarte, D. Brandao, P. Ferrari, and C. D. Maciel, "Analysis of Operating Conditions and Failure Detection in Industrial PROFINET Networks", *2025 16th IEEE International Conference on Industry Applications, INDUSCON 2025 - Proceedings*, pp. 332 - 333, 2025, doi: 10.1109/INDUSCON66435.2025.11241814.

[3] M. Gaffurini, D. Brandao, S. Rinaldi, A. Flammini, E. Sisinni, and P. Ferrari, "Characterizing the Real-Time Communication Performance of Virtual PLC in Industrial Edge Platform", *IEEE Open Journal of Instrumentation and Measurement*, vol. 4, 2025, doi: 10.1109/OJIM.2025.3559573.

[4] T. Medeiros, M. Medeiros, M. Andrade, M. Silva, I. Silva, M. Gaffurini, et al., "Tailoring RAG Strategies for Industrial Protocols: A Comparative Study on PROFIBUS Document Retrieval using Gemma and GPT Models", *IEEE International Conference on Emerging Technologies and Factory Automation, ETFA*, 2025, doi: 10.1109/ETFA65518.2025.11205618.

[5] E. Sisinni, A. Depari, A. Flammini, S. Rinaldi, and P. Ferrari, "Evaluating the Joint Use of LoRaWAN and Bluetooth Mesh to Improve Survivability for Critical Sensor Applications", *IEEE Sensors Journal*, vol. 24, no. 14, pp. 22992 - 23003, 2024, doi: 10.1109/JSEN.2024.3403308.

[6] M. Gaffurini, P. Bellagente, A. Depari, A. Flammini, D. Brandao, S. Rinaldi, et al., "On computing and real-time communication performance of containerized virtual PLCs", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, 2024, doi: 10.1109/WFCS60972.2024.10540795.

[7] P. Ferrari, P. Bellagente, A. Flammini, M. Gaffurini, S. Rinaldi, E. Sisinni, et al., "Anomaly Detection in Industrial Networks using Distributed Observation of Statistical Behavior", *2024 IEEE International Workshop on Metrology for Industry 4.0 and IoT, MetroInd4.0 and IoT 2024 - Proceedings*, pp. 180 - 185, 2024, doi: 10.1109/MetroInd4.0IoT61288.2024.10584236.

[8] G. S. Sestito, A. C. Turcato, A. L. Dias, P. Ferrari, and M. M. da Silva, "Versatile unsupervised anomaly detection method for RTE-based networks", *Expert Systems with Applications*, vol. 206, 2022, doi: 10.1016/j.eswa.2022.117751.

[9] P. Ferrari, E. Sisinni, P. Bellagente, A. Depari, A. Flammini, M. Pasetti, et al., "Improving classification capability of industrial-grade ATE by means of cloud architecture", *Conference Record - IEEE Instrumentation and Measurement Technology Conference*, 2022, doi: 10.1109/I2MTC48687.2022.9806548.

[10] G. S. Sestito, A. C. Turcato, A. L. Dias, P. Ferrari, and M. M. da Silva, "Evaluating real-time ethernet performance indicators for SERCOS III networks", *2021 14th IEEE International Conference on Industry Applications, INDUSCON 2021 - Proceedings*, pp. 1191 - 1197, 2021, doi: 10.1109/INDUSCON51756.2021.9529676.

[11] G. S. Sestito, A. C. Turcato, A. L. Dias, P. Ferrari, D. H. Spatti, and M. M. da Silva, "A general optimization-based approach to the detection of real-time Ethernet traffic events", *Computers in Industry*, vol. 128, 2021, doi: 10.1016/j.compind.2021.103413.

[12] M. Pasetti, P. Ferrari, P. Bellagente, E. Sisinni, A. O. De Sa, C. B. D. Prado, et al., "Artificial Neural Network-Based Stealth Attack on Battery Energy Storage Systems", *IEEE Transactions on Smart Grid*, vol. 12, no. 6, pp. 5310 - 5321, 2021, doi: 10.1109/TSG.2021.3102833.

[13] P. Ferrari, E. Sisinni, P. Bellagente, S. Rinaldi, M. Pasetti, A. O. De Sa, et al., "Model-Based Stealth Attack to Networked Control System Based on Real-Time Ethernet", *IEEE Transactions on Industrial Electronics*, vol. 68, no. 8, pp. 7672 - 7683, 2021, doi: 10.1109/TIE.2020.3001850.

[14] A. C. Turcato, A. L. Dias, G. S. Sestito, R. Flauzino, D. Brandao, E. Sisinni, et al., "Introducing a cloud based architecture for the distributed analysis of Real-Time Ethernet traffic", *2020 IEEE International Workshop on Metrology for Industry 4.0 and IoT, MetroInd 4.0 and IoT 2020 - Proceedings*, pp. 235 - 240, 2020, doi: 10.1109/MetroInd4.0IoT48571.2020.9138288.

[15] E. Sisinni, P. Ferrari, D. Fernandes Carvalho, S. Rinaldi, P. Marco, A. Flammini, et al., "LoRaWAN Range Extender for Industrial IoT", *IEEE Transactions on Industrial Informatics*, vol. 16, no. 8, pp. 5607 - 5616, 2020, doi: 10.1109/TII.2019.2958620.

[16] P. Ferrari, E. Sisinni, A. Depari, A. Flammini, S. Rinaldi, P. Bellagente, et al., "Evaluation of the impact of Cloud Database services on Industrial IoT Applications", *I2MTC 2020 - International Instrumentation and Measurement Technology Conference, Proceedings*, 2020, doi: 10.1109/I2MTC43012.2020.9129080.

[17] P. Ferrari, E. Sisinni, A. Depari, A. Flammini, S. Rinaldi, P. Bellagente, et al., "On the performance of cloud services and databases for industrial IoT scalable applications", *Electronics (Switzerland)*, vol. 9, no. 9, pp. 1 - 17, 2020, doi: 10.3390/electronics9091435.

[18] P. Ferrari, E. Sisinni, A. Saifullah, R. MacHado, A. De Sa, and M. Felser, "Work-in-Progress: Compromising Security of Real-time Ethernet Devices by means of Selective Queue Saturation Attack", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, vol. 2020-April, 2020, doi: 10.1109/WFCS47810.2020.9114505.

[19] P. Ferrari, P. Bellagente, A. Depari, A. Flammini, M. Pasetti, S. Rinaldi, et al., "Evaluation of the impact on industrial applications of NTP Used by IoT devices", *2020 IEEE International Workshop on Metrology for Industry 4.0 and IoT, MetroInd 4.0 and IoT 2020 - Proceedings*, pp. 223 - 228, 2020, doi: 10.1109/MetroInd4.0IoT48571.2020.9138290.

[20] F. Bonafini, A. Depari, P. Ferrari, A. Flammini, M. Pasetti, S. Rinaldi, et al., "Exploiting localization systems for LoRaWAN transmission scheduling in industrial applications", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, vol. 2019-May, 2019, doi: 10.1109/WFCS.2019.8757999.

[21] M. S. Rocha, G. S. Sestito, A. L. Dias, A. C. Turcato, D. Brandão, and P. Ferrari, "On the performance of OPC UA and MQTT for data exchange between industrial plants and cloud servers", *Acta IMEKO*, vol. 8, no. 2, pp. 80 - 87, 2019, doi: 10.21014/acta_imeko.v8i2.648.

[22] P. Ferrari, S. Rinaldi, E. Sisinni, F. Colombo, F. Ghelfi, D. Maffei, et al., "Performance evaluation of full-cloud and edge-cloud architectures for Industrial IoT anomaly detection based on deep learning", *2019 IEEE International Workshop on Metrology for Industry 4.0 and IoT, MetroInd 4.0 and IoT 2019 - Proceedings*, pp. 420 - 425, 2019, doi: 10.1109/METROI4.2019.8792860.

[23] S. Rinaldi, P. Bellagente, P. Ferrari, A. Flammini, and E. Sisinni, "Are cloud services aware of time? an experimental analysis oriented to industry 4.0", *IEEE International Symposium on Precision Clock Synchronization for Measurement, Control, and Communication, ISPCS*, vol. 2019-September, 2019, doi: 10.1109/ISPCS.2019.8886642.

[24] E. Sisinni, D. F. Carvalho, P. Ferrari, A. Flammini, D. R. C. Silva, and I. M. D. Da Silva, "Enhanced flexible LoRaWAN node for industrial IoT", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, vol. 2018-June, pp. 1 - 4, 2018, doi: 10.1109/WFCS.2018.8402367.

[25] G. S. Sestito, A. C. Turcato, A. L. Dias, M. S. Rocha, M. M. Da Silva, P. Ferrari, et al., "A method for anomalies detection in real-time ethernet data traffic applied to PROFINET", *IEEE Transactions on Industrial Informatics*, vol. 14, no. 5, pp. 2171 - 2180, 2018, doi: 10.1109/TII.2017.2772082.

[26] G. S. Sestito, A. L. Dias, A. C. Turcato, D. Brandao, and P. Ferrari, "The panorama and challenges of PROFIBUS technology in brazilian market", *2018 13th IEEE International Conference on Industry Applications, INDUSCON 2018 - Proceedings*, pp. 692 - 697, 2018, doi: 10.1109/INDUSCON.2018.8627204.

[27] P. Bellagente, A. Depari, P. Ferrari, A. Flammini, E. Sisinni, and S. Rinaldi, "M3IoT - Message-oriented middleware for M-health Internet of Things: Design and validation", *I2MTC 2018 - 2018 IEEE International Instrumentation and Measurement Technology Conference: Discovering New Horizons in Instrumentation and Measurement, Proceedings*, pp. 1 - 6, 2018, doi: 10.1109/I2MTC.2018.8409656.

[28] P. Bellagente, F. Bonafini, C. Crema, A. Depari, P. Ferrari, A. Flamrnini, et al., "Distributed Human Machine Interface with Localization Functionalities: A Real Test Bench", *2018 Workshop on Metrology for Industry 4.0 and IoT, MetroInd 4.0 and IoT 2018 - Proceedings*, pp. 46 - 51, 2018, doi: 10.1109/METROI4.2018.8439039.

[29] P. Ferrari, A. Flammini, E. Sisinni, S. Rinaldi, D. Brandao, and M. S. Rocha, "Delay Estimation of Industrial IoT Applications Based on Messaging Protocols", *IEEE Transactions on Instrumentation and Measurement*, vol. 67, no. 9, pp. 2188 - 2199, 2018, doi: 10.1109/TIM.2018.2813798.

[30] P. Ferrari, A. Flammini, S. Rinaldi, E. Sisinni, D. Maffei, and M. Malara, "Evaluation of Communication Delay in IOT Applications Based on OPC UA", *2018 Workshop on Metrology for Industry 4.0 and IoT, MetroInd 4.0 and IoT 2018 - Proceedings*, pp. 224 - 229, 2018, doi: 10.1109/METROI4.2018.8428346.

[31] P. Ferrari, A. Flammini, S. Rinaldi, E. Sisinni, D. Maffei, and M. Malara, "Impact of quality of service on cloud based industrial IoT applications with OPC UA", *Electronics (Switzerland)*, vol. 7, no. 7, 2018, doi: 10.3390/electronics7070109.

[32] M. Rizzi, P. Ferrari, A. Flammini, and E. Sisinni, "Evaluation of the IoT LoRaWAN Solution for Distributed Measurement Applications", *IEEE Transactions on Instrumentation and Measurement*, vol. 66, no. 12, pp. 3340 - 3349, 2017, doi: 10.1109/TIM.2017.2746378.

[33] M. Rizzi, P. Ferrari, A. Flammini, E. Sisinni, and M. Gidlund, "Using LoRa for industrial wireless networks", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, 2017, doi: 10.1109/WFCS.2017.7991972.

[34] P. Ferrari, A. Flammini, M. Rizzi, E. Sisinni, and M. Gidlund, "On the evaluation of LoRaWAN virtual channels orthogonality for dense distributed systems", *2017 IEEE International Workshop on Measurement and Networking, M and N 2017 - Proceedings*, 2017, doi: 10.1109/IWMN.2017.8078371.

[35] P. Ferrari, E. Sisinni, D. Brandão, and M. Rocha, "Evaluation of communication latency in industrial IoT applications", *2017 IEEE International Workshop on Measurement and Networking, M and N 2017 - Proceedings*, 2017, doi: 10.1109/IWMN.2017.8078359.

[36] F. A. Fernandes, G. S. Sestito, A. L. Dias, D. Brandão, and P. Ferrari, "Influence of network parameters on the recovery time of a ring topology PROFINET network", *IFAC-PapersOnLine*, vol. 49, no. 30, pp. 278 - 283, 2016, doi: 10.1016/j.ifacol.2016.11.141.

[37] M. Felser, P. Ferrari, and A. Flammini, "PROFINET", *Industrial Communication Systems*, pp. 40, 2016, Available: https://www.scopus.com/pages/publications/85051448972?origin=resultslist.

[38] P. Bellagente, P. Ferrari, A. Flammini, S. Rinaldi, and E. Sisinni, "Enabling PROFINET devices to work in IoT: Characterization and requirements", *Conference Record - IEEE Instrumentation and Measurement Technology Conference*, vol. 2016-July, 2016, doi: 10.1109/I2MTC.2016.7520417.

[39] P. Ferrari, A. Flammini, S. Rinaldi, M. Rizzi, E. Sisinni, and G. Prytz, "On the use of multiple MAC registration protocol in industrial networks", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, vol. 2015-July, 2015, doi: 10.1109/WFCS.2015.7160546.

[40] S. Rinaldi, P. Ferrari, N. M. Ali, and F. Gringoli, "IEC 61850 for micro grid automation over heterogeneous network: Requirements and real case deployment", *Proceeding - 2015 IEEE International Conference on Industrial Informatics, INDIN 2015*, pp. 923 - 930, 2015, doi: 10.1109/INDIN.2015.7281859.

[41] D. Fontanelli, D. Macii, S. Rinaldi, P. Ferrari, and A. Flammini, "A servo-clock model for chains of transparent clocks affected by synchronization period jitter", *IEEE Transactions on Instrumentation and Measurement*, vol. 63, no. 5, pp. 1085 - 1095, 2014, doi: 10.1109/TIM.2013.2286871.

[42] D. Fontanelli, D. Macii, S. Rinaldi, P. Ferrari, and A. Flammini, "Performance analysis of a clock state estimator for PROFINET IO IRT synchronization", *Conference Record - IEEE Instrumentation and Measurement Technology Conference*, pp. 1828 - 1833, 2013, doi: 10.1109/I2MTC.2013.6555730.

[43] P. Ferrari, A. Flammini, S. Rinaldi, and G. Prytz, "High availability IEEE 1588 nodes over IEEE 802.1aq Shortest Path Bridging networks", *IEEE International Symposium on Precision Clock Synchronization for Measurement, Control, and Communication, ISPCS*, pp. 35 - 40, 2013, doi: 10.1109/ISPCS.2013.6644760.

[44] P. Ferrari, A. Flammini, S. Rinaldi, E. Sisinni, and A. Vezzoli, "Toward smart metering application exploiting IPv6 over wM-bus", *2013 IEEE Workshop on Environmental, Energy and Structural Monitoring Systems, EESMS 2013 - Proceedings*, 2013, doi: 10.1109/EESMS.2013.6661706.

[45] P. Ferrari, A. Flammini, S. Rinaldi, E. Sisinni, and G. Prytz, "Advanced networks for distributed measurement in substation automation systems", *2013 IEEE International Workshop on Applied Measurements for Power Systems, AMPS 2013 - Proceedings*, pp. 108 - 113, 2013, doi: 10.1109/amps.2013.6656235.

[46] D. D. Giustina, P. Ferrari, A. Flammini, and S. Rinaldi, "Experimental characterization of service latency over Broadband Power Line in Medium Voltage grid", *2012 IEEE International Workshop on Applied Measurements for Power Systems, AMPS 2012 Proceedings*, pp. 149 - 154, 2012, doi: 10.1109/AMPS.2012.6343994.

[47] H. A. Cozzetti, D. Brevi, R. Scopigno, P. Ferrari, E. Sisinni, and A. Flammini, "MS-Aloha: Preliminary analysis of its suitability for wireless automation", *IEEE International Conference on Emerging Technologies and Factory Automation, ETFA*, 2012, doi: 10.1109/ETFA.2012.6489555.

[48] P. Ferrari, A. Flammini, S. Rinaldi, and G. Prytz, "Mixing Real Time Ethernet traffic on the IEC 61850 Process bus", *IEEE International Workshop on Factory Communication Systems - Proceedings, WFCS*, pp. 153 - 156, 2012, doi: 10.1109/WFCS.2012.6242559.

[49] M. Felser, P. Ferrari, and A. Flammini, "PROFINET", *The Industrial Electronics Handbook - Five Volume Set*, pp. 40 - 1, 2011, Available: https://www.scopus.com/pages/publications/85131466524.

[50] P. Ferrari, A. Flammini, F. Venturini, and A. Augelli, "Large PROFINET IO RT networks for factory automation: A case study", *IEEE International Conference on Emerging Technologies and Factory Automation, ETFA*, 2011, doi: 10.1109/ETFA.2011.6059160.

[51] P. Ferrari, A. Flammini, S. Rinaldi, and G. Prytz, "Applying PTP-to-SNTP time-gateway to IEC61850 systems", *IEEE International Conference on Emerging Technologies and Factory Automation, ETFA*, 2011, doi: 10.1109/ETFA.2011.6059153.





