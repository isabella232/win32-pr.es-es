---
description: El método AddBefore inserta un elemento antes de la posición especificada. Este método usa los parámetros ' p ' y ' pObj '.
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Método CGenericList. AddBefore (Wxlist. h)-p, parámetros pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104004000"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Método CGenericList. AddBefore (Wxlist. h)-p, parámetros pObj

El `AddBefore` método inserta un elemento antes de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Posición antes de la que se va a insertar la lista. Si *p* es **null**, este método agrega el elemento al final de la lista.

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

 

 




