---
description: El método PreparePerformanceData establece los \_ valores m trLate y m \_ trFrame del marco actual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660244"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>CBaseVideoRenderer. PreparePerformanceData, método

El `PreparePerformanceData` método establece los valores **m \_ trLate** y **m \_ trFrame** del marco actual.

## <a name="syntax"></a>Sintaxis


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*trLate* 
</dt> <dd>

Valor que indica el retraso de la muestra más allá de su tiempo de espera, en unidades de tiempo de referencia.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tiempo de INTERMARCO, en unidades de tiempo de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro establece **m \_ trLate** en el valor de *trLate* y **m \_ trFrame** en el valor de *trFrame*.

Cuando se llama a la función miembro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) desde [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), pasa los valores de **m \_ trLate** y **m \_ trFrame** para que actualice las estadísticas. `PreparePerformanceData` se llama desde [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) para establecer estos valores de miembro de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




