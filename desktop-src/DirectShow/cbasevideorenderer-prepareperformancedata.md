---
description: El método PreparePerformanceData establece los valores \_ m trLate y m \_ trFrame del marco actual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer.PreparePerformanceData (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173782"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Método CBaseVideoRenderer.PreparePerformanceData

El `PreparePerformanceData` método establece los valores m **\_ trLate** **y m \_ trFrame** del marco actual.

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

Valor que indica el retraso de la muestra más allá de su tiempo debido, en unidades de tiempo de referencia.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tiempo de interframe, en unidades de tiempo de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro establece **m \_ trLate en** el valor de *trLate* y **m \_ trFrame** en el valor de *trFrame*.

Cuando se llama a la función miembro [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) desde [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), pasa los valores **de m \_ trLate** y **m \_ trFrame** para que actualice las estadísticas. `PreparePerformanceData` Se llama desde [**CBaseVideoRenderer::OnWaitEnd para**](cbasevideorenderer-onwaitend.md) establecer estos valores de miembro de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




