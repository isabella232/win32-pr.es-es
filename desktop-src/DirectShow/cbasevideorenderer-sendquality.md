---
description: El método SendQuality envía un mensaje de calidad para indicar lo que el proveedor debe hacer sobre la calidad.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Método CBaseVideoRenderer.SendQuality (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063351"
---
# <a name="cbasevideorenderersendquality-method"></a>Método CBaseVideoRenderer.SendQuality

El `SendQuality` método envía un mensaje de calidad para indicar lo que el proveedor debe hacer sobre la calidad.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*trLate* 
</dt> <dd>

Cantidad de tiempo durante el cual el fotograma llega tarde.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Hora de la secuencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro envía un mensaje de control de calidad ascendente para controlar la administración de la calidad. La naturaleza del mensaje de calidad (es decir, si se reduce o aumenta el número de muestras) se determina en la implementación de administración de calidad en esta clase derivada (vea [**CBaseVideoRenderer::ShouldDrawSampleNow).**](cbasevideorenderer-shoulddrawsamplenow.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




