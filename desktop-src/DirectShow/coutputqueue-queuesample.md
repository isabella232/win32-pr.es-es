---
description: El método QueueSample pone en cola un ejemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue.QueueSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909595"
---
# <a name="coutputqueuequeuesample-method"></a>Método COutputQueue.QueueSample

El `QueueSample` método pone en cola un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método agrega un ejemplo al final de la cola. Mantenga la sección crítica antes de llamar a este método y llámelo solo cuando el objeto use un subproceso para entregar ejemplos. Para determinar si el objeto usa un subproceso, llame al [**método COutputQueue::IsQueued.**](coutputqueue-isqueued.md)

Este método también se puede usar para colocar mensajes de control en la cola. Un mensaje de control es una constante definida (conversión a un tipo LONG PTR) que indica al subproceso \_ que realice alguna acción. La **clase COutputQueue** define los mensajes de control que se muestran en la tabla siguiente.



| Etiqueta | Value |
|---------------|----------------------------------------|
| Message       | Acción                                 |
| PAQUETE \_ EOS   | Entrega de una notificación de fin de flujo. |
| NUEVO \_ SEGMENTO  | Entrega de un nuevo segmento.                 |
| RESTABLECER \_ PAQUETE | Restablezca el estado de la cola.          |
| ENVIAR \_ PAQUETE  | Envíe un lote parcial de ejemplos.       |



 

Se trata de un método protegido que la **clase COutputQueue** usa internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




