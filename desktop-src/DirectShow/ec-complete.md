---
description: Se han representado todos los datos de una secuencia determinada.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680257"
---
# <a name="ec_complete"></a>EC \_ completado

Se han representado todos los datos de una secuencia determinada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Estado de la secuencia al finalizar. Si no se produjo ningún error durante la reproducción, el valor es S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Cero o un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

De forma predeterminada, el administrador de gráficos de filtro no reenvía este evento a la aplicación. Sin embargo, después de que se **\_ completen** todas las secuencias del informe de gráficos, el administrador de gráficos de filtros publica un evento de **EC \_ Complete** independiente en la aplicación.

Si la acción predeterminada está deshabilitada para este evento, la aplicación recibe todos los eventos de **\_ finalización de EC** de los representadores.

## <a name="remarks"></a>Observaciones

Un filtro de representador envía este evento cuando recibe un aviso de final de secuencia. (El final de la secuencia se señaliza a través del método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ). El filtro envía exactamente un evento de **\_ finalización de EC** para cada flujo. El filtro debe procesar cualquier ejemplo pendiente antes de enviar el evento. Al detener un representador, se restablece cualquier estado de final de secuencia que se almacenó en caché.

Si el representador está en pausa, no envía la **\_ finalización de EC** hasta que se llama al método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) . Además, sigue enviando eventos de **\_ finalización de EC** para cada transición de la pausa a la ejecución hasta que el filtro se detenga o se vacíe.

Los filtros establecen el parámetro *lParam2* en un puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Si la acción predeterminada está habilitada, el administrador de gráficos de filtro establece este parámetro en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Representadores de vídeo alternativos](alternative-video-renderers.md)
</dt> </dl>

 

 




