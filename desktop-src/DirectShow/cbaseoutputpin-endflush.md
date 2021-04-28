---
description: 'Método CBaseOutputPin.EndFlush: el método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin::EndFlush.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Método CBaseOutputPin.EndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099513"
---
# <a name="cbaseoutputpinendflush-method"></a>Método CBaseOutputPin.EndFlush

El `EndFlush` método finaliza una operación de vaciado. Este método implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ UNEXPECTED.

## <a name="remarks"></a>Comentarios

Solo se debe llamar a este método en los pines de entrada, por lo que la implementación **de CBaseOutputPin** devuelve E \_ UNEXPECTED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




