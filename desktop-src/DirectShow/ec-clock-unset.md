---
description: El proveedor de reloj se desconectó.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061199"
---
# <a name="ec_clock_unset"></a>EC \_ CLOCK \_ UNSET

El proveedor de reloj se desconectó.

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

El Administrador Graph filtro elige un nuevo reloj de referencia en el siguiente comando de pausa o ejecución. También reenvía el evento a la aplicación.

## <a name="remarks"></a>Observaciones

KSProxy señala este evento cuando se desconecta la marca de un filtro que proporciona el reloj.

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

 

 




