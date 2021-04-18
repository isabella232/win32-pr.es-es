---
description: El método AddBeforeI inserta un elemento antes de la posición especificada.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Método CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670945"
---
# <a name="cbaselistaddbeforei-method"></a>CBaseList. AddBeforeI, método

El `AddBeforeI` método inserta un elemento antes de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición antes de la que se va a agregar el elemento.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición del elemento insertado.

## <a name="remarks"></a>Observaciones

Si *pos* es **null**, este método agrega el elemento al final de la lista (equivalente a llamar al método [**CBaseList:: AddTailI**](cbaselist-addtaili.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




