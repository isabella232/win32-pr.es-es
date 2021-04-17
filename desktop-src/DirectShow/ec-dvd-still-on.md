---
description: Indica el principio de cualquier todavía (PGC, Cell o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
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
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653404"
---
# <a name="ec_dvd_still_on"></a>\_DVD \_ de EC todavía \_ encendido

Indica el principio de cualquier todavía (PGC, Cell o VOBU).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor booleano (**bool**) que indica si los botones están disponibles. Cero (0) indica que los botones están disponibles, por lo que el método [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) no funcionará. Uno (1) indica que no hay botones disponibles, por lo que **IDvdControl2:: StillOff** funcionará.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **DWORD** que indica el número de segundos que sigue siendo el último. 0xFFFFFFFF indica un infinito fijo, lo que significa esperar hasta que el usuario presione un botón o hasta que la aplicación llame a [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todas las combinaciones de botones y siguen siendo posibles (botones en con la opción con el mismo botón activado, botones en con todavía desactivado, botón desactivado con el botón sin conexión).

Este evento se desencadena en todos los dominios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




