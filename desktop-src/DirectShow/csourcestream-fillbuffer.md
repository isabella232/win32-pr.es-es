---
description: El método FillBuffer rellena un ejemplo multimedia con datos.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Método CSourceStream.FillBuffer (Source.h)
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
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687405"
---
# <a name="csourcestreamfillbuffer-method"></a>Método CSourceStream.FillBuffer

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

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Fin de la secuencia<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Success<br/>       |



 

## <a name="remarks"></a>Comentarios

La clase derivada debe implementar este método.

El ejemplo multimedia dado a este método no tiene marcas de tiempo. La clase derivada debe llamar al [**método IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) para establecer las marcas de tiempo. Si es adecuado para el tipo de medio, la clase derivada también debe establecer las horas de medios mediante una llamada al [**método IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) Para obtener más información, [vea Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

Devuelve S \_ FALSE al final de la secuencia. Esto hace que **la clase CSourceStream** envíe la notificación de fin de flujo y detenga el bucle de procesamiento del búfer. Vea [**CSourceStream::D oBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




