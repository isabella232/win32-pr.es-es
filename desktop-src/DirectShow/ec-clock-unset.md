---
description: El proveedor de reloj se desconectó.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7bc9daecb9e39ca2d121c9fa903b2e4e8257e6247f28d718ca093b302cc2e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998225"
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

El Administrador Graph filtros elige un nuevo reloj de referencia en el siguiente comando de pausa o ejecución. También reenvía el evento a la aplicación.

## <a name="remarks"></a>Comentarios

KSProxy señala este evento cuando se desconecta el pin de un filtro que proporciona reloj.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




