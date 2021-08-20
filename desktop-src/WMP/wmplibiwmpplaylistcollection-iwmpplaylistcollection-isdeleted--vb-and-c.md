---
title: IWMPPlaylistCollection isDeleted (método)
description: El método isDeleted devuelve un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- Método isDeleted Reproductor de Windows Media
- Método isDeleted Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media método , isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c332a524b334933d587929cdd0e5b5fa61bc15d9110260af8af8e472d7c05fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568482"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>IWMPPlaylistCollection::isDeleted (método)

El **método isDeleted** devuelve un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción consultada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Boolean que** especifica si se eliminó la lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





