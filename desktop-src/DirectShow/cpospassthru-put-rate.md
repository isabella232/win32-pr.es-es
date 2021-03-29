---
description: El \_ método de velocidad Put establece la velocidad de reproducción. Este método implementa el método de velocidad IMediaPosition::p UT \_ .
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Método CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678930"
---
# <a name="cpospassthruput_rate-method"></a>CPosPassThru. put ( \_ método de tasa)

El `put_Rate` método establece la velocidad de reproducción. Este método implementa el método de [**\_ velocidad IMediaPosition::p UT**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dRate* 
</dt> <dd>

Velocidad de reproducción. No debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ INVALIDARG si *dRate* es cero. De lo contrario, devuelve el valor **HRESULT** del PIN conectado.

## <a name="remarks"></a>Observaciones

Los tipos negativos indican reproducción inversa. No todos los medios serán compatibles con la reproducción inversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




