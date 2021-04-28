---
description: 'Destructor DE LAVTHREAD.~CAMThread: método destructor.'
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Destructor CAMThread.~CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096443"
---
# <a name="camthreadcamthread-destructor"></a>Destructor CAMThread.~CAMThread

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Comentarios

El destructor llama al [**método CAMThread::Close,**](camthread-close.md) que espera a que se cierre el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




