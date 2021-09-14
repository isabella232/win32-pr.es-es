---
description: El método ThreadProc es el procedimiento de subproceso.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Método CAMThread.ThreadProc (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160238"
---
# <a name="camthreadthreadproc-method"></a>Método CAMThread.ThreadProc

El `ThreadProc` método es el procedimiento de subproceso.

## <a name="syntax"></a>Sintaxis


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** cuyo significado se define mediante la clase derivada.

## <a name="remarks"></a>Observaciones

Se trata de un método virtual puro. Implemente este método en la clase derivada para proporcionar un procedimiento de subproceso. Cuando el [**método CAMThread::Create**](camthread-create.md) crea un subproceso, proporciona la dirección del método [**CAMThread::InitialThreadProc,**](camthread-initialthreadproc.md) que a su vez llama al método ThreadProc.

Normalmente, el método ThreadProc escribirá un bucle que recupera las solicitudes (mediante una llamada a los métodos [**CAMThread::GetRequest**](camthread-getrequest.md) o [**CAMThread::CheckRequest)**](camthread-checkrequest.md) y procesa los datos.

Cuando este método vuelve, el subproceso se cierra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




