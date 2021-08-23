---
description: El método NotifyEvent envía una notificación de eventos al administrador de gráficos de filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Método CBaseFilter.NotifyEvent (Amfilter.h)
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
ms.openlocfilehash: e21ab1275aba05331055b7a38631f8c98ae65476aacf8f17073ed1dc45c90bf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640315"
---
# <a name="cbasefilternotifyevent-method"></a>Método CBaseFilter.NotifyEvent

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

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El administrador de gráficos de filtros no acepta notificaciones de eventos.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | El filtro no tiene un puntero a la [**interfaz IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)<br/> |



 

## <a name="remarks"></a>Comentarios

Para obtener una lista de códigos de notificación y valores de parámetros, vea [Códigos de notificación de eventos](event-notification-codes.md).

En la clase base, si el código de evento es EC COMPLETE, el método establece el parámetro EventParam2 en un puntero a la interfaz \_ [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) filtro. 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




