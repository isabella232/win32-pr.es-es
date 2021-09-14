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
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362542"
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
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/>                       |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El tiempo devuelto es el mismo que el valor anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

Este método llama al [**método CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) para determinar la hora del reloj real. Si la hora del reloj es estrictamente mayor que el valor anterior, `GetTime` usa la hora del reloj y devuelve S \_ OK. De lo `GetTime` contrario, usa el valor anterior y devuelve S \_ FALSE. Por lo tanto, el reloj interno puede ejecutarse hacia atrás durante un breve período, sin hacer que el tiempo de referencia se ejecute hacia atrás. En su lugar, la hora de referencia se "detiene" en el mismo valor hasta que el reloj interno se activa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




