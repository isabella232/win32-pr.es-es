---
description: 'EC_DVD_VOBU_Timestamp: se envía cuando el navegador de DVD analiza un paquete PCI.'
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246489"
---
# <a name="ec_dvd_vobu_timestamp"></a>Marca de \_ tiempo DE VOBU de DVD \_ de EC \_

Se envía cuando [el navegador de DVD](dvd-navigator-filter.md) analiza un paquete PCI.

Los datos del evento son la marca de tiempo de la unidad de objeto de vídeo (VOBU) más reciente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Contiene el **DWORD** de orden bajo de la marca de tiempo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Contiene el **DWORD** de orden superior de la marca de tiempo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento está deshabilitado de forma predeterminada. Para habilitar este evento, llame a [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **\_ EnableLoggingEvents** de DVD en **TRUE.**

Reconstruye la marca de tiempo como se muestra a continuación:


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



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

 

 




