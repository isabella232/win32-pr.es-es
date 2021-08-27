---
description: 'Constructor COutputQueue.COutputQueue: método constructor.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Constructor COutputQueue.COutputQueue (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bf50314fd0ceb1afbe00c5a6a63708cc79ab38d77931c80b086039c7ca9704c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087245"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Constructor COutputQueue.COutputQueue

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInputPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada. El objeto entregará ejemplos a este pin.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **código de retorno HRESULT.** Establezca el valor en S \_ OK antes de llamar a este método. En la devolución, *phr* recibe un valor que indica el éxito o error del método.

</dd> <dt>

*bAuto* 
</dt> <dd>

Marca que especifica si el objeto decide cuándo crear una cola. Si **es TRUE,** el objeto crea una cola solo si el pin de entrada puede bloquearse. Si **es FALSE,** *el parámetro bQueue* especifica si se va a crear una cola.

</dd> <dt>

*bQueue* 
</dt> <dd>

Si *bAuto* es **TRUE,** se omite este parámetro. Si *bAuto* es **FALSE,** esta marca especifica si se va a crear una cola.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Número máximo de muestras que se entregan en un lote.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Marca que especifica si se deben usar tamaños de lote exactos. Si **es TRUE,** el objeto espera los ejemplos *de lBatchSize* antes de entregarlos al pin de entrada. Si **es FALSE,** el objeto entrega muestras a medida que las recibe.

</dd> <dt>

*lListSize* 
</dt> <dd>

Tamaño de caché de la cola. El valor predeterminado, DEFAULTCACHE, es una constante definida para la [**clase CBaseList.**](cbaselist.md)

</dd> <dt>

*dwPriority* 
</dt> <dd>

Prioridad del subproceso que entrega ejemplos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si *bAuto* es **TRUE,** el objeto llama al método [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) en el pin de bajada. Si **ReceiveCanBlock devuelve** S OK (lo que significa que el pin podría bloquearse en \_ llamadas [**IMemInputPin::Receive),**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) el objeto crea un subproceso para entregar ejemplos. De lo contrario, no crea un subproceso.

Si *bAuto* es **FALSE,** el valor de *bQueue* determina si se va a crear un subproceso.

Si el objeto crea un subproceso, asigna el identificador de subproceso a la variable miembro [**COutputQueue::m \_ hThread.**](coutputqueue-m-hthread.md) El procedimiento del subproceso [**es COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md)y el parámetro thread es un puntero a esto. El objeto también crea una cola para contener ejemplos, que se proporciona mediante la variable miembro [**COutputQueue::m \_ List.**](coutputqueue-m-list.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




