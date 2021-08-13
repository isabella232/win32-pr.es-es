---
title: Media.sourceURL
description: La propiedad sourceURL recupera la dirección URL del elemento multimedia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Archivo Media.sourceURL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415955"
---
# <a name="mediasourceurl"></a>Media.sourceURL

La **propiedad sourceURL** recupera la dirección URL del elemento multimedia.

## <a name="syntax"></a>Sintaxis

*player*. *currentMedia*.sourceURL

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **sourceURL para** recuperar la dirección URL del primer elemento multimedia de la lista de reproducción de ejemplo; A continuación, la dirección URL del elemento multimedia se asigna a la propiedad de dirección URL del **objeto de** reproductor. El **objeto Player** se creó con id. = "Player".


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





