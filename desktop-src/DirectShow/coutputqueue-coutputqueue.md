---
description: Método de constructor.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Constructor COutputQueue. COutputQueue (Outputq. h)
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
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680583"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Constructor COutputQueue. COutputQueue

Método de constructor.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada. El objeto proporcionará ejemplos a este pin.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un código de retorno **HRESULT** . Establezca el valor en es \_ correcto antes de llamar a este método. En la devolución, *PHR* recibe un valor que indica si el método se ha ejecutado correctamente o no.

</dd> <dt>

*bAuto* 
</dt> <dd>

Marca que especifica si el objeto decide cuándo se debe crear una cola. Si **es true**, el objeto crea una cola solo si el PIN de entrada puede bloquearse. Si **es false**, el parámetro *bQueue* especifica si se va a crear una cola.

</dd> <dt>

*bQueue* 
</dt> <dd>

Si *bAuto* es **true**, se omite este parámetro. Si *bAuto* es **false**, esta marca especifica si se va a crear una cola.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Número máximo de muestras que se van a enviar en un lote.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Marca que especifica si se van a utilizar tamaños de lote exactos. Si **es true**, el objeto espera los ejemplos de *lBatchSize* antes de entregarlos al pin de entrada. Si **es false**, el objeto proporciona ejemplos a medida que los recibe.

</dd> <dt>

*lListSize* 
</dt> <dd>

Tamaño de la memoria caché para la cola. El valor predeterminado, DEFAULTCACHE, es una constante definida para la clase [**CBaseList**](cbaselist.md) .

</dd> <dt>

*dwPriority* 
</dt> <dd>

Prioridad del subproceso que proporciona ejemplos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si *bAuto* es **true**, el objeto llama al método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) en el código PIN de nivel inferior. Si **ReceiveCanBlock** devuelve S \_ correcto (lo que significa que el PIN podría bloquearse en las llamadas a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ), el objeto crea un subproceso para entregar ejemplos. De lo contrario, no crea un subproceso.

Si *bAuto* es **false**, el valor de *bQueue* determina si se va a crear un subproceso.

Si el objeto crea un subproceso, asigna el identificador de subproceso a la variable miembro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) . El procedimiento de subproceso es [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)y el parámetro Thread es un puntero a este. El objeto también crea una cola para contener ejemplos, que viene dado por la variable de miembro de [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




