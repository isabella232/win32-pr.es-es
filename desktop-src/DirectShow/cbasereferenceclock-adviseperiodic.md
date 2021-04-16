---
description: 'El método AdvisePeriodic crea una solicitud de notificación periódica. Este método implementa el método IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock. AdvisePeriodic (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671254"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>CBaseReferenceClock. AdvisePeriodic, método

El `AdvisePeriodic` método crea una solicitud de notificación periódica. Este método implementa el método [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* 
</dt> <dd>

Hora de la primera notificación, en unidades de 100-nanosegundos. Debe ser mayor que cero y menor que \_ el tiempo máximo.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Tiempo entre notificaciones, en unidades de 100-nanosegundos. Debe ser mayor que cero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Identificador de un semáforo, creado por el autor de la llamada.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de hora no válidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Error<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

En cada momento de la notificación, el reloj libera el semáforo especificado en el parámetro *hSemaphore* . Cuando no se requieran más notificaciones, llame al método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor de *pdwAdviseToken* devuelto desde esta llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




