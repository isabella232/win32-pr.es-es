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
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172018"
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

Devuelve un valor POSITION para la nueva posición de cola. Si se produce un error en el método, devuelve **NULL**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




