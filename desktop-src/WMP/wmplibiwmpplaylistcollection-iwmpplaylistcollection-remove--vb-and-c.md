---
title: Método remove de IWMPPlaylistCollection
description: El método remove quita una lista de reproducción de la biblioteca. | Método remove de IWMPPlaylistCollection
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- remove method Reproductor de Windows Media
- Remove method Reproductor de Windows Media , IWMPPlaylistCollection (interfaz)
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media , método remove
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
ms.openlocfilehash: b342251bb1885b40d8cd225612ad68b1b54c6ca74cc29a9a934b1fa603837e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745720"
---
# <a name="iwmpplaylistcollectionremove-method"></a>IWMPPlaylistCollection::remove (método)

El **método remove** quita una lista de reproducción de la biblioteca.

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

*pItem* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción que este método quitará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





