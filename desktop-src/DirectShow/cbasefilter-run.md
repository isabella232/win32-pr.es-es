---
description: 'El método Run ejecuta el filtro. Este método implementa el método IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660435"
---
# <a name="cbasefilterrun-method"></a>CBaseFilter. Run (método)

El `Run` método ejecuta el filtro. Este método implementa el método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Hora de referencia correspondiente al tiempo de secuencia 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Si se detiene el filtro, este método pausa el filtro llamando al método [**CBaseFilter::P ause**](cbasefilter-pause.md) . A continuación, llama al método [**CBasePin:: Run**](cbasepin-run.md) en cada una de las clavijas conectadas del filtro. Por último, establece la variable miembro de [**\_ Estado CBaseFilter:: m**](cbasefilter-m-state.md) en el estado en \_ ejecución.

El tiempo de secuencia se calcula como el tiempo de referencia actual menos *tStart*. Un ejemplo multimedia con una marca de tiempo de cero se debe representar a la hora *tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




