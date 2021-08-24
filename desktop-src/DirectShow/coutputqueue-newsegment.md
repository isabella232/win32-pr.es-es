---
description: El método NewSegment entrega un nuevo segmento al pin de entrada.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Método COutputQueue.NewSegment (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768145"
---
# <a name="coutputqueuenewsegment-method"></a>Método COutputQueue.NewSegment

El `NewSegment` método entrega un nuevo segmento a la patilla de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Posición del medio inicial del segmento, en unidades de 100 nanosegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Posición del medio final del segmento, en unidades de 100 nanosegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad a la que se debe procesar este segmento, como porcentaje de la velocidad original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Si el objeto usa un subproceso, pone en cola los siguientes elementos, en orden:

-   Mensaje de \_ control NEW SEGMENT.
-   Datos de segmento.

El mensaje NEW \_ SEGMENT notifica al subproceso que el siguiente elemento de la cola contendrá datos de segmento. Los datos de segmento se agrupan en una estructura, declarada de la siguiente manera:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



El subproceso llama al [**método IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el pin de entrada, utilizando los datos dados en la estructura .

Si el objeto no usa un subproceso, llama al método [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) para entregar los ejemplos pendientes. A continuación, **llama a IPin::NewSegment en** el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




