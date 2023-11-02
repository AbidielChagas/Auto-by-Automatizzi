<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
[![LinkedIn][website-shield]][website-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698940983/Screenshot_2_w4kgpp.png" alt="Logo">
  </a>

<h3 align="center">Auto by Automatizzi</h3>

  <p align="center">
    Automated car management made easy
    <br />
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#caching-data-with-timestamp">Caching data with timestamp</a></li>
    <li><a href="#backend-features">Backend Features</a></li>
    <li><a href="#database">Datanase</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698792752/main_ywgm8o.png" />

Auto a mobile application crafted by Automatizzi, bringing a revolutionary solution tailored to the unique needs of car washers, detailers, and mechanics. 
This innovative app is meticulously designed to be a game-changer in the realm of vehicle management, offering a range of exceptional features that empower professionals in the automotive industry.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- BUILT WITH -->
### Built With

* [![React-native][React-native]][React-native-url]
* [![Django][Django]][Django-url]
* [![MySQL][MySQL]][MySQL-url]
* [![AWS][AWS]][AWS-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

This serves as both a visual exhibit of the mobile app and a glimpse into some of the powerful backend capabilities.

### Animated Home Screen
<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698934452/ezgif.com-optimize_v1h77d.gif" />

### Auth Screens - Dark Mode
These screenshoots were took from a Motorola Moto G9 Play which has 6.5 inch screen with a 720x1600 pixel resolution
<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698793663/tertiary_xucw7v.png" />

### Auth Screens - Light Mode 
These screenshoots were took from a Motorola Moto G7 Play which has 5.7 inch screen with a 720x1512 pixel resolution
<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698935113/Sem_t%C3%ADtulo_bm8kpb.png" />

### Responsive Desgin

#### 5.7 inch screen
<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698935671/Sem_t%C3%ADtulo1_eprxby.png" />

#### 6.5 inch screen
<img src="https://res.cloudinary.com/dsques4uz/image/upload/v1698792752/main_ywgm8o.png" />

## Caching data with timestamp
To optimize resource utilization and boost system performance, an asynchronous caching feature was developed.
This feature plays a pivotal role in caching data with exceptional efficiency and versatility.

The today cache gets updated every time a new vehicle is added to the database.
```ts
import AsyncStorage from "@react-native-async-storage/async-storage";

export const getCachedData = async (cacheKey) => {
  try {
    const cachedData = await AsyncStorage.getItem(cacheKey);
    return JSON.parse(cachedData);
  } catch (error) {
    console.error(`Error getting cached data for ${cacheKey}:`, error);
    return null;
  }
};

export const setCachedData = async (cacheKey, data) => {
  try {
    const timestamp = new Date().getDate();
    const dataToCache = { data, timestamp };
    await AsyncStorage.setItem(cacheKey, JSON.stringify(dataToCache));
  } catch (error) {
    console.error(`Error setting cached data for ${cacheKey}:`, error);
  }
};
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- BACKEND FEATURES -->
## Backend Features

### Serveless architecture
The backend of this application has been constructed on top of a serverless architecture, 
meaning that a Lambda function is invoked through an API Gateway whenever a client initiates a request from within the mobile app.

### Weekly report
This application offers a valuable feature in the form of a weekly report, which is generated based on the data collected throughout the week.</br>
The purpose of this report is to empower the customer with insightful information that can drive informed decision-making.

### Real time filtering
This application provides a dynamic real-time filtering feature that empowers customers to make more informed decisions and gain valuable insights into their business operations. </br>
By offering the capability to filter data by brand, color, and model, this feature enhances the user experience and contributes to the success of their business

<!-- DATABASE -->
## Database

### Cached data

This application's database is designed with an advanced caching feature that significantly enhances performance, optimizes lookup times, and conserves server resources.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->
## Roadmap

- [ ] WhatsApp API integration
  - [ ] Notify customer on vehicle status
- [ ] Add phone number field
    - [ ] Add switch button for Whatsapp notification in the profile screen

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Abidiel Chagas - abidielchagas@outlook.com

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [White car door handle](https://www.pexels.com/video/white-car-door-handle-6873502/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-shield]: https://img.shields.io/github/license/AbidielChagas/Auto-by-Automatizzi.svg?style=for-the-badge
[license-url]: https://github.com/AbidielChagas/Auto-by-Automatizzi/blob/main/LICENSE

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/abidiel-chagas/

[website-shield]: https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white
[website-url]: http:automatizzi.com.br

[React-native]: https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-native-url]: https://reactnative.dev/

[Django]: https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white
[Django-url]: https://www.djangoproject.com/

[MySQL]: https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white
[MySQL-url]: https://www.mysql.com/

[AWS]:https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white
[AWS-url]:https://aws.amazon.com/
