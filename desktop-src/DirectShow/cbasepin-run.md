---
description: El método Run notifica al pin que el filtro se está ejecutando.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Método CBasePin.Run (Amfilter.h)
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
ms.openlocfilehash: 4f145a827546a9258ee2968d0348ab7725147bb47132f5df5acbd2865a45b78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429815"
---
# <a name="cbasepinrun-method"></a>Método CBasePin.Run

El `Run` método notifica al pin que el filtro se está ejecutando.

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

Hora de inicio que se pasa al [**método IMediaFilter::Run del**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Cuando el filtro pasa de pausado a en ejecución, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los pines del filtro.

Este método no hace nada en la clase base. Las clases derivadas pueden invalidar este método. Por ejemplo, un pin podría iniciar un subproceso de trabajo que entregue ejemplos.

El estado interno del administrador de gráficos de filtros no se actualiza hasta después de que se devuelva esta función miembro, por lo que no pruebe el estado desde este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




