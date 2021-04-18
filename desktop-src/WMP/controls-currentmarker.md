---
title: Controls. currentMarker
description: La propiedad currentMarker especifica o recupera el número de marcador actual.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Media Player de Windows Controls. currentMarker
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
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699928"
---
# <a name="controlscurrentmarker"></a>Controls. currentMarker

La propiedad **currentMarker** especifica o recupera el número de marcador actual.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**) con un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

La configuración de **currentMarker** hace que la reproducción se inicie desde el marcador especificado. Antes de intentar establecer **currentMarker**, determine si un archivo tiene marcadores y cuántos tiene con **markerCount**. Si un archivo no tiene marcadores, si se establece **currentMarker** en cualquier cosa pero cero, se produce un error. Establecer **currentMarker** en un número mayor que **markerCount** también produce un error.

La propiedad **currentMarker** siempre devuelve el marcador actual o el último, lo que significa que la posición del archivo real puede estar en el marcador actual o antes del marcador siguiente. Los marcadores se numeran a partir de 1, por lo que si un archivo tiene marcadores, puede establecer **currentMarker** en cero para cambiar la posición del archivo a cero.

Hasta que se establezca el elemento multimedia actual (mediante *Player*.**Dirección URL** o *reproductor*. **currentMedia**), **currentMarker** devuelve cero.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa **currentMarker** para iniciar la reproducción de vídeo desde el marcador que corresponde a la propiedad **SelectedIndex** de un elemento Select de HTML. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





