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
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074769"
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

Cantidad de tiempo en la que el fotograma llega tarde.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Hora de la secuencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro envía un mensaje de control de calidad ascendente para controlar la administración de la calidad. La naturaleza del mensaje de calidad (es decir, si se reduce o aumenta el número de muestras) se determina en la implementación de administración de calidad en esta clase derivada (vea [**CBaseVideoRenderer::ShouldDrawSampleNow).**](cbasevideorenderer-shoulddrawsamplenow.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




