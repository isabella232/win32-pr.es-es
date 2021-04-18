---
description: Indica que el navegador ha terminado de reproducirse el segmento especificado en una llamada a IDvdControl2::P layPeriodInTitleAutoStop.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679348"
---
# <a name="ec_dvd_playperiod_autostop"></a>\_detención de \_ PLAYPERIOD de DVD de EC \_

Indica que el navegador ha terminado de reproducirse el segmento especificado en una llamada a [**IDvdControl2::P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento se desencadena en el dominio de título.

Este evento también se envía cuando se cancela la reproducción antes de que el navegador finalice la reproducción del segmento especificado.

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
</dt> <dt>

[**IDvdControl2::P layPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




