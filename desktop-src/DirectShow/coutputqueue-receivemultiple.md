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
ms.openlocfilehash: 2bb893c0d77907832e160d54c73ee404ccddf6932d94a2ec75d0ecfc984f9014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831815"
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



 

## <a name="remarks"></a>Comentarios

Si el objeto usa un subproceso, este método pone en cola todos los ejemplos pasados en la matriz. De lo contrario, el método llama [**al método IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




