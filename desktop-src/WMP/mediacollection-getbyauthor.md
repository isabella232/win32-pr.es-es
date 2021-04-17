---
title: MediaCollection. getByAuthor, método
description: El método getByAuthor recupera una lista de reproducción de los elementos multimedia por el autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- método getByAuthor de Windows Media Player
- método getByAuthor de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708215"
---
# <a name="mediacollectiongetbyauthor-method"></a>MediaCollection. getByAuthor, método

El método **getByAuthor** recupera una lista de reproducción de los elementos multimedia por el autor especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*autor* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del autor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByAuthor** para recuperar una lista de reproducción de elementos multimedia. La lista de reproducción contiene elementos que coinciden con el autor especificado por el usuario en un elemento de entrada de texto HTML denominado GetAuthor. El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





