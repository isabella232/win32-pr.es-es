---
description: El reloj de referencia ha cambiado.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6a1346c4d445245e62c4823edb4f2cc5accfcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680261"
---
# <a name="ec_clock_changed"></a>reloj de EC \_ \_ cambiado

El reloj de referencia ha cambiado.

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

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

El administrador de gráficos de filtros envía este evento cuando se llama a su método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




