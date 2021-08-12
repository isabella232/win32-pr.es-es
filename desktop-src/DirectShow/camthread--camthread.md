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
ms.openlocfilehash: 884460b0c1af3b96a610a18b7475d2a144dc32bf308ea0e0191f0f526565726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662381"
---
# <a name="camthreadcamthread-destructor"></a>Destructor CAMThread.~CAMThread

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a>Observaciones

El destructor llama al [**método CAMThread::Close,**](camthread-close.md) que espera a que se cierre el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




