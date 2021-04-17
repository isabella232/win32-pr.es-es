---
description: 'El método Notify notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método IQualityControl:: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670908"
---
# <a name="cbasepinnotify-method"></a>CBasePin. Notify (método)

El `Notify` método notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

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

Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.

</dd> <dt>

*respuestas* 
</dt> <dd>

Especifica una estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La clase base devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Observaciones

Los pin de salida deben invalidar este método para aceptar mensajes de control de calidad.

Si se instaló un administrador de calidad externo (consulte [**CBasePin:: SetSink**](cbasepin-setsink.md)), pase el mensaje a ese administrador de calidad. De lo contrario, el filtro debe controlar el propio mensaje o pasar el mensaje ascendente. Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




