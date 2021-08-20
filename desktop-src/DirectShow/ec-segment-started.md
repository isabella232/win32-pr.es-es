---
description: Se ha iniciado un nuevo segmento.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015923"
---
# <a name="ec_segment_started"></a>EC \_ SEGMENT \_ STARTED

Se ha iniciado un nuevo segmento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **REFERENCE \_ TIME**) Puntero a un valor REFERENCE TIME que especifica el tiempo de flujo acumulado desde el inicio del segmento, en \* unidades de 100 nanosegundos. **\_**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Número de segmento (basado en cero).

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Este evento no se envía a la aplicación. Las aplicaciones no pueden invalidar la acción predeterminada para este evento.

## <a name="remarks"></a>Comentarios

Si un filtro enviará una [**EC \_ END OF \_ \_ SEGMENT**](ec-end-of-segment.md) al final de un segmento, envía este evento al principio del segmento. El administrador de gráficos de filtros usa esta notificación de eventos para calcular cuántas notificaciones EC END OF SEGMENT debe esperar \_ \_ al final del \_ segmento.

De forma predeterminada, los filtros no envían eventos [**EC \_ END OF \_ \_ SEGMENT**](ec-end-of-segment.md) al final de segmentos y, por lo tanto, no deben enviar este evento. Para obtener más información, [**vea IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

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

 

 




