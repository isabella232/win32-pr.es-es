---
description: El \_ método put CurrentPosition establece la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaPosition::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Método CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681148"
---
# <a name="cpospassthruput_currentposition-method"></a>CPosPassThru. put \_ CurrentPosition (método)

El `put_CurrentPosition` método establece la posición actual, en relación con la duración total de la secuencia. Este método implementa el método [**IMediaPosition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*llTime* 
</dt> <dd>

Nueva posición, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




