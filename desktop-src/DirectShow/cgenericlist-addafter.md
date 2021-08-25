---
description: El método AddAfter inserta un elemento después de la posición especificada y usa los parámetros "p" y "pObj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: 'Método CGenericList.AddAfter (Wxlist.h): parámetros p, pObj'
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
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697541"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Método CGenericList.AddAfter (Wxlist.h): parámetros p, pObj

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

*P* 
</dt> <dd>

Posición después de la cual se va a agregar el elemento. Si *p* es **NULL,** el método agrega el elemento al final de la lista.

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

 

 




