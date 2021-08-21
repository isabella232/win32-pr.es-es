---
description: El método ConnectedIMemInputPin recupera un puntero al pin de entrada de bajada. Este método devuelve la variable miembro CBaseOutputPin::m \_ pInputPin.
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Método CTransInPlaceOutputPin.ConnectedIMemInputPin (Transip.h)
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
ms.openlocfilehash: 180cce9bc0d52c6e11bbd90b64cfe7d57d4dcc99eada3a794f924df6857c4698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076185"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>CTransInPlaceOutputPin.ConnectedIMemInputPin (método)

El `ConnectedIMemInputPin` método recupera un puntero a la patilla de entrada de nivel inferior. Este método devuelve la variable [**miembro CBaseOutputPin::m \_ pInputPin.**](cbaseoutputpin-m-pinputpin.md)

## <a name="syntax"></a>Sintaxis


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en el pin de entrada de bajada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceOutputPin (clase)**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




