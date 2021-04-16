---
description: El tamaño de vídeo nativo ha cambiado.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680234"
---
# <a name="ec_video_size_changed"></a>tamaño de vídeo de EC \_ \_ \_ cambiado

El tamaño de vídeo nativo ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Palabra de orden inferior especifica el nuevo ancho, en píxeles. Palabra de orden superior especifica el nuevo alto, en píxeles.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Los representadores de vídeo pueden enviar este evento si detectan un cambio en el tamaño de vídeo nativo.

El [representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) y el [representador de combinación de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) envían este evento en modo de ventana, pero no en modo sin ventanas ni en modo sin procesar. Para obtener más información sobre el modo de ventana en VMR, consulte [representación de vídeo](video-rendering.md).

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

 

 




