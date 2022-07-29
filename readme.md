<style>h2,h3,h4 { border-bottom: 0; } </style>

# rl-tools
This repo contains two separate projects made for rocket league.
* [Price tracker](#price-tracker)
* [Epic Games custom map changer](#map-changer)

<br />

## <p align="center">**Price tracker**</p>
### <p align="center">track changes in item prices</p>
 
### <center>**\*\* Not working due to [www.rl.insider.gg](https://www.rl.insider.gg) skeleton loading \*\***</center>

<br />

Price tracker is an app made in Flask that scrapes data from [rl.insider.gg](https://rl.insider.gg) using BeautifulSoup4. Main purpose of this project is to save time while trading items. Shows how prices have changed since the last data update, so you know in which offers you need to adjust the price. The new price in the top-right corner indicates how many credits have been added/subtracted from the lowest price on rl.insider.gg.

## Run Locally
To run this project install its dependencies:  
`pip3 install -r requirements.txt`  
When it's done run `server.py` and open **127.0.0.1:5000/** in your browser:  
`python3 server.py `  
Or just run `run.sh`

## Roadmap
* Fix app to work on new rl.insider.gg frontend
* Optimize receiving data from website

## Usage

To customize offers edit `config.json`  
```json
"my-offers":[
    {
        "_comment": "max 10 items/paints, paints: no-bl-tw-gr-cr-pi-co-sb-bs-sa-li-fo-or-pu",
        "Dueling Dragons": "no-bl-pi-fo",
        "OEM": {"paints": "bl", "rarity": "veryRare"}
    }
]
```
To add an item to the list edit the same file
```json
"all-items":[
    "Dueling Dragons",
    "New item"
],
```
## Screenshots
![List view](https://i.imgur.com/7QPGAYP.png "List view")
![Offers view](https://i.imgur.com/rlSJ8Ge.png "Offers view")

<br/>

---

<br/>

## <p align="center">**Map changer**</p>
### <p align="center">Allows to play Steam custom maps while playing on Epic Games</p>

<br />

Map changer is a tool written in PyQt that allows you to use Steam custom maps when playing on Epic Games. It swaps `ThrowbackStadium_P.upk` with a custom map of your choice. These maps must have the `.udk` extension in order to work. After swapping, just play on custom.

## Run Locally
To run this project install its dependencies:  
`pip3 install -r requirements.txt`

Copy `ThrowbackStadium_P.upk` from rl installation directory to `maps/original map` in project.

Download maps from Steam using [steamworkshopdownloader.io](https://steamworkshopdownloader.io/) and copy `{mapname}.udk` to a new folder in project directory. Example `maps/map_name/map.udk`. To show the preview image, just paste the file in the same folder as the map.

Finally run `python3 main.pyw`

![preview](https://i.imgur.com/otERVuj.png)