---
description: El método AddHead agrega un elemento al principio de la lista.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: 'Método CGenericList. AddHead (Wxlist. h): parámetro pObj'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104083824"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Método CGenericList. AddHead (Wxlist. h): parámetro pObj

El `AddHead` método agrega un elemento al principio de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero a un objeto de tipo **Object** (el tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de posición que indica la nueva posición del encabezado. Si se produce un error en el método, el valor devuelto es **null**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




