---
description: 'Método CPosPassThru.GetRate: el método GetRate recupera la velocidad de reproducción. Este método implementa el método IMediaSeeking::GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Método CPosPassThru.GetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063335"
---
# <a name="cpospassthrugetrate-method"></a>Método CPosPassThru.GetRate

El `GetRate` método recupera la velocidad de reproducción. Este método implementa el [**método IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdRate* 
</dt> <dd>

Puntero a una variable que recibe la velocidad de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




