# Wheat Detection and Other Extraction of Qualified Data 🌾

![Workflow](https://user-images.githubusercontent.com/31928447/117530943-9c085f80-afe8-11eb-846c-af664f6b72ec.png)
*The image above depicts the general workflow of the project, from data acquisition to analysis.*

## Overview
This project focuses on the detection of wheat spikes from optical images using machine learning and image processing techniques. The primary goal is to extract valuable information such as spike density, maturity, and overall health of wheat crops. This data can aid farmers in monitoring their fields, making informed decisions to mitigate losses, and ultimately improving wheat yield and quality.

## Problem Statement
Wheat is a critical global food source, and its demand is continuously rising with the growing world population. However, maximizing wheat yield is challenging. Traditional methods of monitoring large wheat fields are often labor-intensive and may not provide timely insights into crop health. Delays in identifying issues like diseases, nutrient deficiencies, or maturity variations can lead to significant production losses. This project aims to address these challenges by providing an automated way to analyze wheat crops.

## Solution
The core of this project is a system built to analyze optical images of wheat fields. The methodology involves:
*   **Machine Learning:** An object detection model, specifically EfficientDet-D4, is trained to identify and locate wheat spikes within images.
*   **Image Processing:** Various techniques are employed to enhance image quality and prepare data for the model and subsequent analysis.
*   **Data Extraction:** The system aims to extract key metrics such as spike density, estimate maturity levels, and derive basic health indicators from the processed images and detected spikes.

## Features
The project incorporates several key steps and techniques:

*   **Image Augmentation:** To improve model robustness and performance, various image augmentation techniques are applied to the training dataset, including:
    *   Crop
    *   Rotate
    *   Flip
    *   Mixup
    *   Mosaic
    *   Hue adjustments
    *   Gaussian Noise
*   **Machine Learning Model:**
    *   Algorithm: EfficientDet-D4 is utilized for its efficiency and accuracy in object detection tasks, specifically for detecting wheat spikes.
*   **Model Training Methodology:**
    *   The EfficientDet-D4 model was trained using various normalization techniques, with sequential normalization being selected for the final model.
*   **Image Processing:**
    *   The Chale histogram method is applied to optimize image contrast and quality, enhancing the visibility of features relevant for analysis.
*   **Analytical Approach:**
    *   By leveraging the outputs of the object detection model, various analytical approaches are suggested to extract basic information and insights from the images.

## Dataset
The project utilizes optical images of wheat fields as its primary dataset. These images are processed and used to train the machine learning model for wheat spike detection. *(Further details about the dataset, such as source, resolution, and size, can be found in the referenced Kaggle notebooks.)*

## Installation
1.  Clone the repository:
    ```bash
    git clone https://github.com/username/repository-name.git # Replace with the actual repository URL
    cd repository-name
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
    *Note: The `requirements.txt` file lists necessary Python packages. Ensure you have Python and pip installed.*

## Usage
The primary workflows, including model training, data analysis, and reporting, are conducted within Jupyter Notebooks. Please refer to the following Kaggle notebooks for detailed implementation:

*   **Training & Model Implementation**: [Jupyter Notebook Workspace for Train](https://www.kaggle.com/shemskurtoglu/wheat-tpu-tfkeras-00?scriptVersionId=52800232) (this notebook also includes model weights)
*   **Summary Report**: [Jupyter Notebook Workspace for Final Report](https://www.kaggle.com/shemskurtoglu/wheat-summary-report)

## Results
The machine learning model developed in this study demonstrates promising performance, achieving mean Average Precision (mAP) values generally greater than 0.5 for wheat spike detection. This indicates a successful foundational model. To further enhance the stability and accuracy of the model, future work includes applying additional image processing techniques and conducting more training iterations. The insights derived from the model's outputs, using analytical approaches, can provide valuable health information about wheat plants to users and producers.

## Contributing
We welcome contributions to enhance this project! Please follow these steps:
1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes and improvements.
4.  Commit your changes (`git commit -m 'Add some feature'`).
5.  Push to the branch (`git push origin feature/your-feature-name`).
6.  Open a Pull Request for review.

## License
This project is licensed under the terms of the [LICENSE](./LICENSE) file.

## Acknowledgements & Links
*   This project is based on the original research and notebooks developed by [Shems Kurtoglu on Kaggle](https.www.kaggle.com/shemskurtoglu).
*   **Kaggle Notebooks:**
    *   [Wheat TPU TF Keras (Training Notebook)](https://www.kaggle.com/shemskurtoglu/wheat-tpu-tfkeras-00?scriptVersionId=52800232)
    *   [Wheat Summary Report (Final Report Notebook)](https://www.kaggle.com/shemskurtoglu/wheat-summary-report)

## Turkish Abstract (ÖZET)
Bu çalışmamızda buğday başaklarının takibini yapılarak sağlıklı gelişim süreci sağlanması için optik görüntülerden başak yoğunluğu, olgunluk ve temel sağlık bilgilerinin çıkarımı hedeflenmektedir. Bu amaçla görüntü işleme ve makine öğrenimi metotları kullanılarak buğday fotoğraflarından temel sağlık verileri elde edilmesi amaçlanmaktadır. Bu veriler buğday üreticisinin üretim sürecindeki kayıplara ilişkin çözümlerin oluşturulması ve kaliteli ürün elde edilmesi açısından fayda sağlayacaktır.
