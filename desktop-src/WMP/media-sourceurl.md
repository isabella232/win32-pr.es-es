---
title: Media. sourceURL
description: La propiedad sourceURL recupera la dirección URL del elemento multimedia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media Player Windows Media. sourceURL
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
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699953"
---
# <a name="mediasourceurl"></a>Media. sourceURL

La propiedad **sourceURL** recupera la dirección URL del elemento multimedia.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. sourceURL

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **sourceURL** para recuperar la dirección URL del primer elemento multimedia de la lista de reproducción de ejemplo; la dirección URL del elemento multimedia se asigna entonces a la propiedad **dirección URL** del objeto de reproductor. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





