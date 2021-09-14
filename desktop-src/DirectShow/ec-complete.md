---
description: Se han representado todos los datos de una secuencia determinada.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061195"
---
# <a name="ec_complete"></a>EC \_ COMPLETE

Se han representado todos los datos de una secuencia determinada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Estado de la secuencia al finalizar. Si no se ha producido ningún error durante la reproducción, el valor es S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Cero, o un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

De forma predeterminada, el administrador de gráficos de filtro no reenvía este evento a la aplicación. Sin embargo, después de todas las secuencias del informe de grafo **EC \_ COMPLETE,** el administrador de gráficos de filtro envía un evento **EC \_ COMPLETE** independiente a la aplicación.

Si la acción predeterminada está deshabilitada para este evento, la aplicación recibe todos los eventos **EC \_ COMPLETE** de los representadores.

## <a name="remarks"></a>Observaciones

Un filtro de representador envía este evento cuando recibe un aviso de fin de flujo. (El final de la secuencia se señala a través [**del método IPin::EndOfStream).**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) El filtro envía exactamente un **evento EC \_ COMPLETE** para cada secuencia. El filtro debe procesar los ejemplos pendientes antes de enviar el evento. Al detener un representador, se restablece cualquier estado de fin de flujo almacenado en caché.

Si el representador está en pausa, no envía **EC \_ COMPLETE** hasta que se llama al método [**IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) Además, continúa con el envío de eventos **\_ EC COMPLETE** para cada transición de pausa a ejecución, hasta que el filtro se detiene o se vacía.

Los filtros establecen *el parámetro lParam2* en un [**puntero IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Si la acción predeterminada está habilitada, el administrador de gráficos de filtro establece este parámetro en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Representadores de vídeo alternativos](alternative-video-renderers.md)
</dt> </dl>

 

 




