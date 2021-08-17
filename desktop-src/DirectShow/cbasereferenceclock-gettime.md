---
description: El método GetTime recupera la hora de referencia actual. Este método implementa el método IReferenceClock::GetTime.
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock.GetTime (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a1ffd021ac917a7aa1e12f3d3dc9c4a62ea1f883f126bca1d9c1300d335bdae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954984"
---
# <a name="cbasereferenceclockgettime-method"></a>Método CBaseReferenceClock.GetTime

El `GetTime` método recupera la hora de referencia actual. Este método implementa el [**método IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* 
</dt> <dd>

Puntero a una variable que recibe la hora actual, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | Argumento de puntero **NULL.**<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El tiempo devuelto es el mismo que el valor anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Comentarios

Este método llama al [**método CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) para determinar la hora real del reloj. Si la hora del reloj es estrictamente mayor que el valor anterior, usa la `GetTime` hora del reloj y devuelve S \_ OK. De lo `GetTime` contrario, usa el valor anterior y devuelve S \_ FALSE. Por lo tanto, el reloj interno puede ejecutarse hacia atrás durante un breve período, sin hacer que el tiempo de referencia se ejecute hacia atrás. En su lugar, la hora de referencia se "detiene" en el mismo valor hasta que el reloj interno se activa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




