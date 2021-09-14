---
description: El método ThreadProc es el procedimiento de subproceso para el subproceso de trabajo. Este método implementa el método PURE VIRTUAL CAMThread::ThreadProc.
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream.ThreadProc (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070023"
---
# <a name="csourcestreamthreadproc-method"></a>Método CSourceStream.ThreadProc

El `ThreadProc` método es el procedimiento de subproceso para el subproceso de trabajo. Este método implementa el método PURE VIRTUAL [**CAMThread::ThreadProc.**](camthread-threadproc.md)

## <a name="syntax"></a>Sintaxis


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si el subproceso se completó correctamente o 1 en caso contrario. Si el valor devuelto es 1, es posible que todavía se asignen los recursos del subproceso.

## <a name="remarks"></a>Observaciones

Este método espera indefinidamente las solicitudes de subproceso mediante una llamada al [**método CAMThread::GetRequest.**](camthread-getrequest.md) Si recibe una [**solicitud CSourceStream::Run**](csourcestream-run.md) o [**CSourceStream::P ause,**](csourcestream-pause.md) llama al método [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) El **método DoBufferProcessingLoop** inserta datos hasta que recibe una [**solicitud CSourceStream::Stop.**](csourcestream-stop.md) El procedimiento del subproceso se cierra cuando recibe una [**solicitud CSourceStream::Exit.**](csourcestream-exit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




