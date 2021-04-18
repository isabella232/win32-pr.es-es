---
description: 'El método ConnectedIMemInputPin recupera un puntero al pin de entrada de nivel inferior. Este método devuelve la variable miembro CBaseOutputPin:: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Método CTransInPlaceOutputPin. ConnectedIMemInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660359"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>CTransInPlaceOutputPin. ConnectedIMemInputPin, método

El `ConnectedIMemInputPin` método recupera un puntero al pin de entrada de nivel inferior. Este método devuelve la variable miembro [**CBaseOutputPin:: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .

## <a name="syntax"></a>Sintaxis


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en el PIN de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




