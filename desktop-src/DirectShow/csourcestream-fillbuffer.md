---
description: El método FillBuffer rellena un ejemplo multimedia con datos.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: CSourceStream. FillBuffer (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690268"
---
# <a name="csourcestreamfillbuffer-method"></a>CSourceStream. FillBuffer, método

El `FillBuffer` método rellena un ejemplo multimedia con datos.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Final de la secuencia<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto<br/>       |



 

## <a name="remarks"></a>Observaciones

La clase derivada debe implementar este método.

El ejemplo multimedia dado a este método no tiene marcas de tiempo. La clase derivada debe llamar al método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) para establecer las marcas de tiempo. Si es adecuado para el tipo de medio, la clase derivada también debe establecer las horas del medio, llamando al método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Para obtener más información, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).

Devuelve S \_ false al final de la secuencia. Esto hace que la clase **CSourceStream** envíe la notificación de final de secuencia y detenga el bucle de procesamiento del búfer. Vea [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




