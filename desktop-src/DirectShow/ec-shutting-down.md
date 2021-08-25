---
description: El gráfico de filtros se está cerrando, antes de destruirse.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917a8f79b1a5201e50d0fcf2761a99b2801f75601f95ef866902492fb36065f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079115"
---
# <a name="ec_shutting_down"></a>EC \_ SHUTTING \_ DOWN

El gráfico de filtros se está cerrando, antes de destruirse.

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

Este evento no se envía a la aplicación. El administrador de gráficos de filtros lo envía a los distribuidores de complementos para notificarles que el grafo se está cerrando. Las aplicaciones no pueden invalidar la acción predeterminada de este evento.

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

 

 




