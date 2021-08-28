---
title: Propiedad AxWindowsMediaPlayer.URL
description: La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propiedades de dirección URL Reproductor de Windows Media
- Propiedad URL Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media propiedad , URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123885"
---
# <a name="axwindowsmediaplayerurl-property"></a>Propiedad AxWindowsMediaPlayer.URL

La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valor de propiedad

System.String que es la dirección URL del elemento multimedia.

## <a name="remarks"></a>Comentarios

Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o página web de llamada.

Las aplicaciones que abren elementos multimedia desde detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

No llame a este método desde el código del controlador de eventos. La llamada **a la dirección URL** desde un controlador de eventos puede producir resultados inesperados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se permite al usuario especificar un archivo multimedia especificando una ruta de acceso de archivo en un cuadro de texto. Cuando se hace clic en un botón, la propiedad URL se establece en el archivo especificado y se reproduce el archivo. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





