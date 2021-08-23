---
description: El método InitialThreadProc llama al método COutputQueue::ThreadProc cuando se crea el subproceso.
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimétodo tialThreadProc (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813595"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Inimétodo tialThreadProc

El `InitialThreadProc` método llama al método [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) cuando se crea el subproceso.

## <a name="syntax"></a>Sintaxis


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Puntero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor devuelto por el [**método COutputQueue::ThreadProc.**](coutputqueue-threadproc.md)

## <a name="remarks"></a>Comentarios

Este método es el procedimiento de subproceso para el subproceso de trabajo del objeto. El puntero del objeto `this` es el parámetro de subproceso. El método desreferencia esto para llamar a **ThreadProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




