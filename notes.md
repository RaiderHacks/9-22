## Make a new Repl evironment

### Go to https://repl.it/

<img src="notes.assets/image-20200919180927141.png" alt="image-20200919180927141" style="zoom: 33%;" />

### Under language select Bash and name it `jokes-bot`

<img src="notes.assets/image-20200919181233484.png" alt="image-20200919181233484" style="zoom: 33%;" />

### In the terminal make a new python file using the `touch` command 

<img src="notes.assets/image-20200919181149273.png" alt="image-20200919181149273" style="zoom: 50%;" />



### Write the following code in the new python file

```python
import requests

URL = 'https://official-joke-api.appspot.com/random_joke'


def check_valid_status_code(request):
    if request.status_code == 200:
        return request.json()

    return False


def get_joke():
    request = requests.get(URL)
    data = check_valid_status_code(request)

    return data
  
print(get_joke())
```

- Run the code with `python main.py`
  - What happens? 



```javascript
{
    'id': 25,
    'type': 'programming', 
    'setup': 'How many programmers does it take to change a lightbulb?',
    'punchline': "None that's a hardware problem"
}
```



# Setting up a Discord server

### Make your own discord server

<img src="notes.assets/image-20200921180200582.png" alt="image-20200921180200582" style="zoom:50%;" />

<img src="notes.assets/image-20200921180333361.png" alt="image-20200921180333361" style="zoom:50%;" />

<img src="notes.assets/image-20200921180457050.png" alt="image-20200921180457050" style="zoom:50%;" />

## Sign into https://discord.com/developers/applications

### Click on `New Application`

<img src="notes.assets/image-20200921180752493.png" alt="image-20200921180752493" style="zoom:50%;" />

### Give your bot a name 

<img src="notes.assets/image-20200921180927933.png" alt="image-20200921180927933" style="zoom:50%;" />

### Under `Settings > Bot > Authorization Flow` Make sure the `PUBLIC BOT` option is enabled and the `REQUIRES OAUTH2 CODE GRANT` option is disabled

<img src="notes.assets/image-20200921183640772.png" alt="image-20200921183640772" style="zoom:50%;" />

### Under the settings tab navigate to `OAuth2 > Scopes`

<img src="notes.assets/image-20200921181141866.png" alt="image-20200921181141866" style="zoom:50%;" />

### Under Scopes select `Bot` then you will see a new section named `BOT PERMISSIONS` under that section select `Administrator`

<img src="notes.assets/image-20200921181525407.png" alt="image-20200921181525407" style="zoom:50%;" />

### Now copy the link under scopes and paste it into a new browser window 

<img src="notes.assets/image-20200921181658740.png" alt="image-20200921181658740" style="zoom:50%;" />

<img src="notes.assets/image-20200921182558508.png" alt="image-20200921182558508" style="zoom:50%;" />

### Select the server we set up earlier & click `Authorize` on the next window

<img src="notes.assets/image-20200921182849404.png" alt="image-20200921182849404" style="zoom:50%;" />

