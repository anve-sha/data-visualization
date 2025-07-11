# data-visualization
#the code is written in python language it is use to get data (weather)of a city it is made with integrating open API
import requests
API_Key="ff37cba89c40e97d05ee880f01507177"
c_name="kanpur" 

url=f'https://api.openweathermap.org/data/2.5/weather?q={c_name}&appid={API_Key}&units=metric'



response=requests.get(url)
if response.status_code == 200:
    data=response.json()
    print('weather is ',data['weather'][0]['description'])
    print('current temperature is',data['main']['temp'])
    print('current temperature feels like is',data['main']['feels_like'])
    print('humidity is',data['main']['humidity'])
    
