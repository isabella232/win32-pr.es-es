---
title: IWMPPlaylistCollection Remove (método)
description: El método Remove quita una lista de reproducción de la biblioteca. | IWMPPlaylistCollection Remove (método)
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- quitar Media Player de Windows de método
- quitar método Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, Remove (método)
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719028"
---
# <a name="iwmpplaylistcollectionremove-method"></a>IWMPPlaylistCollection:: Remove (método)

El método **Remove** quita una lista de reproducción de la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* \[ de\]
</dt> <dd>

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que este método va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso total a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

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

 

 





