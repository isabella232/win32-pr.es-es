---
description: Señala la hora actual, en \_ formato de código de tiempo HMSF de DVD \_ , con respecto al inicio del título. Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690083"
---
# <a name="ec_dvd_current_hmsf_time"></a>\_hora de \_ \_ HMSF actual del DVD \_ de EC

Señala la hora actual, en formato de [**\_ código de \_ tiempo HMSF de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) , con respecto al inicio del título. Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor ULONG que contiene la estructura de \_ código de tiempo HMSF de DVD \_ . Asigne lParam1 a una variable ULONG y, a continuación, convierta esa variable en un \_ \_ código de tiempo HMSF de DVD para tener acceso a sus valores.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor ULONG que contiene una Unión de [**\_ \_ marcas de código de tiempo de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El formato de código de tiempo de HMSF de DVD \_ \_ está pensado para reemplazar el formato BCD anterior que se devuelve en \_ \_ los eventos de hora actual de DVD de EC \_ . Los códigos de tiempo de HMSF son más fáciles de usar. Para que el navegador envíe \_ eventos de \_ \_ \_ tiempo de HMSF actual de DVD de EC en lugar de \_ eventos de hora actual de DVD de EC \_ \_ , una aplicación debe llamar a `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Cuando se establece esta marca, el navegador también espera que todos los parámetros de tiempo de los métodos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) se pasen como códigos de tiempo de HMSF de DVD \_ \_ .

Este evento se desencadena en los dominios de título.

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

 

 




