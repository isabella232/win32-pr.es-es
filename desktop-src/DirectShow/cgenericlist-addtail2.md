---
description: El método Addtail (anexa una lista al final de la lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: 'Método CGenericList. Addtail ((Wxlist. h): parámetro plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105660105"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Método CGenericList. Addtail ((Wxlist. h): parámetro plist

El `AddTail` método anexa una lista al final de la lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pList* 
</dt> <dd>

Puntero a la lista que se va a anexar.

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

 

 




