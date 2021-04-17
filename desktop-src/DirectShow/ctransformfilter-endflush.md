---
description: El método EndFlush finaliza una operación de vaciado.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter. EndFlush (Transfrm. h)
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
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660622"
---
# <a name="ctransformfilterendflush-method"></a>CTransformFilter. EndFlush, método

El `EndFlush` método finaliza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Al final de una operación de vaciado, el método [**CTransformInputPin:: EndFlush**](ctransforminputpin-endflush.md) del PIN de entrada llama a este método. Este método pasa la `EndFlush` llamada de nivel inferior.

Si la clase derivada utiliza un subproceso de trabajo para proporcionar ejemplos, debe descartar todos los datos en cola antes de enviar la `EndFlush` llamada de nivel inferior. Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




