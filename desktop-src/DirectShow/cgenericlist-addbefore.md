---
description: El método AddBefore inserta un elemento antes de la posición especificada. Este método usa los parámetros "p" y "pObj".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: 'Método CGenericList.AddBefore (Wxlist.h): parámetros p, pObj'
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
ms.openlocfilehash: b508cc6cacba3c2a6c5877c69797ce3f6d396296610910a15701c00e3dbbadf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697475"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Método CGenericList.AddBefore (Wxlist.h): parámetros p, pObj

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

*P* 
</dt> <dd>

Posición antes de la que se va a insertar la lista. Si *p* es **NULL,** este método agrega el elemento al final de la lista.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntero a un objeto de tipo **OBJECT** (tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición del elemento insertado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (Clase)**](cgenericlist.md)
</dt> </dl>

 

 




