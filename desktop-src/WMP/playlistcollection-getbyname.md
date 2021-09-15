---
title: Método PlaylistCollection.getByName
description: El método getByName recupera un objeto PlaylistArray que contiene listas de reproducción con el nombre especificado, si existe alguna.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- Método getByName Reproductor de Windows Media
- Método getByName Reproductor de Windows Media , clase PlaylistCollection
- Clase PlaylistCollection Reproductor de Windows Media método , getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466143"
---
# <a name="playlistcollectiongetbyname-method"></a>Método PlaylistCollection.getByName

El **método getByName** recupera un objeto **PlaylistArray** que contiene listas de reproducción con el nombre especificado, si existe alguna.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre de las listas de reproducción que se recuperarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **PlaylistArray.**

## <a name="remarks"></a>Observaciones

Use *PlaylistArray*. **count** para determinar si existe una lista de reproducción. Si **count** es cero, no existe una lista de reproducción.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa playlistCollection*. **getByName para** comprobar el objeto **playlistCollection** de una lista de reproducción denominada "ThreeList". Si existe la lista de reproducción "Threelist", **getByName** establece "ThreeList" como la lista de reproducción actual. El **objeto Player** se creó con el identificador = "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





