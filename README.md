# Completion Rate Decline Analysis: Investigating Viewership Drop-Off on weather.com

This project examines patterns behind declining video completion rates on weather.com, aiming to identify potential platform-specific, content-specific, or behavioral factors contributing to audience drop-off.

---

## 📌 Purpose

The project has three primary objectives:

- **Explore Completion Rate Trends:** Understand current state of completion rate across platforms and forms of content
- **Draw User Insights:** Find strongest correlating variables that have effected completion rates in this target period
- **Support Editorial and Platform Strategy:** Provide data-driven insight to optimize video content performance across platforms.

---

## 🔬 Research Foundation

This analysis builds upon platform-sourced behavioral metrics from Amplitude, including completion rates, video views, and watched ads, segmented by platform (Desktop, iOS, Android, etc.). It aims to pinpoint underperforming conditions or patterns through time-based and categorical trends.

---

## 🧪 Methodology

- **Amplitude Data Processing:** Imported multiple Amplitude exports, merged them by video title or UUID, and computed platform-specific completion rates
- **CMS Metadata Integration:** Used regex to extract `uuid` values from CMS URLs, merged CMS metadata with Amplitude metrics, parsed, and reformatted publish dates.
- **Collection Extraction:** Parsed the content type (e.g., “science”, “news”, “forecast”) from the structure of the `Live Link` URL using regex and mapped it into a new `Collection` column.
- **Monthly Platform Averages:** Grouped videos by month and platform to compute average platform-level completion rates. These were used to normalize performance.
- **Content Score Calculation:** Created a `Content Score` metric for each video by summing its completion rates across platforms, each weighted relative to that platform’s monthly average.
- **Daypart Alignment:** Compared the hour each video was published (`Publish Hour`) to the average hour of peak performance for its content type to assess whether timing aligned with viewer behavior.
- **Visualization & Debugging:** Created histograms, bar plots, and scatter plots to visualize trends in drop-off rate by platform, hour, and content type. Also displayed outliers and edge cases for editorial review.

---

## 📚 Report

- Link to report can be found [here]([url](https://docs.google.com/presentation/d/1Sbhys5O0SUExWZO2iokIri_KX7Wi_I0gig7uRK5Ufk0/edit?usp=sharing))

---

## 📂 Repository Structure

- `Completion Rate Decline Analysis.ipynb`: Contains the full analysis in Jupyter format.
- `requirements.txt`: Requirements file to download all imbedded libraries and tools.

---

## 🔧 Requirements

To run this project:

```bash
pip install -r requirements.txt
