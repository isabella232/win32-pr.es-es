---
description: 'Método CRenderedInputPin.EndFlush: el método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin::EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Método CRenderedInputPin.EndFlush (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098923"
---
# <a name="crenderedinputpinendflush-method"></a>Método CRenderedInputPin.EndFlush

El `EndFlush` método finaliza una operación de vaciado. Este método implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error de lo contrario.

## <a name="remarks"></a>Comentarios

Este método borra los eventos [**EC \_ COMPLETE pendientes.**](ec-complete.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amextra.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRenderedInputPin (clase)**](crenderedinputpin.md)
</dt> </dl>

 

 




