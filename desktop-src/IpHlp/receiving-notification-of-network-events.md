---
description: Use las siguientes funciones para asegurarse de que una aplicación recibe la notificación de determinados eventos de red.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Recepción de notificaciones de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160069"
---
# <a name="receiving-notification-of-network-events"></a>Recepción de notificaciones de eventos de red

Use las siguientes funciones para asegurarse de que una aplicación recibe la notificación de determinados eventos de red.

Use la [**función NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar la notificación de cualquier cambio que se produzca en la asignación entre direcciones IP e interfaces en el equipo local.

De forma similar, [**la función NotifyRouteChange permite**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) a una aplicación solicitar la notificación de cualquier cambio que se produzca en la tabla de enrutamiento IP.

Las notificaciones proporcionadas por estas funciones no especifican lo que ha cambiado; simplemente especifican que algo ha cambiado. Use otras funciones auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) y [**GetBestRoute,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)para determinar la naturaleza exacta del cambio.

 

 



