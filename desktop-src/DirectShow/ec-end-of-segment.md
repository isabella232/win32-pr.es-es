---
description: Se alcanzó el final de un segmento.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246453"
---
# <a name="ec_end_of_segment"></a>FIN \_ DE SEGMENTO DE \_ \_ EC

Se alcanzó el final de un segmento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **REFERENCE \_ TIME**) Puntero a un valor DE TIEMPO DE REFERENCIA que especifica el tiempo de flujo acumulado desde el inicio del segmento, en \* unidades de 100 nanosegundos. **\_**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Número de segmento (de base cero).

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtros comprueba el número de eventos **\_ EC END OF \_ \_ SEGMENT** con respecto al número de [**eventos EC SEGMENT \_ \_ STARTED.**](ec-segment-started.md) Si coinciden, reenvía el evento **\_ EC END OF \_ \_ SEGMENT** a la aplicación. Las aplicaciones no pueden invalidar la acción predeterminada para este evento.

## <a name="remarks"></a>Observaciones

Este código de evento admite bucles sin problemas. Cuando una llamada al método [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) incluye la marca segmento AM SEEKING, el filtro de origen envía este código de evento en lugar de llamar a \_ \_ [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 




