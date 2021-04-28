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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085163"
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

Si la clase derivada usa un subproceso de trabajo para entregar ejemplos, debe descartar los datos en cola durante una operación de vaciado. Esto se puede hacer en el `BeginFlush` método o en el método [**EndFlush.**](ctransformfilter-endflush.md) Sin embargo, tenga en cuenta que las `BeginFlush` llamadas a no se sincronizan con el subproceso de streaming. Si el método descarta los datos en cola, el filtro debe tener cuidado de no procesar más datos entre `BeginFlush` las llamadas a y `BeginFlush` **EndFlush.** Para obtener más información, [vea Data Flow para desarrolladores de filtros.](data-flow-for-filter-developers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




