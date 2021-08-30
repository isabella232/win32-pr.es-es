---
description: El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método invalida el método CBasePin::EndOfStream.
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Método CRendererInputPin.EndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e8f292016d24de69f71f91391c3c0d028c05e9cfa9c9057509877424ab02c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908305"
---
# <a name="crendererinputpinendofstream-method"></a>Método CRendererInputPin.EndOfStream

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método invalida el [**método CBasePin::EndOfStream.**](cbasepin-endofstream.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 




