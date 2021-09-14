---
description: El reloj de referencia ha cambiado.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f6a1346c4d445245e62c4823edb4f2cc5accfcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061200"
---
# <a name="ec_clock_changed"></a>CAMBIO \_ DEL RELOJ DE LA \_ EC

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

El administrador de gráficos de filtros envía este evento cuando se llama a su método [**IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




