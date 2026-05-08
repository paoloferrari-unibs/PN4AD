# PN4AD  
## PROFINET for Automotive Dataset (PN4AD)

PN4AD, **PROFINET for Automotive Dataset**, is a dataset derived from industrial PROFINET network validation activities performed in automotive production environments.

The dataset is intended to support research on industrial communication networks, PROFINET-based automation systems, network validation procedures, and data-driven analysis of industrial Ethernet infrastructures.

This release currently includes a .csv file containing anonymized plant- and line-level validation information. 

NOTE:Raw packet capture files are not distributed due to non-disclosure agreements and industrial confidentiality constraints.

---

## Repository Content

The current release contains:

```text
PN4AD/
├── README.md
└── LineInformation.csv
```

The Excel file contains anonymized statistical and validation metadata extracted from PROFINET network validation procedures.

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

## Related Scientific Articles

Related publications:

1. [To be added]
2. [To be added]
3. [To be added]

---

## Data Availability

While raw pcap files are restricted by non-disclosure agreements, the authors are committed to scientific transparency. The derived database, containing all anonymized statistical features and validation labels described in the related scientific work, is available upon request to facilitate benchmarking and collaborative research.

---

## License

The source specifies that the data can be used as is without any warranty. 
Current status: **license to be defined**.

---

## Citation

If you use PN4AD in your research, please cite the related scientific article.

```bibtex
@article{pn4ad,
  title   = {To be added},
  author  = {To be added},
  journal = {To be added},
  year    = {To be added},
  doi     = {To be added}
}
```

---

## Contact

For questions, collaboration requests, or access to additional derived data, please contact:

```text
Name: To be added
Institution: To be added
Email: To be added
```
