---
description: 'El método ThreadProc es el procedimiento de subproceso para el subproceso de trabajo. Este método implementa el método CAMThread:: ThreadProc virtual puro.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream. ThreadProc (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679169"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream. ThreadProc (método)

El `ThreadProc` método es el procedimiento de subproceso para el subproceso de trabajo. Este método implementa el método [**CAMThread:: ThreadProc**](camthread-threadproc.md) virtual puro.

## <a name="syntax"></a>Sintaxis


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si el subproceso se completó correctamente o 1 de lo contrario. Si el valor devuelto es 1, es posible que los recursos del subproceso sigan asignados.

## <a name="remarks"></a>Observaciones

Este método espera indefinidamente a las solicitudes de subprocesos llamando al método [**CAMThread:: GetRequest**](camthread-getrequest.md) . Si recibe una solicitud [**CSourceStream:: Run**](csourcestream-run.md) o [**CSourceStream::P ause**](csourcestream-pause.md) , llama al método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . El método **DoBufferProcessingLoop** envía datos hasta que recibe una solicitud [**CSourceStream:: Stop**](csourcestream-stop.md) . El procedimiento de subproceso se cierra cuando recibe una solicitud [**CSourceStream:: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




