---
title: Controls.currentMarker
description: La propiedad currentMarker especifica o recupera el número de marcador actual.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls.currentMarker Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc11f79460661b6622da529b0de025672794af660aeb27bf56c7910a6d5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580311"
---
# <a name="controlscurrentmarker"></a>Controls.currentMarker

La **propiedad currentMarker** especifica o recupera el número de marcador actual.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de **lectura** y escritura (**long**) con un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Al **establecer currentMarker,** la reproducción se inicia desde el marcador especificado. Antes de intentar establecer **currentMarker**, determine si un archivo tiene marcadores y cuántos tiene mediante **markerCount**. Si un archivo no tiene marcadores, si **establece currentMarker** en cualquier cosa menos cero, se producirá un error. Si **se establece currentMarker** en un número mayor que **markerCount,** también se producirá un error.

La **propiedad currentMarker** siempre devuelve el marcador actual o el último, lo que significa que la posición real del archivo puede estar en el marcador actual o antes del marcador siguiente. Los marcadores se numeran a partir de 1, por lo que si un archivo tiene marcadores, puede establecer **currentMarker** en cero para cambiar la posición del archivo a cero.

Hasta que se establece el elemento multimedia actual (mediante el *Reproductor de*.**Dirección URL** o *reproductor.* **currentMedia**), **currentMarker** devuelve cero.

## <a name="examples"></a>Ejemplos

En el JScript ejemplo siguiente se usa **currentMarker** para iniciar la reproducción de vídeo desde el marcador que corresponde a la propiedad **selectedIndex** de un elemento SELECT HTML. El **objeto Player** se creó con id. = "Player".


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





