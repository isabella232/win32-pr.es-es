---
description: El método AddHead agrega un elemento al frente de la lista.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: 'Método CGenericList.AddHead (Wxlist.h): parámetro pObj'
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
ms.openlocfilehash: 176a31c3acf846c4112e7bcb7bd457872e1e4086b4a8d214ccc7a175e7891feb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697474"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Método CGenericList.AddHead (Wxlist.h): parámetro pObj

El `AddHead` método agrega un elemento al frente de la lista.

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

Puntero a un objeto de tipo **OBJECT** (tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor POSITION que indica la nueva posición de la cabeza. Si se produce un error en el método , el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




