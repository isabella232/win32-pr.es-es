---
description: 'Método CBaseInputPin.Notify: el método Notify notifica al pin que se solicita un cambio de calidad. Este método implementa el método IQualityControl::Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin.Notify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120003"
---
# <a name="cbaseinputpinnotify-method"></a>Método CBaseInputPin.Notify

El `Notify` método notifica al pin que se solicita un cambio de calidad. Este método implementa el [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSelf* 
</dt> <dd>

Puntero al filtro que envía el mensaje de control de calidad.

</dd> <dt>

*Q* 
</dt> <dd>

[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los filtros suelen pasar mensajes de control de calidad a un pin de salida ascendente, no a un pin de entrada. Por lo tanto, este método devuelve S \_ OK sin hacer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> </dl>

 

 




