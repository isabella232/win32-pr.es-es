---
title: MediaCollection. getByName, método
description: El método getByName recupera una lista de reproducción de los elementos multimedia con el nombre especificado.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- método getByName de Windows Media Player
- método getByName de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690298"
---
# <a name="mediacollectiongetbyname-method"></a>MediaCollection. getByName, método

El método **getByName** recupera una lista de reproducción de los elementos multimedia con el nombre especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByName** para recuperar tres elementos de la biblioteca. Después, cada elemento se anexa a la lista de reproducción actual. El objeto **Player** se creó con ID = "Player".


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

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

 

 





