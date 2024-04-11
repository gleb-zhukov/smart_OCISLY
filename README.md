# OCISLY. local hub - Yandex IoT core (mqtt brocker)

примеры запросов.

#1
запрос от сервера узнать состояние ргб контроллера 
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "304521789",
"Command": "getState",
"DeviceID": "4",
"Type": "RGBcontroller"
}
```
ответ от ocisly
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "304521789",
"Command": "Ok",
"DeviceID": "4",
"Type": "RGBcontroller",
"Values": [
  {"Value": "90", "Type": "INT", "Name": "Brightness"}, 
  {"Value": "125", "Type": "INT", "Name": "Red"}, 
  {"Value": "32", "Type": "INT", "Name": "Green"}, 
  {"Value": "31", "Type": "INT", "Name": "Blue"}]
}
```
#2
запрос от сервера изменить состояние ргб контроллера 
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "304521789",
"Command": "changeState",
"DeviceID": "4",
"Type": "RGBcontroller",
"OnOffState": "On",
"Values": [
  {"Value": "90", "Type": "INT", "Name": "Brightness"}, 
  {"Value": "125", "Type": "INT", "Name": "Red"}, 
  {"Value": "32", "Type": "INT", "Name": "Green"}, 
  {"Value": "31", "Type": "INT", "Name": "Blue"}]
}
```
ответ от ocisly
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "304521789",
"Command": "Ok",
"DeviceID": "4",
"Type": "RGBcontroller",
"OnOffState": "On",
"Values": [
  {"Value": "90", "Type": "INT", "Name": "Brightness"}, 
  {"Value": "125", "Type": "INT", "Name": "Red"}, 
  {"Value": "32", "Type": "INT", "Name": "Green"}, 
  {"Value": "31", "Type": "INT", "Name": "Blue"}]
}
```

#3
запрос от сервера узнать показания метеостанции
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "getState",
"DeviceID": "2",
"Type": "Meteostantion"
}
```
ответ от ocicly
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "Ok",
"DeviceID": "2",
"Type": "Meteostantion",
"Values": [
  {"Value": "90.22961", "Type": "Float", "Name": "Humidity"}, 
  {"Value": "125.06672", "Type": "Float", "Name": "CarbonDioxide"}, 
  {"Value": "32.808365", "Type": "Float", "Name": "Pressure"}, 
  {"Value": "31.049744", "Type": "Float", "Name": "Temperature"}]
}
```
#4
запрос от сервера узнать состояние реле
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "getState",
"DeviceID": "7",
"Type": "relay"
}
```
ответ от ocisly
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "Ok",
"DeviceID": "7",
"Type": "relay",
"OnOffState": "On"
}
```

#5
запрос от сервера включить реле
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "changeState",
"DeviceID": "7",
"Type": "relay",
"OnOffState": "On"
}
```
ответ от ocisly
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "Ok",
"DeviceID": "7",
"Type": "relay",
"OnOffState": "On"
}
```
#6
сообщение от ocisly что появилось новое устройство
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "newDevice",
"DeviceID": "10",
"Type": "relay"
}
```
#7
сообщение от сервера об удалении устройства
```cpp
{
"UserID": "skfl2O;lksdhfdkjs@jkljfdfj",
"SendTgMsg": "null",
"Command": "deleteDevice",
"DeviceID": "10",
"Type": "relay"
}
```
