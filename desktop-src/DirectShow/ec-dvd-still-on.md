---
description: Indica el principio de cualquier todavía (PGC, Cell o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 801db7f1e14002aa6333b18349e259e40928a0cd45958c0e1aa618d1d1143be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303336"
---
# <a name="ec_dvd_still_on"></a>DVD \_ DE EC TODAVÍA EN \_ \_ ON

Indica el principio de cualquier todavía (PGC, Cell o VOBU).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **booleano (BOOL)** que indica si hay botones disponibles. Cero (0) indica que los botones están disponibles, por lo que el método [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) no funcionará. Uno (1) indica que no hay botones disponibles, por lo **que IDvdControl2::StillOff** funcionará.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor DWORD** que indica el número de segundos que seguirá durando. 0xFFFFFFFF indica un valor infinito, lo que significa esperar hasta que el usuario presione un botón o hasta que la aplicación llame a [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todas las combinaciones de botones y siguen siendo posibles (botones encendidos con todavía encendido, botones encendidos con todavía desactivados, botón apagado con todavía encendido, botón desactivado con todavía desactivado).

Este evento se genera en todos los dominios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




