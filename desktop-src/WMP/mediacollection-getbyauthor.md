---
title: Método MediaCollection.getByAuthor
description: El método getByAuthor recupera una lista de reproducción de los elementos multimedia del autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Método getByAuthor Reproductor de Windows Media
- Método getByAuthor Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media , método getByAuthor
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
ms.openlocfilehash: 87989d38d49ff87ce26b7394f4ee79ef4bd7197cd0e35dcd5316797df401ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574632"
---
# <a name="mediacollectiongetbyauthor-method"></a>Método MediaCollection.getByAuthor

El **método getByAuthor** recupera una lista de reproducción de los elementos multimedia del autor especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*author* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del autor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getByAuthor para recuperar** una lista de reproducción de elementos multimedia. La lista de reproducción contiene elementos que coinciden con el autor especificado por el usuario en un elemento de entrada HTML TEXT denominado GetAuthor. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
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

 

 





