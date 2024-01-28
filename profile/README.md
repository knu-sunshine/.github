<a name="readme-top"></a>


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!--
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![webos][webos-shield]][webos-url]
-->


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://localhost:9999">
    <img src="https://raw.githubusercontent.com/knu-sunshine/.github/fab105dbeebc68d380808fcd844568bb62ebc5a5/profile/logo_text.svg" alt="Logo" style="width: 50%;">
  </a>


  <h3 align="center">Mr. Sunshine</h3>

  <p align="center">
    Smart home app & server solution for lighting, curtain control, sunrise/sunset tracking, and automated environment-based controls.
    <br />
    <br />
    <a href="https://localhost:9999">🎥 View Demo</a>
    ·
    <a href="https://localhost:9999">🐞 Report Bug</a>
    ·
    <a href="https://localhost:9999">💬 Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>🗂️ Table of Contents 🗂️</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#specifications">Specifications</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage-screenshot">Usage Screenshot</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<p align="center" style="display: flex; justify-content: space-between;">
    <<사진2개>>
</p>


### Background
With the recent development of smart home technology, it has become possible to effectively manage and automate lighting and curtain systems in the home. More and more users want to utilize these technologies for a more convenient life. In addition, there is a growing interest in environmental and energy conservation, and there is a growing need for an automatic control system to support it.

### Project Objectives and Scope
The Mr. Sunshine project encompasses the following key functionalities:

- **Login:** Users can log in to the app using their Google accounts.

- **Sunrise and Sunset Time Check:** Users can conveniently check sunrise and sunset times on the initial screen.

- **Room Registration:** Users have the ability to register rooms, which can contain various devices such as LED lights, curtains, and light sensors.

- **Device Registration:** Multiple devices can be registered within each room.

- **Device Control:** Users can register and control LED devices, adjusting brightness from 0 (off) to 100 (maximum brightness). Similarly, curtain devices can be registered and controlled, managing the curtain openness from 0 (closed) to 100 (fully open).

- **Room-Wide Device Control:** Users can control all registered control-related devices (LED lights and curtains) within a room collectively.

- **Auto Mode:** Auto mode relies on light sensors (minimum one for LED, curtain, and light) that periodically send light sensor values to the server. The server then compares these values with predefined thresholds. If the light sensor value falls below or exceeds the threshold, the server automatically adjusts the registered devices (LED lights and curtains) within the room to match the desired light level, aligning it with the predefined threshold.

This project uses IoT devices (LED, curtains, sensors) and MQTT for device control and sensor data transmission, while user-server interactions occur over HTTP. The server handles user control requests, AUTO mode, and device registrations, controlling IoT devices through MQTT.

<details>
  <summary>🖼️ System Architecture 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img src="https://github.com/knu-sunshine/.github/assets/112642604/53ec6c31-136e-45c1-8ae0-cb067f0a0326" alt="System Architecture" style="width: 99%;">
  </p>
</details>

<details>
  <summary>🖼️ Database ERD 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img src="https://github.com/noFlowWater/signage_solution/assets/112642604/db15a09a-faa7-4797-8f58-b865d7965681" alt="Database ERD" style="width: 99%;">
  </p>
</details>


### Tech Stack

| Category | Technology |
|----------|------------|
| Application | [![Flutter][Flutter]][Flutter-url][![Dart][Dart]][Dart-url][![Figma][Figma]][Figma-url] |
| Server | [![Nodejs][Nodejs]][Nodejs-url][![Express][Express]][Express-url][![npm][npm]][npm-url][![JavaScript][JavaScript.js]][JavaScript-url][![MQTT][MQTT]][MQTT-url] |
| Database | [![MongoDB][MongoDB]][MongoDB-url] |
| IoT Device | [![Raspberry][Raspberry]][Raspberry-url][![Ubuntu][Ubuntu]][Ubuntu-url][![Python][Python.org]][Python-url][![MQTT][MQTT]][MQTT-url] |
| Development Environment | [![macOS][macOS]][macOS-url][![Window][Window]][Window-url][![Linux][Linux]][Linux-url] |
| Collaborative Software | [![Git][Git]][Git-url][![GitHub][GitHub]][GitHub-url][![Notion][Notion]][Notion-url][![Skype][Skype]][Skype-url] | 


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!--SPECIFICATIONS-->
# Specifications

### Development Environment Specifications
Our project was developed in an Apple Silicon environment, which provided us with advanced computing capabilities and efficiency. Here are the details:

- **Platform**: Apple Silicon (M1, M1 Pro, M1 Max, or later)
- **Operating System**: macOS Big Sur or later
- **Memory**: 8GB RAM or more
- **Storage**: 256GB SSD or higher

We recommend using a similar Apple Silicon-based environment for development to ensure compatibility

### Hardware Requirements for Client Device

For setting up the client device in this project, you will need the following hardware components:

- **Raspberry Pi 4 4GB**(+@): The core computing unit for the kiosk.
- **MicroSD Card with webOS Image**: Use a microSD card loaded with the webOS image to boot the Raspberry Pi. For this project, we have used the pre-built webOS OSE 2.24.0 image for Raspberry Pi 4, which can be downloaded from [here](https://github.com/webosose/build-webos/releases/tag/v2.24.0). Additionally, if you need guidance on flashing the webOS Open Source Edition to your microSD card, please refer to [flashing webos-ose guide](https://www.webosose.org/docs/guides/setup/flashing-webos-ose/) for detailed instructions.
- **Touchscreen or Monitor**: A display unit to interact with the kiosk. A touchscreen is preferred for a more interactive experience.<br/> we use [this](https://www.icbanq.com/P009842845)
- **Webcam**: An essential component for facial recognition or other interactive features. Ensure compatibility with the Raspberry Pi.
- **Optional Input Devices**: Devices like a mouse and keyboard for initial setup and troubleshooting.
- **Power Supply and Cables**: A suitable power supply for the Raspberry Pi and screen, along with necessary cables such as HDMI for connectivity.


Ensure that you have all these components available before proceeding with the setup of your client device for the signage solution project.


> [webOS Offitial Docs](https://www.webosose.org/docs/guides/setup/system-requirements/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
# Getting Started

This guide will help you set up and run the project in your local environment. Follow these steps to get started.

> **Note:** This guide is tailored for a setup on **a single local PC**. It can also be adapted for multi-server environments, accommodating both centralized and distributed systems efficiently.

> **Note:** For effective data processing, we recommend hosting both the **Flask application and database on the same system**. This setup reduces latency and improves operational efficiency, especially for large, user-specific models.

## Installation

The process for installing and setting up the project is as follows. This template does not rely on any external dependencies or services.

1. Clone the repository.
   ```sh
   git clone https://github.com/noFlowWater/signage_solution.git
   ```
2. Move into the cloned directory.
   ```sh
   cd signage_solution
   ```
After cloning and moving into the directory, you will find three folders in the project directory:<br/>
`react`, `flask`, `nodejs`.

Proceed with the project in the following order:
- First, [Get Start for Kiosk API Server & Init Database](nodejs/README.md)
- Then, [Get Start for Face Authentication Server](flask/README.md)
- Finally, [Get Start for React for Deploy to webOS Client Device](react_signage/README.md)

Each step is detailed in the `README.md` file of the respective folder, allowing you to sequentially progress and gather the necessary information.


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage Screenshot 


<details>
  <summary>🖼️ Home 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="홈 화면" src="https://github.com/noFlowWater/signage_solution/assets/112642604/966af761-2f10-447f-90cb-241577823e90">
  </p>
</details>
<details>
<summary>🖼️ User 🖼️</summary>
<br>

### Select User Mode
<details>
  <summary>🖼️ 1. Select User Mode 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="사용자 모드 선택" src="https://github.com/noFlowWater/signage_solution/assets/112642604/211d6ba5-61ba-488c-bff9-eb5d333f68a8">
  </p>
</details>

### User Registration

<details>
  <summary>🖼️ 1. Enter User Basic Information 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="사용자 기본정보 입력" src="https://github.com/noFlowWater/signage_solution/assets/112642604/142c1e9f-d351-465c-b968-f7da5d178d3a">
  </p>
</details>

<details>
  <summary>🖼️ 2. Register user's face 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="사용자 얼굴 등록" src="https://github.com/noFlowWater/signage_solution/assets/112642604/f4fa27ea-f77b-4dc8-8914-bfe9d90eddf7">
  </p>
</details>

<details>
  <summary>🖼️ 3. Select User Allergy 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="사용자 알러지 선택" src="https://github.com/noFlowWater/signage_solution/assets/112642604/c4d73443-6c36-4eb9-8caf-a15b70af8eae">
  </p>
</details>

### User Login

<details>
  <summary>🖼️ 1. User Authentication 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="사용자 인식" src="https://github.com/noFlowWater/signage_solution/assets/112642604/999e78e4-031e-4ee0-885a-2683735138b9">
    <img style="width: 49%;" alt="사용자 확인" src="https://github.com/noFlowWater/signage_solution/assets/112642604/f8ba2823-7dd0-420a-8adc-106e66505853">
  </p>
</details>

<details>
  <summary>🖼️ 2. User Alternate Authentication 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="대체 인증" src="https://github.com/noFlowWater/signage_solution/assets/112642604/05f5b522-1237-4f15-a699-8b89271df2d8">
  </p>
</details>

### Menu 

<details>
  <summary>🖼️ 1. Custom Menu recommendation 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="메뉴 추천" src="https://github.com/noFlowWater/signage_solution/assets/112642604/101989ca-4f2f-42ef-be41-31651c4bacf6">
  </p>
</details>

<details>
  <summary>🖼️ 2. Check Menu Allergy/Soldout, Detail 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="알러지:매진 확인" src="https://github.com/noFlowWater/signage_solution/assets/112642604/40395041-7485-4749-878e-212477655be5">
    <img style="width: 49%;" alt="알러지 확인창" src="https://github.com/noFlowWater/signage_solution/assets/112642604/0bd82e2d-221d-4d94-ad35-da4a7d5be4f0">
  </p>
</details>

<details>
  <summary>🖼️ 3. Check Shopping Cart & Pay 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="장바구니 확인" src="https://github.com/noFlowWater/signage_solution/assets/112642604/58823132-e6b8-4b13-a667-04b4f535ec82">
    <img style="width: 49%;" alt="결제 완료" src="https://github.com/noFlowWater/signage_solution/assets/112642604/a0d01536-a62a-4bc7-aac4-8cc9555f21dd">
  </p>
</details>

</details>
<details>
<summary>🖼️ Admin 🖼️</summary>
<br>

### Administrator Login

<details>
  <summary>🖼️ 1. Administrator Login 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="관리자 로그인" src="https://github.com/noFlowWater/signage_solution/assets/112642604/e73aef73-ac9e-4c6e-b058-7fe5dcd4463c">
  </p>
</details>

<details>
  <summary>🖼️ 2. Administrator Login Failure 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="관리자 비밀번호 체크" src="https://github.com/noFlowWater/signage_solution/assets/112642604/83ae69bb-9e44-4482-bb19-297c15e288d5">
  </p>
</details>

### Administrator Menu Management

<details>
  <summary>🖼️ 1. Administrator Menu List 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="관리자 홈" src="https://github.com/noFlowWater/signage_solution/assets/112642604/6d8d6f01-440e-4b0c-96f8-2c8d2ba21fc9">
  </p>
</details>

<details>
  <summary>🖼️ 2. Administrator Menu Details 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="관리자 메뉴 상세보기" src="https://github.com/noFlowWater/signage_solution/assets/112642604/5bca34f5-1ab6-49a9-8e0b-bdf6257eb0b2">
  </p>
</details>


<details>
  <summary>🖼️ 3. Administrator Menu Registration and Deletion 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img src="https://github.com/noFlowWater/signage_solution/assets/112642604/bdb89e7e-4208-4aea-9f93-90c3daece562" 
           alt="관리자 메뉴 등록" 
           style="width: 49%;">
    <img src="https://github.com/noFlowWater/signage_solution/assets/112642604/4433ee82-b9fa-43dd-a325-8b84be381131"    
           alt="관리자 메뉴 수정"
           style="width: 49%;">
  </p>
</details>

### Administrator Password Change

<details>
  <summary>🖼️ 1. Changing Password (fail 1) 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="admin_change_password_1" src="https://github.com/noFlowWater/signage_solution/assets/112642604/3e66a0d8-ec91-4464-9f4a-6c32f2c897e7">
  </p>
</details>

<details>
  <summary>🖼️ 2. Changing Password (fail 2) 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="admin_change_password_2" src="https://github.com/noFlowWater/signage_solution/assets/112642604/435dae5a-4e51-480d-8a18-9c6921775a97">
  </p>
</details>

<details>
  <summary>🖼️ 3. Changing Password (success) 🖼️</summary>
  <p align="center" style="display: flex; justify-content: space-between;">
    <img style="width: 49%;" alt="admin_change_password_3" src="https://github.com/noFlowWater/signage_solution/assets/112642604/73223ce7-e487-4bbc-80ba-ffc505fd58c3">
  </p>
</details>

</details>

<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- CONTACT -->
## Contact

### 💡 노유수 ([noFlowWater](https://github.com/noFlowWater)) : [noyusu98@gmail.com](mailto:noyusu98@gmail.com)

### 💡 주보경 ([jupyter1234](https://github.com/jupyter1234)) : [wntjdals0412@gmail.com](mailto:wntjdals0412@gmail.com)

### 💡 윤진노 ([jinno321](https://github.com/jinno321)) : [jinno5522@gmail.com](mailto:jinno5522@gmail.com)

### 💡 이민수 ([ohyatt](https://github.com/ohyatt)) : [minsoo030232@gmail.com](mailto:minsoo030232@gmail.com)

### 💡 김현수 ([beoldshoe](https://github.com/beoldshoe)) : [howeve18@gmail.com](mailto:howeve18@gmail.com)


<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/noFlowWater/signage_solution.svg?style=for-the-badge
[contributors-url]: https://github.com/noFlowWater/signage_solution/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/noFlowWater/signage_solution.svg?style=for-the-badge
[forks-url]: https://github.com/noFlowWater/signage_solution/network/members
[stars-shield]: https://img.shields.io/github/stars/noFlowWater/signage_solution.svg?style=for-the-badge
[stars-url]: https://github.com/noFlowWater/signage_solution/stargazers
[issues-shield]: https://img.shields.io/github/issues/noFlowWater/signage_solution.svg?style=for-the-badge
[issues-url]: https://github.com/noFlowWater/signage_solution/issues
[license-shield]: https://img.shields.io/github/license/noFlowWater/signage_solution.svg?style=for-the-badge
[license-url]: https://github.com/noFlowWater/signage_solution/blob/master/LICENSE.txt
[webos-shield]: https://img.shields.io/badge/webos%20official%20example-A50034?style=for-the-badge&logo=lg
[webos-url]: https://www.webosose.org/samples/2023/12/21/facial-recognition-kiosk-using-webos
[product-screenshot]: images/screenshot.png

[Flutter]: https://img.shields.io/badge/Flutter-02569B.svg?style=for-the-badge&logo=Flutter&logoColor=white
[Flutter-url]: https://flutter.dev/

[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com

[Figma]: https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=fff
[Figma-url]: https://www.figma.com/

[Express]: https://img.shields.io/badge/Express-000000.svg?style=for-the-badge&logo=Express&logoColor=white
[Express-url]: https://expressjs.com/

[Raspberry]: https://img.shields.io/badge/Raspberry%20Pi-A22846.svg?style=for-the-badge&logo=Raspberry-Pi&logoColor=white
[Raspberry-url]: https://www.raspberrypi.com/

[Nodejs]: https://img.shields.io/badge/Node.js-393?style=for-the-badge&logo=nodedotjs&logoColor=fff
[Nodejs-url]: https://nodejs.org/en

[npm]: https://img.shields.io/badge/npm-CB3837.svg?style=for-the-badge&logo=npm&logoColor=white
[npm-url]: https://www.npmjs.com/

[MQTT]: https://img.shields.io/badge/MQTT-660066.svg?style=for-the-badge&logo=MQTT&logoColor=white
[MQTT-url]: https://mqtt.org/

[Dart]: https://img.shields.io/badge/Dart-0175C2.svg?style=for-the-badge&logo=Dart&logoColor=white
[Dart-url]: https://dart.dev/

[MongoDB]: https://img.shields.io/badge/MongoDB-47A248.svg?style=for-the-badge&logo=MongoDB&logoColor=white
[MongoDB-url]: https://www.mongodb.com/

[Python.org]: https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white
[Python-url]: https://www.python.org/

[JavaScript.js]: https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black
[JavaScript-url]: https://developer.mozilla.org/ko/docs/Learn/JavaScript

[LG]: https://img.shields.io/badge/webOS-A50034?style=for-the-badge&logo=lg&logoColor=fff
[LG-url]: https://www.webosose.org/

[Raspberry]: https://img.shields.io/badge/Raspberry%20Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=fff
[Raspberry-url]: https://www.raspberrypi.com/

[macOS]: https://img.shields.io/badge/macOS-000?style=for-the-badge&logo=macOS&logoColor=fff
[macOS-url]: https://support.apple.com/ko-kr/macOS


[Window]: https://img.shields.io/badge/Windows-0078D4.svg?style=for-the-badge&logo=Windows&logoColor=white
[Window-url]: https://www.microsoft.com/en-in/windows?r=1
[Notion]: https://img.shields.io/badge/Notion-000000.svg?style=for-the-badge&logo=Notion&logoColor=white
[Notion-url]: https://www.notion.so/


[Skype]: https://img.shields.io/badge/Skype-00AFF0.svg?style=for-the-badge&logo=Skype&logoColor=white
[Skype-url]: https://skype.com/


[GitHub]: https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=GitHub&logoColor=white

[GitHub-url]: https://github.com/


[Git]: https://img.shields.io/badge/Git-F05032.svg?style=for-the-badge&logo=Git&logoColor=white
[Git-url]: https://git-scm.com/


[Ubuntu]: https://img.shields.io/badge/Ubuntu-E95420.svg?style=for-the-badge&logo=Ubuntu&logoColor=white

[Ubuntu-url]: https://ubuntu.com/

[Linux]: https://img.shields.io/badge/Linux-FCC624.svg?style=for-the-badge&logo=Linux&logoColor=black

[Linux-url]: https://www.linux.org/
