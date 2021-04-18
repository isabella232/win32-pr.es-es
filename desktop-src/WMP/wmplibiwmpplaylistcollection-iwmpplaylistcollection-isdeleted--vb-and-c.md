---
title: IWMPPlaylistCollection isDeleted (método)
description: El método isDeleted devuelve un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método isDeleted
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708146"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>IWMPPlaylistCollection:: isDeleted (método)

El método **IsDeleted** devuelve un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.

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

*pItem* \[ de\]
</dt> <dd>

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción consultada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Boolean** que especifica si se eliminó la lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





