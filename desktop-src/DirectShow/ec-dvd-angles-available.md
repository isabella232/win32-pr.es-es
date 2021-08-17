---
description: Indica si se reproduce un bloque angular y se pueden realizar cambios de ángulo.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e95c692aed8ac6c709ff0db1d6056fc59219fa73f5aa2e4cfb9b31b2c1a03d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015993"
---
# <a name="ec_dvd_angles_available"></a>ÁNGULOS \_ DE DVD EC \_ \_ DISPONIBLES

Indica si se reproduce un bloque angular y se pueden realizar cambios de ángulo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **booleano (BOOL)** que indica si se reproduce un bloque angular. Cero (0) indica que la reproducción no está en un bloque angular y que los ángulos no están disponibles, uno (1) indica que se reproduce un bloque angular y se pueden realizar cambios de ángulo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los cambios de ángulo no están restringidos a los bloques angulares y la demostración del cambio de ángulo solo se puede ver en un bloque angular.

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

 

 




