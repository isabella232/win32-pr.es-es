---
description: El método GetDeliveryBuffer recupera un ejemplo multimedia que contiene un búfer vacío.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Método CBaseOutputPin.GetDeliveryBuffer (Amfilter.h)
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
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823614"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Método CBaseOutputPin.GetDeliveryBuffer

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

Dirección de una variable que recibe un puntero a la [**interfaz IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) búfer.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntero a la hora de inicio del ejemplo o **NULL.**

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a la hora de finalización del ejemplo o **NULL.**

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinación bit a bit de marcas admitidas por la [**interfaz IMemAllocator::GetBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | No hay ningún asignador disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al **método IMemAllocator::GetBuffer** en el asignador y pasa los parámetros a ese método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




