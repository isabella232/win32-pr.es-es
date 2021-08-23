---
title: Método MediaCollection.getAll
description: El método getAll recupera una lista de reproducción que contiene todos los elementos multimedia de la biblioteca.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- Método getAll Reproductor de Windows Media
- Método getAll Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3bba961f9400470c16e3d773a5765d389ce05bc23c2e948f0b94c7ad22229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135077"
---
# <a name="mediacollectiongetall-method"></a>Método MediaCollection.getAll

El **método getAll** recupera una lista de reproducción que contiene todos los elementos multimedia de la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getAll para** reproducir elementos multimedia aleatoriamente desde la colección de medios. El **objeto Player** se creó con id. = "Player".


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





