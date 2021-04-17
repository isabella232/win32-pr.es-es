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
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="86376-103">Recepción de notificaciones de eventos de red</span><span class="sxs-lookup"><span data-stu-id="86376-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="86376-104">Utilice las siguientes funciones para asegurarse de que una aplicación recibe la notificación de ciertos eventos de red.</span><span class="sxs-lookup"><span data-stu-id="86376-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="86376-105">Utilice la función [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar la notificación de cualquier cambio que se produzca en la asignación entre las direcciones IP y las interfaces en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="86376-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="86376-106">Del mismo modo, la función [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permite a una aplicación solicitar la notificación de cualquier cambio que se produzca en la tabla de enrutamiento IP.</span><span class="sxs-lookup"><span data-stu-id="86376-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="86376-107">Las notificaciones proporcionadas por estas funciones no especifican lo que ha cambiado; simplemente especifican que algo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="86376-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="86376-108">Use otras funciones auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) y [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), para determinar la naturaleza exacta del cambio.</span><span class="sxs-lookup"><span data-stu-id="86376-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



