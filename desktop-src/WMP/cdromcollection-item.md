---
title: Método CdromCollection.item
description: El método item recupera el objeto Cdrom en el índice especificado.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método item Reproductor de Windows Media
- método item Reproductor de Windows Media , CdromCollection (clase)
- CdromCollection class Reproductor de Windows Media , item method
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f700a17c29c382e96a5601bd9bbfabf3c4ede1b253d9f271b1d37ab1106ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864085"
---
# <a name="cdromcollectionitem-method"></a>Método CdromCollection.item

El **método** item recupera el **objeto Cdrom** en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto Cdrom.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa CdromCollection*. **elemento** para imprimir el nombre de la lista de reproducción de cada CD disponible en el equipo. Si la unidad realmente contiene contenido de DVD, Windows XP o posterior. Se creó un elemento TextArea HTML con id. = "listas de reproducción". El **objeto Player** se creó con id. = "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom.driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**CdromCollection (objeto)**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection.count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





