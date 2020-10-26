# My Maps 

## Chia-Jui Hung*

**My Maps** displays a list of maps, each of which show user-defined markers with a title, description, and location. The user can also create a new map. 

Time spent: **20** hours spent in total

## Functionality 

The following **required** functionality is completed:

* [X] The list of map titles is displayed.
* [X] After tapping on a map title, the associated markers in the map are shown.
* [X] The user is able to create a new map.

The following **extensions** are implemented:

* [X] When a map marker is created, the pin is animated.
* [X] The theme color is purple

## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src='https://j.gifs.com/oVqGGL.gif' title='Video Walkthrough of MyMaps' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

I had some difficulties when I wanted to display the google map. At first, I thought my API key may have some problems, so I recreated my key and
save it to another google cloud project to see if it worked. I also tried to delete the app and reinstall it to see if it would work. 
However, none of them work. Then, I noticed that my package name didn't match my SHA-1 certificate in google_maps_api xml file after digging it for a while.
I went to my directories to see if I create map activity in the wrong place. It turned out that my DisplayMapActivity was generated under the directory models,
which should only contain Place and UserMap. Thus, my google map was not properly displayed and I had to redo everything. Android studio is smart enough to generate
code, files and folders for us once we create some objects. The integration of UI and code is convenient. However, we also have to be careful when we generate a new
object and understand the hierarchy between different files and objects. Otherwise, it's also hard to debug.


## License

    Copyright [2020] [Chia-Jui Hung]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
