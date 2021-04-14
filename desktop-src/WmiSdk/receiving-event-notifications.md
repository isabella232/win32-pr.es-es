---
description: Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos. Los consumidores de eventos usan consultas de eventos para especificar los eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648282"
---
# <a name="receiving-event-notifications"></a><span data-ttu-id="cf1e2-104">Recibir notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="cf1e2-104">Receiving Event Notifications</span></span>

<span data-ttu-id="cf1e2-105">Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="cf1e2-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="cf1e2-106">Los consumidores de eventos usan consultas de eventos para especificar los eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.</span><span class="sxs-lookup"><span data-stu-id="cf1e2-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="cf1e2-107">Los [consumidores temporales](receiving-events-for-the-duration-of-your-application.md) colocan consultas en llamadas al método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="cf1e2-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="cf1e2-108">Los [consumidores de eventos permanentes](receiving-events-at-all-times.md) colocan consultas en la propiedad de **consulta** de una instancia de la clase del sistema [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1e2-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="cf1e2-109">Los [proveedores de eventos](writing-an-event-provider.md) usan consultas de eventos para registrarse para admitir uno o varios tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="cf1e2-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="cf1e2-110">Las consultas se colocan en la propiedad **EventQueryList** de una instancia de la clase del sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1e2-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="cf1e2-111">Todos los proveedores de eventos crean una instancia de **\_ \_ EventProviderRegistration** para registrarse con instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cf1e2-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="cf1e2-112">Para obtener más información, vea [registrar un proveedor de eventos](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cf1e2-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="cf1e2-113">Los consumidores y proveedores de eventos usan la [instrucción SELECT](select-statement-for-event-queries.md) y una cláusula WHERE relacionada para las consultas de eventos, además de una variedad de extensiones específicas del lenguaje de consulta de WMI (WQL).</span><span class="sxs-lookup"><span data-stu-id="cf1e2-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="cf1e2-114">Las extensiones se utilizan para proteger a los consumidores de la saturación con notificaciones que se producen con demasiada frecuencia para ser útiles.</span><span class="sxs-lookup"><span data-stu-id="cf1e2-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="cf1e2-115">Los consumidores que no requieren notificación cada vez que se produce un evento pueden especificar las siguientes cláusulas en sus consultas:</span><span class="sxs-lookup"><span data-stu-id="cf1e2-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="cf1e2-116">Cláusula [Within](within-clause.md)</span><span class="sxs-lookup"><span data-stu-id="cf1e2-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="cf1e2-117">[Group](group-clause.md) (cláusula)</span><span class="sxs-lookup"><span data-stu-id="cf1e2-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="cf1e2-118">Cláusula [having](having-clause.md)</span><span class="sxs-lookup"><span data-stu-id="cf1e2-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="cf1e2-119">Las cláusulas dentro de y HAVING afectan al tiempo de los eventos, y la cláusula GROUP hace que se envíe un evento representativo en lugar de un evento que se produce con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cf1e2-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



