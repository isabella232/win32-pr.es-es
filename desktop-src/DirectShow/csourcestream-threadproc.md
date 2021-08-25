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
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915275"
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

## <a name="remarks"></a>Comentarios

Este método espera indefinidamente las solicitudes de subproceso llamando al [**método CAMThread::GetRequest.**](camthread-getrequest.md) Si recibe una [**solicitud CSourceStream::Run**](csourcestream-run.md) o [**CSourceStream::P ause,**](csourcestream-pause.md) llama al método [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) El **método DoBufferProcessingLoop** inserta datos hasta que recibe una [**solicitud CSourceStream::Stop.**](csourcestream-stop.md) El procedimiento del subproceso se cierra cuando recibe una [**solicitud CSourceStream::Exit.**](csourcestream-exit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




