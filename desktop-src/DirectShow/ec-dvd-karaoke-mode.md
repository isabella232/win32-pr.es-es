---
description: Indica que el navegador de DVD ha empezado a reproducir o ha terminado de reproducir los datos de la máquina.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246572"
---
# <a name="ec_dvd_karaoke_mode"></a>MODO \_ EC DVD DVD \_ \_ DVD

Indica que el navegador [de DVD ha](data-flow-in-the-dvd-navigator.md) empezado a reproducir o ha terminado de reproducir los datos de la máquina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor booleano. Si **es TRUE,** se reproduce una pista de track. De lo contrario, no se reproduce ninguna pista de track.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El reproductor de DVD señala este evento cada vez que cambia de dominio.

Este evento se genera en todos los dominios de DVD.

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

 

 




