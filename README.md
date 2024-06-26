# Welfare Expectations Across U.S. Economic Cycles
## Analysis of the the American public's views on government provision of benefits under different economic conditions over the past 50 years

## Overview

This paper investigates how economic conditions have influenced public views on government welfare over fifty years. It questions whether public expectations for welfare match the economic cycles. The study uses the General Social Survey (GSS) Welfare data to explore American public opinion on welfare adequacy during economic fluctuations.

Findings indicate that public welfare preferences vary with the economy—decreasing during growth periods and intensifying during recessions. The research also uncovers that welfare expectations differ significantly across income groups, highlighting the need for nuanced welfare policies.

The study emphasizes that welfare policies should be adaptable to economic changes and sensitive to diverse societal needs, aiming for equitable welfare strategies that align with economic realities.

## File Structure

The repo is structured as:

-   `data/raw_data` contains the raw data as obtained from GSS.
-   `data/analysis_data` contains the cleaned dataset that was constructed.
-   `model` contains fitted models. 
-   `other` contains relevant literature, details about LLM chat interactions, and sketches.
-   `paper` contains the files used to generate the paper, including the Quarto document and reference bibliography file, as well as the PDF of the paper. 
-   `scripts` contains the R scripts used to simulate, download and clean data.

## Statement on Parquet File

When the author tried to complete the conversion of cleaned_data into parquet format, he encountered a problem that was difficult to fix. The specific error code is as follows:

> Error in parquet___arrow___ArrowReaderProperties__Make(isTRUE(use_threads)) :
   Cannot call parquet___arrow___ArrowReaderProperties__Make(). See https://arrow.apache.org/docs/r/articles/install.html for help installing Arrow C++ libraries.

The arrow package is an interface to the Apache Arrow C++ libraries, and Parquet is a columnar storage file format that is optimized for use with data analysis tools. The error message Cannot call parquet___arrow___ArrowReaderProperties__Make() specifically means that the R session tried to execute a function related to reading Parquet files but failed because it couldn't find the necessary underlying Arrow C++ library functions.

## Statement on LLM usage

- `inputs/llm/usage.text` The ChatGPT-4 language model was utilized in authoring this report to garner insights and recommendations for addressing issues within the GSS welfare dataset. ChatGPT-4 offered the author various indicators that aid in identifying problems and potential solutions influenced by model trends (refer to usage.txt for detailed information); these insights prompted the author to include certain third-party journal research in the present paper as supplemental empirical evidence to bolster the conclusions drawn from the welfare analysis. Additionally, ChatGPT-4 contributed suggestions for grammatical and structural refinements to the content of the paper, enhancing clarity and brevity.


## Access to GSS Data

Licensing and copyright constraints prevent the direct inclusion of the raw General Social Survey (GSS) data within this repository. The GSS data is crucial for the replication of the analyses conducted in our study. Below, we provide comprehensive instructions on how to acquire the data straight from the original source to aid in obtaining the datasets necessary for replication.

Step 1: Navigate to the GSS Website

Access to the GSS data is provided by NORC at the University of Chicago. Begin by going to the GSS website: https://gssdataexplorer.norc.org/variables/4/vshow.

Step 2: Sign Up for Access

You will likely need to create an account to download the GSS data. This simple registration process promotes the data's responsible utilization. Adhere to the registration guidelines available on the GSS website.

Step 3: Identify the Appropriate Datasets

Post-registration, the datasets become accessible. For our study, we used the "number of hours worked last week" data, covering the period from 1972 to 2022. The GSS website's search and filtering tools can assist you in pinpointing the exact datasets you need.

Step 4: Obtain the Data

Once you have found the datasets you need, you are ready to download them. The GSS website allows you to download data in a range of formats. Select the format that best suits the analysis software you plan to use.

Step 5: Consult the Codebook

The GSS includes a detailed codebook that explains each variable and its coding scheme. To fully comprehend the dataset's structure, variables, and any temporal changes that could influence your analysis, it is crucial to consult the codebook.

Responsible Data Use

It is imperative to use the GSS data in line with NORC's specified terms and conditions. Typically, this involves employing the data exclusively for scholarly research and crediting the GSS as required in your scholarly outputs.
