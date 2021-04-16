---
description: 'El \_ método get Rate recupera la velocidad de reproducción. Este método implementa el método de velocidad IMediaPosition:: get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Método CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679547"
---
# <a name="cpospassthruget_rate-method"></a>CPosPassThru. Get \_ Rate (método)

El `get_Rate` método recupera la velocidad de reproducción. Este método implementa el método de [**\_ velocidad IMediaPosition:: get**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Rate(
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

 

 




