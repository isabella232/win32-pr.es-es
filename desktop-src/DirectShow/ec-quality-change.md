---
description: El gráfico está quitando muestras para el control de calidad.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9c2b540a5740812050532d4d4e6e45fb334eaff9927148471aada09ab1a434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043365"
---
# <a name="ec_quality_change"></a>CAMBIO \_ DE CALIDAD DE \_ EC

El gráfico está quitando muestras para el control de calidad.

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

## <a name="remarks"></a>Comentarios

Un filtro envía este evento si quita muestras en respuesta a un mensaje de control de calidad. Envía el evento solo cuando ajusta el nivel de calidad, no para cada muestra que quita. Para obtener más información, vea [Administración de control de calidad.](quality-control-management.md)

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

 

 




