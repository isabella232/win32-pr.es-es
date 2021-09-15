---
title: Método getAll de IWMPPlaylistCollection
description: El método getAll devuelve una interfaz IWMPPlaylistArray que proporciona acceso a todas las listas de reproducción de la biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- Método getAll Reproductor de Windows Media
- Método getAll Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media , método getAll
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466999"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>IWMPPlaylistCollection::getAll (método)

El **método getAll** devuelve una **interfaz IWMPPlaylistArray** que proporciona acceso a todas las listas de reproducción de la biblioteca.

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

Interfaz **WMPLib.IWMPPlaylistArray** para la matriz recuperada de listas de reproducción.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





