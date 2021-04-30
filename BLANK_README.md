[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab">
    <img src="images/CNL_logo_Square.jpeg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">trial by trial data export eeglab</h3>

  <p align="center">
    project_description
    <br />
    <a href="https://https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/tree/main/src"><strong>Explore the code »</strong></a>
    <br />
    <br />
    ·
    <a href="https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/issues">Report Bug</a>
    ·
    <a href="https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/issues">Request Feature</a>
	.
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This project is build so that one can automatically export trial by trial data from Matlab to any other file type so that other programs (such as Rstudio) can read the data.
This code uses both EEGlab functions and EEGlab structures. This means that your data needs to at least be epoched using EEGlab.


### Built With

* [Matlab](https://www.mathworks.com/)
* [EEGlab](https://sccn.ucsd.edu/eeglab/index.php)




<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites
Software: You need to have a copy of [EEGlab] (https://sccn.ucsd.edu/eeglab/download.php) (this script works for version eeglab2019_1)
Data: you need to have you .set files epoched and there need to be triggers in this epoched data.  

<!-- ROADMAP -->
## Roadmap
To use EEGlab
[In matlab, set path --> add with Subfolders... -->the main eeglab folder --> close](https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/blob/main/images/screenshot_add_path.PNG)
Or you can hardcode this: 

  ```matlab
   addpath(genpath('theplacewhereyouhavethefolder\eeglab2019_1\'));
  ```
Set-up your variables:

```matlab
group = 1; 
load_path  = 'C:\data\';
save_path= 'C:\results\';
typefile= '.xlsx'; 
time_window = [];
name_timewindow= '';
chan = '';  
name_file = '_epoched'; 
events_in_epoch_cond1 = {'1'}; 
events_in_epoch_cond2 = {'15'}; 
events_in_epoch_cond3 = {}; 
```

*Groups
	you can choose up to 4 groups. These will be assiged a number (1,2,3,4) so that the groups can be indentified in your next program.
*typefile
	final file can be saved as mat, txt, dat, csv, xls, xlsm, xlsx or xlsb
*time_window
	the script will give you 1 averaged amplitude for the time (in ms) you input in this variable. For example input here the time of your N1/MMN/P2 or whatever is of interest
*name_timewindow 
	this is for naming the file at the end of the script. to prevent overwriting files if there are mulitple times of intresset
*name_file
	this is the part of the .set file that is the same for all your participants (so without the ID)
*events_in_epoch_cond#
	you choose here which trigger or tiggers need to be included in the epoch. if you add multiple, it will not necessarily have them all in the epoch together.

*promts
	the first promt is to see if you have your .set files in indivual folders per subject or in one general folder
	the second promt will ask how many condtions need to be looked at. these are the ones you defined in events_in_epoch_cond#
	
See the [open issues](https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/issues) for a list of proposed features (and known issues).


## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Douwe Horsthuis - [@douwejhorsthuis](https://twitter.com/douwejhorsthuis) - douwehorsthuis@gmail.com

Project Link: [https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab](https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/DouweHorsthuis/trial_by_trial_data_export_eeglab.svg?style=for-the-badge
[contributors-url]: https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/DouweHorsthuis/trial_by_trial_data_export_eeglab.svg?style=for-the-badge
[forks-url]: https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/network/members
[stars-shield]: https://img.shields.io/github/stars/DouweHorsthuis/trial_by_trial_data_export_eeglab.svg?style=for-the-badge
[stars-url]: https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/stargazers
[issues-shield]: https://img.shields.io/github/issues/DouweHorsthuis/trial_by_trial_data_export_eeglab.svg?style=for-the-badge
[issues-url]: https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/issues
[license-shield]: https://img.shields.io/github/license/DouweHorsthuis/trial_by_trial_data_export_eeglab.svg?style=for-the-badge
[license-url]: https://github.com/DouweHorsthuis/trial_by_trial_data_export_eeglab/blob/main/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/DouweHorsthuis
