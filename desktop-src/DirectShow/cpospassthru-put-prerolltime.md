---
description: El \_ método put PrerollTime establece la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaPosition::p UT \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Método CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660815"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru. put \_ PrerollTime (método)

El `put_PrerollTime` método establece la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el método [**IMediaPosition::p UT \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*llTime* 
</dt> <dd>

Tiempo de preplantación, en segundos.

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

 

 




