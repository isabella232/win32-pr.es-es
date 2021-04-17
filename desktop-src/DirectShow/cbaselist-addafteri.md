---
description: El método AddAfterI inserta un elemento después de la posición especificada.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Método CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670949"
---
# <a name="cbaselistaddafteri-method"></a>CBaseList. AddAfterI, método

El `AddAfterI` método inserta un elemento después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición detrás de la que se va a agregar el elemento.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición del elemento insertado.

## <a name="remarks"></a>Observaciones

Si *pos* es **null**, este método agrega el elemento al encabezado de la lista (equivalente a llamar al método [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




