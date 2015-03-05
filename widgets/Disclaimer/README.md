#Disclaimer Widget for CMV
A simple yet configurable disclaimer widget for CMV

## Configurable Options

| Parameter | Type | Description |
| :----: | :--: | ----------- |
| `openOnStart` | Boolean | Default is true |
| `style` | String | Include the height to center the dialog properly. |
| `content` | String | Default is ''. The HTML you want to display in the disclaimer dialog |
| `href` | String | Default is null. Instead of HTML, you can point to a page that contains your HTML text. |
| `declineHref` | String | Default is `javascript:void(0)`. The url to navigate to when you user presses the decline button|
| `i18n` | Object | Default is {}. You can override the Internationalization with your own strings for the text on the buttons. See example below |


## Example Configuration:
#### Using content from an HTML page:
``` javascript
disclaimer: {
    include: true,
    id: 'disclaimer',
    type: 'floating',
    path: 'config/widgets/Disclaimer',
    title: 'Disclaimer',
    options: {

        // pre-define the height so the dialog is centered properly
        style: 'height:295px;width:375px;',

        // or you can provide the url for another page that includes the content
        href: './disclaimer.html'

    }
}
```
![Screenshot](../images/disclaimer1.jpg)


## Example Configuration:
#### Using content supplied in the widget configuration:
``` javascript
disclaimer: {
    include: true,
    id: 'disclaimer',
    type: 'floating',
    path: 'config/widgets/Disclaimer',
    title: 'Beware!!!',
    options: {

        // you can customize the button text
        i18n: {
            accept: 'Arghhhh!',
            decline: 'Run Away!'
        },

        // pre-define the height so the dialog is centered properly
        style: 'height:295px;width:375px;',

        // you can put your content right in the config
        content: '<div align="center" style="background-color:black;color:white;font-size:18px;padding:25px;">Abandon all hope, ye who enter here...<br/><img src="http://fc06.deviantart.net/fs5/i/2004/313/2/5/Captain_Jolly_Roger_by_ramiusraven.jpg" style="width:160px;margin-top:25px;" /></div>'

        // or you can provide the url for another page that includes the content
        //href: './disclaimer.html',

        // the url to go to if the user declines.
        //declineHref: 'http://esri.com/'

    }
}
```

![Screenshot](../images/disclaimer2.jpg)