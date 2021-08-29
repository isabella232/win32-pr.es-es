---
description: El método AddTail anexa un elemento al final de la lista.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: 'Método CGenericList.AddTail (Wxlist.h): parámetro pObj'
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
ms.openlocfilehash: 614a2f26349834c01f0a3e7587eae28c41e546a0585ef603af0265ea35c187d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055615"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>Método CGenericList.AddTail (Wxlist.h): parámetro pObj

El `AddTail` método anexa un elemento al final de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero a un objeto de tipo **OBJECT** (tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor POSITION para la nueva posición de cola. Si se produce un error en el método, devuelve **NULL.**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




