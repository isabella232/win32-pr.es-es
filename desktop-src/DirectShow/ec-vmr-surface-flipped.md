---
description: Se envía cuando el presentador del asignador VMR-7's ha llamado al método Flip de DirectDraw en la superficie que se está presentando. Esto permite que VMR mantenga su tabla de superficies DirectXVA sincronizada con la cadena de volteo de DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653755"
---
# <a name="ec_vmr_surface_flipped"></a>\_superficie EC \_ VMR \_ volteada

Se envía cuando el presentador del asignador VMR-7's ha llamado al método Flip de DirectDraw en la superficie que se está presentando. Esto permite que VMR mantenga su tabla de superficies DirectXVA sincronizada con la cadena de volteo de DirectDraw.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de estado devuelto por el método DirectDraw flip.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asignador personalizado: los presentadores de VMR-7 deben enviar este evento. Este evento no se reenvía a las aplicaciones y no se usa con los presentadores de asignador para VMR-9.

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

 

 




