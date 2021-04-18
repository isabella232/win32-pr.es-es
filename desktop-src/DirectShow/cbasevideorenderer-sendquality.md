---
description: El método SendQuality envía un mensaje de calidad para indicar lo que el proveedor debe hacer sobre la calidad.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Método CBaseVideoRenderer. SendQuality (Renbase. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660239"
---
# <a name="cbasevideorenderersendquality-method"></a>CBaseVideoRenderer. SendQuality, método

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

Cantidad de tiempo que tarda el fotograma en retrasarse.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Hora de Currentstream.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro envía un mensaje de control de calidad ascendente para controlar la administración de calidad. La naturaleza del mensaje de calidad (es decir, si se va a reducir o aumentar el número de muestras) se determina en la implementación de administración de calidad en esta clase derivada (vea [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




