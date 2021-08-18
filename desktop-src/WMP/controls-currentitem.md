---
title: Controls.currentItem
description: La propiedad currentItem especifica o recupera el elemento multimedia actual.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls.currentItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997564"
---
# <a name="controlscurrentitem"></a>Controls.currentItem

La **propiedad currentItem** especifica o recupera el elemento multimedia actual.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto Multimedia de lectura **y** escritura.

## <a name="remarks"></a>Comentarios

Este método solo funciona con elementos del *Reproductor de*. **currentPlaylist**. No se admite la llamada a **currentItem** con una referencia a un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se usa **currentItem** para establecer el elemento multimedia actual del control de reproductor en el valor seleccionado en un elemento SELECT HTML. La lista de reproducción actual se especificó por primera vez mediante *PlaylistCollection*. **getByName**. El **objeto Player** se creó con id. = "Player".


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





