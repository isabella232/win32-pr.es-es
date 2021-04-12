---
description: El método AddAfter inserta un elemento después de la posición especificada y usa los parámetros ' p ' y ' pObj '.
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Método CGenericList. AddAfter (Wxlist. h)-p, parámetros pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362830"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Método CGenericList. AddAfter (Wxlist. h)-p, parámetros pObj

El `AddAfter` método inserta un elemento después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Posición detrás de la que se va a agregar el elemento. Si *p* es **null**, el método agrega el elemento al encabezado de la lista.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntero a un objeto de tipo **Object** (el tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición del elemento insertado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




