---
description: Notifica a un filtro la ventana del representador de vídeo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161535"
---
# <a name="ec_notify_window"></a>VENTANA \_ DE NOTIFICACIÓN DE \_ EC

Notifica a un filtro la ventana del representador de vídeo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Identificador de la ventana.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Este evento lo usa internamente DirectShow. El administrador de gráficos de filtros no pasa este evento a la aplicación. Las aplicaciones no pueden invalidar la acción predeterminada para este evento.

## <a name="remarks"></a>Observaciones

Cuando se conecta un representador de vídeo, comprueba si el pin de salida ascendente admite la [**interfaz IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) Si es así, el representador envía este evento al filtro ascendente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




