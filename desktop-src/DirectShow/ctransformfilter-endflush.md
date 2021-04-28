---
description: 'Método CTransformFilter.EndFlush: el método EndFlush finaliza una operación de vaciado.'
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085064"
---
# <a name="ctransformfilterendflush-method"></a>Método CTransformFilter.EndFlush

El `EndFlush` método finaliza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Al final de una operación de vaciado, el método [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) del pin de entrada llama a este método. Este método pasa la `EndFlush` llamada de bajada.

Si la clase derivada usa un subproceso de trabajo para entregar ejemplos, debe descartar los datos en cola antes de enviar la `EndFlush` llamada de nivel inferior. Para obtener más información, [vea Data Flow para desarrolladores de filtros.](data-flow-for-filter-developers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




