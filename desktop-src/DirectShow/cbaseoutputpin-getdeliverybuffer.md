---
description: El método GetDeliveryBuffer recupera un ejemplo multimedia que contiene un búfer vacío.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Método CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671504"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>CBaseOutputPin. GetDeliveryBuffer, método

El `GetDeliveryBuffer` método recupera un ejemplo multimedia que contiene un búfer vacío.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSample* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del búfer.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntero a la hora de inicio del ejemplo, o **null**.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a la hora de finalización del ejemplo, o **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinación bit a bit de las marcas admitidas por la interfaz [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | No hay ningún asignador disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método **IMemAllocator:: getBuffer** en el asignador y pasa los parámetros a ese método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




