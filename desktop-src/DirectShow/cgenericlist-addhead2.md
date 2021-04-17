---
description: El método AddHead agrega una lista al principio de la lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: 'Método CGenericList. AddHead (Wxlist. h): parámetro plist'
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
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670275"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Método CGenericList. AddHead (Wxlist. h): parámetro plist

El `AddHead` método agrega una lista al principio de la lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pList* 
</dt> <dd>

Puntero a la lista de elementos que se van a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




