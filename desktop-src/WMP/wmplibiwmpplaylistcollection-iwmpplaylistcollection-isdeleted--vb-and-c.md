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
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466992"
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



| Requisito | Value |
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

 

 





