---
description: Se envía cuando el presentador del asignador de VMR-7 ha llamado al método DirectDraw Flip en la superficie que se presenta. Esto permite que vmr mantenga su tabla de superficies de DirectXVA sincronizada con la cadena de volteo de DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c352af01ee31728b41aa276d14ca64b7c3fa6770bb4c9328a8c4ee5e91bb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043355"
---
# <a name="ec_vmr_surface_flipped"></a>SUPERFICIE \_ DE VMR \_ DE EC \_ VOLTEADO

Se envía cuando el presentador del asignador de VMR-7 ha llamado al método DirectDraw Flip en la superficie que se presenta. Esto permite que vmr mantenga su tabla de superficies de DirectXVA sincronizada con la cadena de volteo de DirectDraw.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de estado devuelto por el método DirectDraw Flip.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los asignadores-presentadores personalizados para VMR-7 deben enviar este evento. Este evento no se reenvía a las aplicaciones y no se usa con los presentadores de asignador para VMR-9.

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

 

 




