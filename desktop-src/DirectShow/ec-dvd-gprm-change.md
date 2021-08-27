---
description: Se envía cuando cambia el valor de un registro de parámetros general (GPRM).
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: b1d6613475a3c61640a7b6b5f5c53bc1baab52c1a69ec3d3c8b7a0e32f91928c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079155"
---
# <a name="ec_dvd_gprm_change"></a>EC \_ DVD \_ GPRM \_ Change

Se envía cuando cambia el valor de un registro de parámetros general (GPRM).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Índice de base cero del valor GPRM que ha cambiado.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Los 16 bits inferiores contienen el nuevo valor gprm.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este evento está deshabilitado de forma predeterminada. Para habilitar este evento, llame a [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **DVD \_ EnableLoggingEvents** en **TRUE.**

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
</dt> <dt>

[**IDvdInfo2::GetAllGPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




