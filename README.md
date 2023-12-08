<!-- ABOUT THE PROJECT -->

## About The Project

![Product Name Screen Shot][product-screenshot]

<!-- Here's a blank template to get started: To avoid retyping too much info. Do a search and replace with your text editor for the following: -->

This project uses UNet, Residual UNet, and Attention UNet with dice score and combined dice loss as below:

| Model          | Dice score | Dice loss |
| -------------- | ---------- | --------- |
| UNet           | 0.8454     | 0.1489    |
| Residual UNet  | 0.8267     | 0.1454    |
| Attention UNet | 0.9412     | 0.1817    |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- [![Lightning][lightning-shield]][lightning-url]
- [![PyTorch][pytorch-shield]][pytorch-url]
- [![Python Version][python-shield]][python-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This project requires Python 3.7 or higher

- You can download the latest Python version [here](https://www.python.org/downloads/).

<!-- USAGE EXAMPLES -->

## Usage

There're 2 approaches to use this project:

1. <a href="#model-arch">Using the model architecture only</a>
2. <a href="#jupy">Using the jupyter notebook</a>

<h3 name="model-arch">Using model architecture only</h3>
Since the model is written in PyTorch nn.module, so the model can be used . In order to do that, do the follows.

1. The model is located at
   ```sh
       .
   └── unetArch/
       ├── .
       ├── .
       ├── .
       ├── unetModel.py
       └── unetParts.py
   ```
2. Import the model
   ```py
   from unetArch import UNet
   ```
3. Assign the model to a variable
   ```py
   model = UNet(n_channels=3, n_classes=5)
   ```
4. Proceed to use the model

<h3 name="jupy">Using the jupyter notebook</h3>
The provided jupyter notebook is only for a guidelines on how to use the model, make sure to modify the notebook to your specific case.

1. Open the provided jupyter notebook with the name of
   ```sh
   colorectalSegm.ipynb
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Model Parameters Documentations -->

## Model Parameters Documentations

> _unetArch.unetModel.UNet(n_channels, n_classes, residual=False, attention=False)_

- n_channels`int`: This parameter initialize the color channels of your image in your dataset. 3 for RGB, and 1 for black and white.
- n_classes`int`: This parameter initialize how many labels you have in your image in your dataset and makesure you add 1 to it because of the background.
- residual`bool`: This parameter initialize whether to use residual connection in your model or not. Default value is False.
- attention`bool`: This parameter initialize wheter to use channel and spatial attention in your model or not. Default value is False.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. As this is my first open source project, any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
