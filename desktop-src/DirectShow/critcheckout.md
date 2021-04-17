---
description: Devuelve FALSE si el subproceso actual es el propietario de la sección crítica especificada.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Función CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670725"
---
# <a name="critcheckout-function"></a>CritCheckOut función)

Devuelve **false** si el subproceso actual es el propietario de la sección crítica especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En las compilaciones de depuración, devuelve **false** si el subproceso actual es el propietario de esta sección crítica, o bien **true** en caso contrario. En las compilaciones comerciales, siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Esta función es la inversa de la función [**CritCheckIn**](critcheckin.md) . Si **CritCheckIn** devuelve **true**, **CritCheckOut** devuelve **false** y viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de sección crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




