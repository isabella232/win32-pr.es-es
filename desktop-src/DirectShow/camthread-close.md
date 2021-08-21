---
description: El método Close espera a que se cierre el subproceso y, a continuación, libera sus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread.Close (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf12a80cd967832755f476db0e8810867326e84598ddce835e1da10dc6943419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158936"
---
# <a name="camthreadclose-method"></a>Método CAMThread.Close

El `Close` método espera a que se cierre el subproceso y, a continuación, libera sus recursos.

## <a name="syntax"></a>Sintaxis


```C++
void Close();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe proporcionar una manera de que el subproceso salga. Por ejemplo, en el [**método CAMThread::ThreadProc,**](camthread-threadproc.md) defina una solicitud que señale al subproceso para salir. A continuación, [**llame al método CAMThread::CallWorker**](camthread-callworker.md) con ese valor.

El [**método destructor ~ CAMThread**](camthread--camthread.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




