---
description: El método GetI recupera el elemento en la posición especificada.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Método CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660671"
---
# <a name="cbaselistgeti-method"></a>CBaseList. GetI, método

El `GetI` método recupera el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posición del elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento.

## <a name="remarks"></a>Observaciones

Si *pos* es **null**, el método devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




