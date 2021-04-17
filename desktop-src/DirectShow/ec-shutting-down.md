---
description: El gráfico de filtro se está cerrando antes de ser destruido.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653555"
---
# <a name="ec_shutting_down"></a>\_cierre de EC \_

El gráfico de filtro se está cerrando antes de ser destruido.

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

Este evento no se envía a la aplicación. El administrador de gráficos de filtros lo envía a los distribuidores de complementos para notificarles que el gráfico se está cerrando. Las aplicaciones no pueden reemplazar la acción predeterminada de este evento.

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

 

 




