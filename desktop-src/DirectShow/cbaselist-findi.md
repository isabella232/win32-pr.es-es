---
description: El método FindI recupera la primera posición que contiene el elemento especificado.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Método CBaseList.FindI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8bdd89de7e28c5645cf8a418a8472d484f891a499f11e238b80af5f7062ff4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635464"
---
# <a name="cbaselistfindi-method"></a>Método CBaseList.FindI

El `FindI` método recupera la primera posición que contiene el elemento especificado.

## <a name="syntax"></a>Sintaxis


```C++
POSITION FindI(
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

Devuelve un valor POSITION o **NULL** si el elemento no está en la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




