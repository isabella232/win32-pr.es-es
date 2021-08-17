---
description: Use las siguientes funciones para asegurarse de que una aplicación recibe la notificación de determinados eventos de red.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Recepción de notificaciones de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146618"
---
# <a name="receiving-notification-of-network-events"></a>Recepción de notificaciones de eventos de red

Use las siguientes funciones para asegurarse de que una aplicación recibe la notificación de determinados eventos de red.

Use la [**función NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar la notificación de cualquier cambio que se produzca en la asignación entre direcciones IP e interfaces en el equipo local.

De forma similar, [**la función NotifyRouteChange permite**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) a una aplicación solicitar la notificación de cualquier cambio que se produzca en la tabla de enrutamiento IP.

Las notificaciones proporcionadas por estas funciones no especifican lo que ha cambiado. simplemente especifican que algo ha cambiado. Use otras funciones del asistente de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) y [**GetBestRoute,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)para determinar la naturaleza exacta del cambio.

 

 



