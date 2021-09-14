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
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062447"
---
# <a name="coutputqueuenewsegment-method"></a>Método COutputQueue.NewSegment

El `NewSegment` método entrega un nuevo segmento al pin de entrada.

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

Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Si el objeto usa un subproceso, pone en cola los siguientes elementos, en orden:

-   Mensaje de control NEW \_ SEGMENT.
-   Datos de segmento.

El mensaje NEW \_ SEGMENT notifica al subproceso que el siguiente elemento de la cola contendrá datos de segmento. Los datos de segmento se agrupan en una estructura , declarada como sigue:


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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




