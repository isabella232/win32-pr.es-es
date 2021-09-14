---
description: El método ReceiveMultiple entrega un lote de muestras multimedia al pin de entrada.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Método COutputQueue.ReceiveMultiple (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062433"
---
# <a name="coutputqueuereceivemultiple-method"></a>Método COutputQueue.ReceiveMultiple

El `ReceiveMultiple` método entrega un lote de muestras de medios al pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSamples* 
</dt> <dd>

Dirección de un puntero a una matriz de ejemplos.

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de ejemplos de la matriz.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Puntero a una variable que recibe el número de muestras entregadas correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Notificación de fin de flujo recibida antes de procesar este ejemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                                           |



 

## <a name="remarks"></a>Observaciones

Si el objeto usa un subproceso, este método pone en cola todos los ejemplos pasados en la matriz. De lo contrario, el método llama [**al método IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




