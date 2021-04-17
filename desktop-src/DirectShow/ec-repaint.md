---
description: Un representador de vídeo requiere volver a pintar.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689955"
---
# <a name="ec_repaint"></a>repintar EC \_

Un representador de vídeo requiere volver a pintar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada del representador de vídeo, o **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El parámetro *lParam1* podría especificar el PIN de entrada del representador de vídeo. Si es así, el administrador de gráficos de filtro busca el PIN de salida conectado a ese pin y lo consulta para la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Si el PIN de salida admite **IMediaEventSink**, el administrador de gráficos de filtros llama a [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) con el \_ código de evento de Repaint de EC. Esto proporciona al filtro de nivel superior la oportunidad de volver a enviar el último ejemplo.

Si *lParam1* es **null**, o si el PIN no admite [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), o si se produce un error en el método [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) , el administrador de gráficos de filtro controla el \_ evento re Repaint por sí mismo. Su comportamiento depende del estado del gráfico:

-   Running: omite el evento. (El representador recibirá el siguiente ejemplo en el flujo).
-   En pausa: busca el gráfico en su ubicación actual, con lo que se vacía el filtro y se vuelven a poner en cola los datos.
-   Stopped: pausa y detiene el gráfico, con lo que se vuelven a poner en cola los datos.

De forma predeterminada, el administrador de gráficos de filtro no pasa este evento a la aplicación.

## <a name="remarks"></a>Observaciones

Los representadores de vídeo envían este mensaje cuando reciben un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) y no tienen datos para mostrar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

