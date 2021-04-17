---
description: El método BeginFlush inicia una operación de vaciado.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter. BeginFlush (Transfrm. h)
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
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660304"
---
# <a name="ctransformfilterbeginflush-method"></a>CTransformFilter. BeginFlush, método

El `BeginFlush` método inicia una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Al inicio de una operación de vaciado, el método [**CTransformInputPin:: BeginFlush**](ctransforminputpin-beginflush.md) del PIN de entrada llama a este método. Este método pasa la `BeginFlush` llamada de nivel inferior.

Si la clase derivada usa un subproceso de trabajo para proporcionar ejemplos, debe descartar todos los datos en cola durante una operación de vaciado. Esto puede hacerse en el `BeginFlush` método o en el método [**EndFlush**](ctransformfilter-endflush.md) . Sin embargo, tenga en cuenta que las llamadas a `BeginFlush` no se sincronizan con el subproceso de streaming. Si el `BeginFlush` método descarta los datos en cola, el filtro debe tener cuidado de no procesar más datos entre las `BeginFlush` llamadas a y **EndFlush** . Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




