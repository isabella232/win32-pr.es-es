---
description: El método EOS entrega una llamada de final de secuencia al pin de entrada.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Método COutputQueue. EOS (Outputq. h)
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
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680582"
---
# <a name="coutputqueueeos-method"></a>COutputQueue. EOS, método

El `EOS` método entrega una llamada de final de secuencia al pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
void EOS();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el objeto utiliza un subproceso, pone en cola un mensaje de control de paquetes de EOS \_ . El subproceso entrega cualquier ejemplo pendiente y llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada.

Si el objeto no utiliza un subproceso, llama al método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para proporcionar cualquier ejemplo pendiente. A continuación, llama a **IPin:: EndOfStream** en el PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




