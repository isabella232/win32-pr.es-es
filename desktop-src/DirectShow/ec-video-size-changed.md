---
description: El tamaño del vídeo nativo ha cambiado.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da9fc430b8d36a61b90f567f082c7224765a702549d050f11555c8e55c387a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792385"
---
# <a name="ec_video_size_changed"></a>CAMBIO \_ EN EL TAMAÑO DEL VÍDEO DE \_ \_ EC

El tamaño del vídeo nativo ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) WORD de orden bajo especifica el nuevo ancho, en píxeles; WORD de orden superior especifica el nuevo alto, en píxeles.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Los representadores de vídeo pueden enviar este evento si detectan un cambio en el tamaño del vídeo nativo.

El representador de mezcla de vídeo [7](video-mixing-renderer-filter-7.md) (VMR-7) y el representador de mezcla de vídeo [9](video-mixing-renderer-filter-9.md) (VMR-9) envían este evento en modo de ventana, pero no en modo sin ventanas ni en modo sin representación. Para obtener más información sobre el modo de ventana en VMR, vea [Video Rendering](video-rendering.md).

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

 

 




