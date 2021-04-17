---
description: El método Run notifica al pin que el filtro se está ejecutando ahora.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Método CBasePin. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670872"
---
# <a name="cbasepinrun-method"></a>CBasePin. Run (método)

El `Run` método notifica al pin que el filtro se está ejecutando ahora.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Hora de inicio que se pasa al método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Cuando el filtro pasa de pausado a en ejecución, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los PIN del filtro.

Este método no hace nada en la clase base. Las clases derivadas pueden invalidar este método. Por ejemplo, un PIN podría iniciar un subproceso de trabajo que entregue ejemplos.

El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve esta función miembro, de modo que no se prueba el estado desde este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




