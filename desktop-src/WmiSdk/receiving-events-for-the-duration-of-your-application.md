---
description: Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recepción de eventos mientras dure la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082396"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="720bf-103">Recepción de eventos mientras dure la aplicación</span><span class="sxs-lookup"><span data-stu-id="720bf-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="720bf-104">Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario.</span><span class="sxs-lookup"><span data-stu-id="720bf-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="720bf-105">Estas aplicaciones se denominan "temporales" porque un consumidor temporal no recibe notificaciones de eventos cuando se apaga.</span><span class="sxs-lookup"><span data-stu-id="720bf-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="720bf-106">Un consumidor temporal llama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) en el script o [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en C++ para suscribirse a eventos en un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="720bf-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="720bf-107">La identidad asociada a esta suscripción es el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="720bf-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="720bf-108">Un consumidor de eventos temporal puede recibir notificaciones de forma asincrónica o semisincrónica tanto en scripts como en C++.</span><span class="sxs-lookup"><span data-stu-id="720bf-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="720bf-109">Por motivos de seguridad, es importante tener en cuenta que no se recomiendan las notificaciones de eventos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="720bf-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="720bf-110">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="720bf-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="720bf-111">Los consumidores de eventos tienen problemas de seguridad especiales.</span><span class="sxs-lookup"><span data-stu-id="720bf-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="720bf-112">Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="720bf-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="720bf-113">Para obtener más información sobre la recepción de notificaciones de eventos asincrónicos y semisincrónicos, consulte recibir notificaciones de eventos [asincrónicos](receiving-asynchronous-event-notifications.md) y [recibir notificaciones de eventos sincrónicos](receiving-synchronous-and-semisynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="720bf-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



