---
title: IWMPPlaylistCollection getAll (método)
description: El método getAll devuelve una interfaz IWMPPlaylistArray que proporciona acceso a todas las listas de reproducción de la biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- Método getAll Reproductor de Windows Media
- Método getAll Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media método , getAll
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
ms.openlocfilehash: c9ff50c2983d911e7aa3951e34f908d9982b623912539aa4e162c9cccb2f5256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568461"
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

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





