---
title: PlaylistCollection. reproducción, método
description: El método reproducción crea una nueva lista de reproducción en la biblioteca.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- método reproducción de Windows Media Player
- método reproducción de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método reproducción
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709085"
---
# <a name="playlistcollectionnewplaylist-method"></a>PlaylistCollection. reproducción, método

El método **reproducción** crea una nueva lista de reproducción en la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre de la lista de reproducción que se va a crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Este método crea una lista de reproducción vacía en la biblioteca. Para rellenar la lista de reproducción con elementos multimedia, use la *lista de reproducción*. **appendItem** o *lista de reproducción*. **insertItem**.

En la biblioteca se permiten varias listas de reproducción con el mismo nombre. Para evitar la creación de un nombre de lista de reproducción duplicado con este método, use **getByName** y *PlaylistArray*. **recuento** para determinar si ya existe una lista de reproducción con un nombre determinado.

Los espacios iniciales y finales no se permiten en los nombres de las listas de reproducción y se quitan automáticamente del valor especificado para el parámetro *Name* .

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se crea una nueva lista de reproducción vacía denominada "ThreeList". El objeto **Player** se creó con ID = "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Lista de reproducción. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Lista de reproducción. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





