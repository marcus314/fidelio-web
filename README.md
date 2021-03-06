# FIDELIO
Webiste for the fidelio project.

## Usage
Clone or download the repository.  
What you need:
 - **Python >= 3.6**
 - **MySQL** or SQLite

Make sure the requirements are installed using `pip`:
```bash
python3 -m pip install -r requirements.txt
```

You might want to setup the MySQL Database:
```bash
./setupdb.sh
```

Prepare the database:
```bash
FLASK_APP=src/app.py python3 -m flask db init
FLASK_APP=src/app.py python3 -m flask db merge -m "init"
FLASK_APP=src/app.py python3 -m flask db upgrade
```

Finally, you can run the server:
```bash
export CONFIG=config/[FILE]
FLASK_APP=src/app.py python3 -m flask run
```

## Development
Follow the same steps as in **Usage**. You migth need to `merge` and `upgrade` the database everytime you change the model.

For a clean setup run:
```bash
./clear-db.sh
```

### Contribute
Pull requests are alyways welcome! Feel free to fork the project and improve it.
## License

   Copyright 2018 Life-Science Lab <meteorkamera@life-science-lab.net>

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
