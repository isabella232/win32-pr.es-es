---
description: El método Close espera a que se cierre el subproceso y, a continuación, libera sus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread. Close (Wxutil. h)
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
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690768"
---
# <a name="camthreadclose-method"></a>CAMThread. Close (método)

El `Close` método espera a que se cierre el subproceso y, a continuación, libera sus recursos.

## <a name="syntax"></a>Sintaxis


```C++
void Close();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe proporcionar una manera de salir del subproceso. Por ejemplo, en el método [**CAMThread:: ThreadProc**](camthread-threadproc.md) , defina una solicitud que indique al subproceso que salga. A continuación, llame al método [**CAMThread:: CallWorker**](camthread-callworker.md) con ese valor.

El método de destructor [**~ CAMThread**](camthread--camthread.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




