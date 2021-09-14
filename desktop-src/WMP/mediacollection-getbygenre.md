---
title: Método MediaCollection.getByGenre
description: El método getByGenre recupera una lista de reproducción de los elementos multimedia con el género especificado.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Método getByGenre Reproductor de Windows Media
- Método getByGenre Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967492"
---
# <a name="mediacollectiongetbygenre-method"></a>Método MediaCollection.getByGenre

El **método getByGenre** recupera una lista de reproducción de los elementos multimedia con el género especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*genre* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del género.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getByGenre para recuperar** una lista de reproducción de elementos multimedia. La lista de reproducción contiene elementos con el género especificado por el usuario en un elemento de entrada HTML TEXT denominado GetGenre. El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





