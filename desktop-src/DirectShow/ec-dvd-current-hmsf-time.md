---
description: Indica la hora actual, en formato DVD \_ HMSF \_ TIMECODE, con respecto al inicio del título. Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973815"
---
# <a name="ec_dvd_current_hmsf_time"></a>EC \_ DVD \_ CURRENT \_ HMSF \_ TIME

Indica la hora actual, en [**formato DVD \_ HMSF \_ TIMECODE,**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) con respecto al inicio del título. Este evento se desencadena al principio de cada VOBU, que se produce cada 0,4 a 1,0 segundos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor ULONG que contiene la estructura \_ TIMECODE de DVD HMSF. \_ Asigne lParam1 a una variable ULONG y, a continuación, conste de esa variable a UN CÓDIGO DE TIEMPO HMSF de DVD para acceder a \_ \_ sus valores.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor ULONG que contiene una unión de [**MARCAS DE CÓDIGO DE TIEMPO \_ \_ de DVD.**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)

</dd> </dl>

## <a name="remarks"></a>Observaciones

El formato TIMECODE de DVD HMSF está pensado para reemplazar el formato BCD antiguo que se devuelve en los eventos \_ \_ EC DVD CURRENT \_ \_ \_ TIME. Los códigos de tiempo de HMSF son más fáciles de trabajar. Para que el navegador envíe eventos \_ ACTUALES DE HORA DE HMSF de DVD EC en lugar de eventos \_ \_ EC DVD CURRENT \_ \_ \_ \_ TIME, una aplicación debe llamar a `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Cuando se establece esta marca, el navegador también esperará que todos los parámetros de tiempo de los métodos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) se pasen como \_ \_ TIMECOD de DVD HMSF.

Este evento se genera en los dominios de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




