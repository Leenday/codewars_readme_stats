<h1 align="center">Codewars readme stats</h1>

Display your codewars stats at your [github readme profile](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)!

<h4 align="center">Service Status </h4>   
<p align="center">
   <a href="https://github.r2v.ch/"> 
      <img src="https://github.r2v.ch/health"/ alt="Currently down 🙃">
    </a>
</p>


## Basic Example

Just replace `USERNAME` in the string below by your codewars username and copy-paste it to your github profile readme.
```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME)
```

![Codewars](https://github.r2v.ch/codewars?user=dinifarb)

---
## Query params

You can add the following query params to the base url: `https://github.r2v.ch/codewars`

|parameter|requierd|describtion|example|
|-----|-----|-----|-----|
| `username` | yes |used to get the user info from codewars|`username=foo`| 
| [name](https://github.com/dinifarb/codewars_readme_stats#Display-nickname)|no|if set to `true` the codewars `name` (nickname) is used on the card instead of the username |`name=true` |
| [top_languages](https://github.com/dinifarb/codewars_readme_stats#Top-trained-languages-icons) |no|extens the crad with 3 icons of the top trained languages |`top_languages=true`|
| [stroke](https://github.com/dinifarb/codewars_readme_stats#Set-card-border) |no|sets a border with the passed in color around the card |`stroke=black`<br>`stroke=rgb(0,0,0)`<br> `stroke=%23000000`|
| [theme](https://github.com/dinifarb/codewars_readme_stats#Themes) |no| sets a theme for the card |`theme=light`<br>`theme=dark`|
| [hide_clan](https://github.com/dinifarb/codewars_readme_stats#hide-clan) |no| removes the clan name from the card |`hide_clan=true`|

## Examples for all query params

### Display nickname

```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME&name=true)
```

![Codewars](https://github.r2v.ch/codewars?user=dinifarb&name=true)

### Top trained languages icons

```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME&top_languages=true)
```

![Codewars](https://github.r2v.ch/codewars?user=dinifarb&top_languages=true)

### Set card border

```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME&stroke=%23BB432C)
```
> :warning: **Important:** 
> You can pass in the usual css color types just make sure to use `%23` instead of `#` while using hex code because of the [url encoding](https://www.w3schools.com/tags/ref_urlencode.asp)

![Codewars](https://github.r2v.ch/codewars?user=dinifarb&stroke=%23BB432C)

### Themes
This allows you to change de default codewars like theme. You can find a example of all themes [here](https://github.com/dinifarb/codewars_readme_stats/blob/master/codewars/themes.md). 

```md
![Codewars](https://github.r2v.ch/codewars?user=dinifarb&theme=gradient)
```
![Codewars](https://github.r2v.ch/codewars?user=dinifarb&theme=gradient)

If you wish for other themes I am happy to take a pull request, just place your desired color set in the [themes.go](https://github.com/dinifarb/codewars_readme_stats/blob/master/codewars/themes.go) and [themes.md](https://github.com/dinifarb/codewars_readme_stats/blob/master/codewars/themes.md) file and your ready to go for the PR. For gradient themes see the special values for the `Card` property of the `Theme` struct. You can find more infos about how to add gradient values in the [themes.go](https://github.com/dinifarb/codewars_readme_stats/blob/master/codewars/themes.go) file.

### Hide Clan

```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME&hide_clan=true)
```
> :warning: **Important:** 
> This feature will eventually be expanded in a way to hide other infos like `honor` from the card. Therefore it is not guaranteed that it will stay exact the same.

![Codewars](https://github.r2v.ch/codewars?user=dinifarb&hide_clan=true)

### All params together

```md
![Codewars](https://github.r2v.ch/codewars?user=USERNAME&name=true&top_languages=true&stroke=%23b362ff&theme=purple_dark)
```

![Codewars](https://github.r2v.ch/codewars?user=dinifarb&name=true&top_languages=true&stroke=%23b362ff&theme=purple_dark)

----
## Link to when clicked
The pattern for linking svg content `![name](link to svg)` can be wrapped in `[]()` markdown option to link somewhere when clicked.

```md
[![Codewars](https://github.r2v.ch/codewars?user=USERNAME)(LINK)]
```

[![Codewars](https://github.r2v.ch/codewars?user=dinifarb&name=true)](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
----

## As Image
Optional to the svg ref markdown style it is possible to load the card as image. This gives you the possibility to center it as example.

```html
<p align="center" >
    <a href="LINK TO: WHEN CLICKED">
      <img src="https://github.r2v.ch/codewars?user=USERNAME" />
    </a>
</p>
```
<p align="center" >
    <a href="LINK TO: WHEN CLICKED">
      <img src="https://github.r2v.ch/codewars?user=dinifarb" />
    </a>
</p>


## Host it on your own
In case you want to run this service on your own server you can use the docker image. The image is available on [dockerhub](https://hub.docker.com/r/dinifarb/codewars).

Try it out with:

```bash
docker run -it -p 3000:3000 dinifarb/codewars
``` 

Or just clone this repo and do whatever you want with it.😉

## Additional

- Inspired by https://github.com/anuraghazra/github-readme-stats

- Icons are from https://simpleicons.org/

- If you have any questions don't hesitate open a issue! 

