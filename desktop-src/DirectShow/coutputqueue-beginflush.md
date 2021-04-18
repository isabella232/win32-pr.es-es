---
description: El método BeginFlush inicia una operación de vaciado.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Método COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671216"
---
# <a name="coutputqueuebeginflush-method"></a>COutputQueue. BeginFlush, método

El `BeginFlush` método inicia una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece la variable miembro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) en **true**. Si el objeto utiliza un subproceso, el subproceso llama al método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) para liberar cualquier ejemplo pendiente. De lo contrario, el objeto llama a **FreeSamples** durante el método [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) . Este método también establece la variable miembro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) en S \_ false, lo que hace que el objeto descarte todos los ejemplos nuevos.

El objeto pasa la notificación de vaciado de nivel inferior llamando al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




