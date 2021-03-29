---
description: El método QueueSample pone en cola un ejemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue. QueueSample (Outputq. h)
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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678977"
---
# <a name="coutputqueuequeuesample-method"></a>COutputQueue. QueueSample, método

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método agrega un ejemplo al final de la cola. Mantenga la sección crítica antes de llamar a este método y llámela solo cuando el objeto esté utilizando un subproceso para ofrecer ejemplos. Para determinar si el objeto está utilizando un subproceso, llame al método [**COutputQueue:: IsQueued**](coutputqueue-isqueued.md) .

Este método también se puede utilizar para colocar mensajes de control en la cola. Un mensaje de control es una constante definida (convertida en un \_ tipo Long PTR) que indica al subproceso que realice alguna acción. La clase **COutputQueue** define los mensajes de control que se muestran en la tabla siguiente.



|               |                                        |
|---------------|----------------------------------------|
| Message       | Acción                                 |
| paquete de EOS \_   | Entrega de una notificación de final de secuencia. |
| NUEVO \_ segmento  | Entregue un nuevo segmento.                 |
| RESTABLECER \_ paquete | Restablecer el estado de la cola.          |
| ENVIAR \_ paquete  | Enviar un lote parcial de ejemplos.       |



 

Se trata de un método protegido, que la clase **COutputQueue** usa internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




