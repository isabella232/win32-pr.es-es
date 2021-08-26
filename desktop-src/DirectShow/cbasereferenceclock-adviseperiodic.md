---
description: El método AdvisePeriodic crea una solicitud de asesoramiento periódica. Este método implementa el método IReferenceClock::AdvisePeriodic.
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock.AdvisePeriodic (Refclock.h)
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
ms.openlocfilehash: e4b81fc8dfc33cc2a6e5207e984de0c2e693b8c00b8f8d35949d0bb7150484bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052435"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>CBaseReferenceClock.AdvisePeriodic (método)

El `AdvisePeriodic` método crea una solicitud de aviso periódica. Este método implementa el [**método IReferenceClock::AdvisePeriodic.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic)

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

Hora de la primera notificación, en unidades de 100 nanosegundos. Debe ser mayor que cero y menor que MAX \_ TIME.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Tiempo entre notificaciones, en unidades de 100 nanosegundos. Debe ser mayor que cero.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Controlar un semáforo creado por el autor de la llamada.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud de asesoramiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de hora no válidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Error<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

En cada hora de notificación, el reloj libera el semáforo especificado en el *parámetro hSemaphore.* Cuando no se requiera ninguna otra notificación, llame al método [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor *pdwAdviseToken* devuelto por esta llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




