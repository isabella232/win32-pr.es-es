---
description: Se envía cuando cambia el valor de un registro de parámetros del sistema (SPRM).
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653405"
---
# <a name="ec_dvd_sprm_change"></a>\_Cambio de \_ SPRM de DVD de EC \_

Se envía cuando cambia el valor de un registro de parámetros del sistema (SPRM).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Índice de base cero del valor de SPRM que cambió.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Los 16 bits inferiores contienen el nuevo valor SPRM.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento está deshabilitado de forma predeterminada. Para habilitar este evento, llame a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **true**.

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

[**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




