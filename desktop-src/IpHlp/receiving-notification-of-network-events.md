---
description: Utilice las siguientes funciones para asegurarse de que una aplicación recibe la notificación de ciertos eventos de red.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Recepción de notificaciones de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686707"
---
# <a name="receiving-notification-of-network-events"></a>Recepción de notificaciones de eventos de red

Utilice las siguientes funciones para asegurarse de que una aplicación recibe la notificación de ciertos eventos de red.

Utilice la función [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar la notificación de cualquier cambio que se produzca en la asignación entre las direcciones IP y las interfaces en el equipo local.

Del mismo modo, la función [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permite a una aplicación solicitar la notificación de cualquier cambio que se produzca en la tabla de enrutamiento IP.

Las notificaciones proporcionadas por estas funciones no especifican lo que ha cambiado; simplemente especifican que algo ha cambiado. Use otras funciones auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) y [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), para determinar la naturaleza exacta del cambio.

 

 



