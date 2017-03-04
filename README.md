# Automatic Moodle Downloader

The `moodleCrawler.py` script downloads all the files posted in the course page of all the courses in your moodle page.
Dublicated Files in the `root_dir` get deleted. Links in the history file get not downloaded.

You can change names of downloaded Files and Places them to a different location, they will not be downloaded again (only if you delete the history files).

Set the following in the file `config.ini` before running the script

- `username` : Moodle Username
- `password` : Moodle Password
- `root_dir` : The root directory for where the files are to be stored
- `url` : URL for moodle authentication
- `forum` : If forums should also be crawled
- `history` : If a history file should be used
- `loglevel` : Sets the level of logging (0 - less information / 5 - all information)
- `externallinks` : If external links should get crawled
- `crawlcoursesink` : Moodle Course Crawler startpoint (Default course/index.php = all Courses) 

All the files are stored in their respective directories inside the `root_dir` with the names as in moodle.


It is planed to build a script to login (and logout) from all courses on a moodle platform. For the moment there is a script called `moodleCourseCrawler.py` that uses the `crawlcoursesink` option. This script only logs all courses on the platform.


#### REQUIREMENTS

- Python 2
- Beautifulsoup - `sudo apt-get install python-beautifulsoup` or `sudo pip install beautifulsoup4`
- Colorama - `sudo pip install colorama`
- Termcolor - `sudo pip install termcolor`
- lxml or similar - `easy_install lxml` or see http://lxml.de/installation.html for more information.

### EXTRAS

- Put `watch -n 3600 python moodleCrawler.py` in startup to fetch the files every hour.



This code is the modified version of the downloader created by Vinay Chandra



  Copyright 2017 Daniel Vogt

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
