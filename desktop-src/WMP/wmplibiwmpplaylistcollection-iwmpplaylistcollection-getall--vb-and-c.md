---
title: IWMPPlaylistCollection getAll (método)
description: El método getAll devuelve una interfaz IWMPPlaylistArray que proporciona acceso a todas las listas de reproducción de la biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll (método) de Windows Media Player
- getAll (método) Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708998"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>IWMPPlaylistCollection:: getAll (método)

El método **getAll** devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a todas las listas de reproducción de la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPPlaylistArray** para la matriz de listas de reproducción recuperada.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





