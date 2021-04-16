---
description: 'El método GetTime recupera la hora de referencia actual. Este método implementa el método IReferenceClock:: GetTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock. GetTime (Refclock. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671531"
---
# <a name="cbasereferenceclockgettime-method"></a>CBaseReferenceClock. GetTime (método)

El `GetTime` método recupera la hora de referencia actual. Este método implementa el método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

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

Puntero a una variable que recibe la hora actual, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/>                       |
| <dl> <dt>**S \_ false**</dt> </dl>   | La hora devuelta es igual que el valor anterior.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) para determinar la hora real del reloj. Si la hora del reloj es estrictamente mayor que el valor anterior, `GetTime` usa la hora de reloj y devuelve S \_ correcto. De lo contrario, `GetTime` utiliza el valor anterior y devuelve S \_ false. Por lo tanto, el reloj interno puede ejecutarse hacia atrás durante un breve período, sin provocar que el tiempo de referencia se ejecute hacia atrás. En su lugar, el tiempo de referencia se "detendrá" en el mismo valor hasta que el reloj interno se ponga al día.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




