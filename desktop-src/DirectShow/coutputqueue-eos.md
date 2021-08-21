---
description: El método EOS entrega una llamada de fin de flujo al pin de entrada.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Método COutputQueue.EOS (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3effb06498ae65cad8eefd9a3144cab140926006cd38acee45c553c4295b0a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537145"
---
# <a name="coutputqueueeos-method"></a>Método COutputQueue.EOS

El `EOS` método entrega una llamada de fin de flujo al pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
void EOS();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el objeto usa un subproceso, pone en cola un mensaje de \_ control EOS PACKET. El subproceso entrega los ejemplos pendientes y llama al método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el pin de entrada.

Si el objeto no usa un subproceso, llama al método [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) para entregar los ejemplos pendientes. A continuación, **llama a IPin::EndOfStream en** el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




