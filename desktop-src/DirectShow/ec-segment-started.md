---
description: Se ha iniciado un nuevo segmento.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653375"
---
# <a name="ec_segment_started"></a>segmento de EC \_ \_ iniciado

Se ha iniciado un nuevo segmento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **Reference \_ Time** \* ) puntero en un valor de **\_ tiempo de referencia** que especifica el tiempo de flujo acumulado desde el inicio del segmento, en unidades de 100-nanosegundos.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Número de segmento (basado en cero).

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Este evento no se envía a la aplicación. Las aplicaciones no pueden invalidar la acción predeterminada para este evento.

## <a name="remarks"></a>Observaciones

Si un filtro va a enviar [**un \_ final \_ de \_ segmento de EC**](ec-end-of-segment.md) al final de un segmento, envía este evento al principio del segmento. Filter Graph Manager usa esta notificación de eventos para calcular el número \_ \_ de notificaciones de fin de segmento de EC \_ que debería esperar al final del segmento.

De forma predeterminada, los filtros no envían eventos [**\_ \_ de fin de \_ segmento de EC**](ec-end-of-segment.md) al final de los segmentos y, por tanto, no deben enviar este evento. Para obtener más información, vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

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

 

 




