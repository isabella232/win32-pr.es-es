---
title: Propiedad AxWindowsMediaPlayer. URL
description: La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propiedades de URL Media Player de Windows
- Propiedad URL Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad URL
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
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699987"
---
# <a name="axwindowsmediaplayerurl-property"></a>Propiedad AxWindowsMediaPlayer. URL

La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valor de propiedad

System. String que es la dirección URL del elemento multimedia.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o la página web que realiza la llamada.

Las aplicaciones que abren elementos multimedia de detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

No llame a este método desde el código del controlador de eventos. La llamada a la **dirección URL** desde un controlador de eventos puede producir resultados inesperados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se permite al usuario especificar un archivo multimedia escribiendo una ruta de acceso de archivo en un cuadro de texto. Cuando se hace clic en un botón, la propiedad URL se establece en el archivo especificado y se reproduce el archivo. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


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
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





