---
description: El representador de vídeo está cambiando del modo de pantalla completa.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680312"
---
# <a name="ec_fullscreen_lost"></a>\_pantalla completa de EC \_ perdida

El representador de vídeo está cambiando del modo de pantalla completa.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador de vídeo, o **null**.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Cuando el [representador de pantalla completa](full-screen-renderer-filter.md) pierde la activación, envía este evento. Cuando otro representador de vídeo cambia de modo de pantalla completa, el administrador de gráficos de filtros envía este evento, en respuesta a un evento de [**\_ activación de EC**](ec-activate.md) del representador.

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

 

 




