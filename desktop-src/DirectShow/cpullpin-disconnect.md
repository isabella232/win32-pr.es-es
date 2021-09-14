---
description: El método Disconnect interrumpe la conexión con el pin de salida.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Método CPullPin.Disconnect (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063315"
---
# <a name="cpullpindisconnect-method"></a>Método CPullPin.Disconnect

El `Disconnect` método interrumpe la conexión con el pin de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método interrumpe cualquier conexión realizada en [**el método CPullPin::Conectar.**](cpullpin-connect.md) Llame a este método dentro del [**método IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) (Si el pin deriva de [**CBasePin,**](cbasepin.md)invalide [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) para llamar a este método).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




