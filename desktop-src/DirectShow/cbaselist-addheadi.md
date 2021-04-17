---
description: El método AddHeadI agrega un elemento al principio de la lista.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Método CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670941"
---
# <a name="cbaselistaddheadi-method"></a>CBaseList. AddHeadI, método

El `AddHeadI` método agrega un elemento al principio de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de posición que indica la nueva posición del encabezado.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, el valor devuelto es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




