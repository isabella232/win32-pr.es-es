---
description: 'Método CTransformFilter.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter.BeginFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be20231cf62148e3487aef405735f764bf5c02b7cbaadba3c140728b66bd5391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053865"
---
# <a name="ctransformfilterbeginflush-method"></a>Método CTransformFilter.BeginFlush

El `BeginFlush` método comienza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Al principio de una operación de vaciado, el método [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) del pin de entrada llama a este método. Este método pasa la `BeginFlush` llamada de bajada.

Si la clase derivada usa un subproceso de trabajo para entregar ejemplos, debe descartar los datos en cola durante una operación de vaciado. Esto se puede hacer en el `BeginFlush` método o en el método [**EndFlush.**](ctransformfilter-endflush.md) Sin embargo, tenga en cuenta que las `BeginFlush` llamadas a no se sincronizan con el subproceso de streaming. Si el método descarta los datos en cola, el filtro debe tener cuidado de no procesar más datos entre `BeginFlush` las llamadas a y `BeginFlush` **EndFlush.** Para obtener más información, vea [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




