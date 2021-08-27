---
description: Un representador de vídeo requiere un repintado.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102795"
---
# <a name="ec_repaint"></a>EC \_ REPAINT

Un representador de vídeo requiere un repintado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada del representador de vídeo, o **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El *parámetro lParam1* podría especificar el pin de entrada del representador de vídeo. Si es así, el administrador de gráficos de filtros busca el pin de salida conectado a ese pin y lo consulta para la [**interfaz IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) Si el pin de salida admite **IMediaEventSink,** el administrador de gráficos de filtro llama a [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) con el código de evento \_ EC REPAINT. Esto ofrece al filtro ascendente la oportunidad de volver a enviar el último ejemplo.

Si *lParam1* es **NULL** o si el pin no admite [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)o si se produce un error en el método [**Notify,**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) el administrador de gráficos de filtro controla el evento \_ EC REPAINT por sí mismo. Su comportamiento depende del estado del gráfico:

-   En ejecución: omite el evento . (El representador recibirá el ejemplo siguiente en la secuencia).
-   En pausa: busca el gráfico en su ubicación actual, lo que vacía el filtro y vuelve a poner en cola los datos.
-   Detenido: pausa y detiene el gráfico, con lo que vuelve a poner en cola los datos.

De forma predeterminada, el administrador de gráficos de filtro no pasa este evento a la aplicación.

## <a name="remarks"></a>Comentarios

Los representadores de vídeo envían este mensaje cuando reciben un [**mensaje \_ WM PAINT**](/windows/desktop/gdi/wm-paint) y no tienen datos que mostrar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

