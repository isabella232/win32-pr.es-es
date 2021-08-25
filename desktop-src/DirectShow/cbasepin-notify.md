---
description: 'Método CBasePin.Notify: el método Notify notifica al pin que se solicita un cambio de calidad. Este método implementa el método IQualityControl::Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin.Notify (Amfilter.h)
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
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910445"
---
# <a name="cbasepinnotify-method"></a>Método CBasePin.Notify

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

Puntero a la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.

</dd> <dt>

*Q* 
</dt> <dd>

Especifica una estructura [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La clase base devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

Los pines de salida deben invalidar este método para aceptar mensajes de control de calidad.

Si se instaló un administrador de calidad externo (vea [**CBasePin::SetSink**](cbasepin-setsink.md)), pase el mensaje a ese administrador de calidad. De lo contrario, el filtro debe controlar el propio mensaje o pasar el mensaje ascendente. Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




