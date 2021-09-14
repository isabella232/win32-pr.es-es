---
description: 'Destructor CAMThread.~CAMThread: método Destructor.'
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160270"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




