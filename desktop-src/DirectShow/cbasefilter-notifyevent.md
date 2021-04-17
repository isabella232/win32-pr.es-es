---
description: El método NotifyEvent envía una notificación de eventos al administrador de gráficos de filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Método CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661170"
---
# <a name="cbasefilternotifyevent-method"></a>CBaseFilter. NotifyEvent, método

El `NotifyEvent` método envía una notificación de eventos al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EventCode* 
</dt> <dd>

Código de notificación de eventos.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Primer parámetro del evento.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Segundo parámetro del evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | El administrador de gráficos de filtro no acepta notificaciones de eventos.<br/>                              |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Filter no tiene un puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de códigos de notificación y valores de parámetros, vea [códigos de notificación de eventos](event-notification-codes.md).

En la clase base, si el código de evento es EC \_ completo, el método establece el parámetro *EventParam2* en un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




