---
description: 'Método CBaseOutputPin.EndOfStream: el método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin::EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Método CBaseOutputPin.EndOfStream (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096153"
---
# <a name="cbaseoutputpinendofstream-method"></a>Método CBaseOutputPin.EndOfStream

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
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

 

 




