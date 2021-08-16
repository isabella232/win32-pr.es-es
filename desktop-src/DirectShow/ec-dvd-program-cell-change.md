---
description: Se envía cuando cambia el número de programa de DVD o el número de celda.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 90683bfff2cc6d3bbdd09c6a51dd7febbb9516f81738c513d446264c2f1ffd0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820400"
---
# <a name="ec_dvd_program_cell_change"></a>CAMBIO \_ DE CELDA DEL PROGRAMA DE DVD DE \_ \_ \_ EC

Se envía cuando cambia el número de programa de DVD o el número de celda.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Nuevo número de programa.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Nuevo número de celda.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este evento está deshabilitado de forma predeterminada. Para habilitar este evento, llame a [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y establezca la opción **\_ DVD NotifyPositionChange** en **TRUE.**

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

 

 




