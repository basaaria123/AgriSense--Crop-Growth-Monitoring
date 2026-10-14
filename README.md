# 🌱 AgriSense — AIoT Crop Growth Monitoring

**An intelligent crop growth monitoring and anomaly detection system for Tomato, Marigold, and Mint.**

AgriSense is an agricultural technology project that aims to monitor crop growth, identify abnormal growth patterns, and help farmers make timely, data-driven decisions. The project focuses on combining crop growth data, environmental information, and future IoT sensor integration with machine learning to support smarter crop management.

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [Crops Covered](#-crops-covered)
- [Repository Contents](#-repository-contents)
- [Understanding the Datasets](#-understanding-the-datasets)
- [Proposed System Workflow](#-proposed-system-workflow)
- [Growth Monitoring Parameters](#-growth-monitoring-parameters)
- [Machine Learning Approach](#-machine-learning-approach)
- [Technology Stack](#-technology-stack)
- [Future Implementation](#-future-implementation)
- [Limitations](#-limitations)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)

## 🌾 Project Overview

Farmers may not notice abnormal crop growth until visible damage or reduced productivity occurs. Regularly measuring plant growth and monitoring environmental conditions can help identify potential problems earlier.

AgriSense aims to address this challenge by developing a smart crop growth monitoring system for three crops:

- 🍅 **Tomato:** Monitoring plant development and identifying deviations from expected growth patterns.
- 🌼 **Marigold:** Tracking growth progression and detecting unusual changes in plant development.
- 🌿 **Mint:** Monitoring plant growth and identifying abnormal growth patterns.

The proposed system will use structured datasets as a foundation for developing growth analysis and anomaly detection models. In a future implementation, IoT sensors and periodic plant measurements may provide additional information about actual growing conditions.

## 🎯 Objectives

1. Collect and organize crop-specific growth-monitoring data.
2. Study growth patterns for tomato, marigold, and mint.
3. Identify unusual growth measurements and potential growth anomalies.
4. Explore the relationship between environmental conditions and crop development.
5. Develop machine learning models for growth analysis when sufficient suitable data is available.
6. Integrate IoT sensors for continuous environmental monitoring in a future implementation.
7. Provide understandable growth status information and alerts to support agricultural decisions.

## 🌿 Crops Covered

| Crop | Monitoring focus |
|---|---|
| Tomato | Plant height, leaf development, and growth progression |
| Marigold | Plant height, leaf development, and overall growth progression |
| Mint | Plant height, leaf development, and overall growth progression |

The actual parameters available for each crop depend on the corresponding dataset and its recorded columns.

## 📂 Repository Contents

The repository currently contains the following dataset files.

| File | Purpose |
|---|---|
| [AgriSense Marigold Growth Monitoring Datasets](AgriSense_Marigold_Growth_Monitoring_Datasets.xlsx) | Workbook for marigold growth-monitoring data |
| [Tomato AgriSense Crop Growth Monitoring Datasets](Tomato%20AgriSense_Crop_Growth_Monitoring_Datasets.xlsx) | Workbook for tomato growth-monitoring data |
| [AgriSense Synthetic Growth Datasets](AgriSense_Synthetic_Growth_Datasets.zip) | ZIP archive containing synthetic growth datasets |
| [Tomato, Marigold and Mint Workbook](tomato%2C%20marigold%2C%20mint.xlsx) | Combined workbook covering the three target crops |

All file links above point to files within this GitHub repository.

**Note:** These files are dataset resources, not necessarily trained machine learning models or a complete running application.

## 📊 Understanding the Datasets

The repository organizes data resources for crop growth monitoring. Each dataset should be examined to identify its source, variables, measurement units, sample count, and intended use.

### 1. Crop-specific growth datasets

The tomato and marigold workbooks provide crop-specific resources for investigating plant growth. Their suitability for model training depends on the actual columns, observations, and labels they contain.

### 2. Combined crop workbook

The combined workbook covers tomato, marigold, and mint. It may help the team organize and compare crop-specific information, provided the underlying data is sufficiently consistent.

### 3. Synthetic growth datasets

Synthetic data is artificially generated rather than directly measured from real plants. It can help with initial development, testing data-processing pipelines, and experimenting with model architectures.

However, synthetic data should not be treated as proof of real-world model accuracy. Models trained on it should eventually be validated using independently collected real-world observations.

### Dataset verification checklist

Before using any workbook for training, verify:

- The dataset's original source and license.
- Whether the records are real, synthetic, or a mixture.
- Which crops and growth stages are represented.
- Whether observations are recorded over time.
- The meanings and units of the columns.
- Whether missing values, duplicates, or inconsistent records exist.
- Whether growth labels or anomaly labels are provided.
- Whether the data is sufficient for the intended prediction task.

## 🔄 Proposed System Workflow

The intended AgriSense workflow is:

1. **Data collection:** Obtain crop growth measurements and relevant environmental readings.
2. **Data preprocessing:** Clean the datasets, standardize units, handle missing values, and validate records.
3. **Growth analysis:** Analyze changes in growth measurements across available observations.
4. **Anomaly detection:** Identify unusual measurements or growth patterns compared with suitable baselines.
5. **Environmental analysis:** Investigate whether temperature, humidity, soil moisture, or other variables are associated with observed growth changes.
6. **Growth status generation:** Present results as understandable growth indicators.
7. **Future IoT integration:** Collect sensor readings and send them to the monitoring application.
8. **Dashboard and alerts:** Display measurements, trends, and potential anomalies for users.

**Important:** This is the proposed workflow. Its implementation depends on the availability of suitable data, sensors, trained models, and application code.

## 📏 Growth Monitoring Parameters

The following parameters are candidates for future monitoring. They should not be assumed to exist in every current dataset.

| Parameter | Purpose |
|---|---|
| Plant height | Track vertical growth over time |
| Number of leaves | Measure leaf development |
| Leaf size | Examine changes in leaf development |
| Stem thickness | Track stem development where measurements are available |
| Days after planting | Compare observations by plant age |
| Soil moisture | Assess the water conditions around the plant |
| Temperature | Monitor environmental temperature |
| Relative humidity | Monitor atmospheric moisture |
| Light intensity | Study light availability |
| Soil pH | Record soil acidity or alkalinity where measured |

Different crops may require different monitoring parameters and suitable reference ranges.

## 🤖 Machine Learning Approach

The project may explore the following methods, depending on the dataset structure and available labels.

### Growth trend analysis

Compare measurements across observation dates to estimate changes in plant development.

### Supervised prediction

If sufficient labeled observations are available, regression models can estimate numerical growth measurements, while classification models can predict defined growth categories.

### Anomaly detection

If reliable anomaly labels are unavailable, methods such as Isolation Forest or other unsupervised approaches may be investigated. Their outputs require validation before being interpreted as genuine crop problems.

### Model evaluation

Model evaluation should use appropriate metrics and a validation strategy that avoids leakage between related observations. Where records come from the same plants over time, observations from a plant should not be indiscriminately split between training and testing sets.

No model accuracy or performance claim should be made until it has been measured on suitable held-out data.

## 🛠️ Technology Stack

The following technologies are potential components of the proposed implementation.

| Component | Candidate technology |
|---|---|
| Dataset processing | Python, Pandas, NumPy |
| Data visualization | Matplotlib |
| Machine learning | Scikit-learn |
| Data storage | CSV, Excel, or a suitable database |
| IoT hardware | ESP32 and compatible environmental sensors |
| Backend | Python with Flask or FastAPI |
| Dashboard | Web-based monitoring interface |

These are proposed implementation choices, not a claim that all components are already implemented in this repository.

## 🚀 Future Implementation

The project can be developed incrementally:

- [ ] Verify and document the sources of all datasets.
- [ ] Inspect the columns and sample records in each workbook.
- [ ] Separate real observations from synthetic records.
- [ ] Standardize growth measurements and units.
- [ ] Develop exploratory data analysis and growth trend visualizations.
- [ ] Establish baseline growth patterns for each crop.
- [ ] Develop and evaluate a suitable anomaly detection model.
- [ ] Integrate IoT sensors for environmental data collection.
- [ ] Develop a dashboard to display growth trends and potential anomalies.
- [ ] Validate the system using real observations collected under practical growing conditions.

## ⚠️ Limitations

- The presence of a crop name in a dataset does not guarantee that it contains sufficient growth measurements for that crop.
- Synthetic datasets may not represent actual growing conditions.
- Growth anomalies do not necessarily indicate a specific disease, pest, or nutrient deficiency.
- Environmental readings alone may not explain every change in plant growth.
- Reliable model evaluation requires suitable data, clearly defined targets, and independent validation.
- Disease detection is a separate task that generally requires appropriately labeled disease observations or images.

AgriSense should therefore distinguish between **growth monitoring, growth anomaly detection, and disease detection** rather than treating them as the same capability.

## 📁 Project Structure

```text
AgriSense--Crop-Growth-Monitoring/
│
├── README.md
│
├── AgriSense_Marigold_Growth_Monitoring_Datasets.xlsx
│
├── Tomato AgriSense_Crop_Growth_Monitoring_Datasets.xlsx
│
├── AgriSense_Synthetic_Growth_Datasets.zip
│
└── tomato, marigold, mint.xlsx
```

This structure reflects the dataset files currently listed in the repository. Additional directories for preprocessing scripts, trained models, sensor integration, and dashboard development may be added as implementation progresses.

## 🤝 Contributing

Contributions are welcome as the project develops.

1. Review the existing dataset files.
2. Document dataset sources and licenses.
3. Keep real and synthetic data clearly identified.
4. Use consistent column names and measurement units.
5. Document preprocessing and model evaluation procedures.
6. Avoid publishing unsupported accuracy claims.
7. Submit improvements through GitHub branches and pull requests.

## 📄 License and Dataset Attribution

Before redistributing datasets or using them in a public deployment, verify the applicable licenses and attribution requirements for each source. The presence of a dataset in this repository does not, by itself, establish permission to redistribute it.

## 🌱 Project Vision

AgriSense aims to combine crop growth data, anomaly detection, and future IoT integration to support earlier identification of abnormal growth patterns and more informed crop management decisions.

**Smarter monitoring. Earlier insights. Better-informed farming.**
