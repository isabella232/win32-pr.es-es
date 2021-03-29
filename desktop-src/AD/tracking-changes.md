---
title: Seguimiento de cambios
description: Algunas aplicaciones deben mantener la coherencia entre los datos específicos almacenados en el servicio de directorio de Active Directory y otros datos.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, seguimiento de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995054"
---
# <a name="tracking-changes"></a><span data-ttu-id="45449-104">Seguimiento de cambios</span><span class="sxs-lookup"><span data-stu-id="45449-104">Tracking Changes</span></span>

<span data-ttu-id="45449-105">Algunas aplicaciones deben mantener la coherencia entre los datos específicos almacenados en el servicio de directorio de Active Directory y otros datos.</span><span class="sxs-lookup"><span data-stu-id="45449-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="45449-106">Los demás datos se pueden almacenar en el directorio, en una tabla de SQL Server, en un archivo o en el registro.</span><span class="sxs-lookup"><span data-stu-id="45449-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="45449-107">Cuando cambian los datos almacenados en el directorio, es posible que sea necesario cambiar el resto de los datos para mantener la coherencia.</span><span class="sxs-lookup"><span data-stu-id="45449-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="45449-108">Las aplicaciones que tienen este requisito incluyen:</span><span class="sxs-lookup"><span data-stu-id="45449-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="45449-109">En esta sección no se tratan los mecanismos que usan las aplicaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="45449-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="45449-110">Se trata de aplicaciones que supervisan los cambios de directorio no con el fin de mantener datos coherentes entre almacenes independientes, pero como una herramienta de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="45449-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="45449-111">Aunque las aplicaciones de supervisión pueden usar los mismos mecanismos que admiten las aplicaciones de seguimiento de cambios, los siguientes mecanismos están diseñados específicamente para supervisar aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="45449-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="45449-112">Auditoría de seguridad.</span><span class="sxs-lookup"><span data-stu-id="45449-112">Security auditing.</span></span> <span data-ttu-id="45449-113">Al modificar la parte de la lista de control de acceso de sistema (SACL) de un descriptor de seguridad de objeto, puede hacer que los accesos al objeto de un controlador de dominio determinado generen registros de auditoría en el registro de eventos de seguridad de ese DC.</span><span class="sxs-lookup"><span data-stu-id="45449-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="45449-114">Puede auditar lecturas, escrituras o ambas cosas. puede auditar todo el objeto o atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="45449-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="45449-115">Para obtener más información, vea [recuperar la SACL de un objeto y la generación de](retrieving-an-objectampaposs-sacl.md) [Auditoría](/windows/desktop/SecAuthZ/audit-generation).</span><span class="sxs-lookup"><span data-stu-id="45449-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="45449-116">Registros de eventos.</span><span class="sxs-lookup"><span data-stu-id="45449-116">Event logging.</span></span> <span data-ttu-id="45449-117">Al modificar la configuración del registro en un controlador de dominio determinado, puede cambiar los tipos de eventos registrados en el registro de eventos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="45449-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="45449-118">En concreto, para registrar todas las modificaciones, establezca el valor **8 de acceso al directorio** en la siguiente clave del registro en 4.</span><span class="sxs-lookup"><span data-stu-id="45449-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="45449-119">Para obtener más información, vea [registro de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="45449-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="45449-120">Seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="45449-120">Event tracing.</span></span> <span data-ttu-id="45449-121">Windows 2000 presentó una API de seguimiento de eventos para el seguimiento y el registro de eventos interesantes en software o hardware.</span><span class="sxs-lookup"><span data-stu-id="45449-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="45449-122">El sistema operativo Windows, y Active Directory Domain Services en particular, admiten el uso del seguimiento de eventos para el planeamiento de la capacidad y el análisis detallado del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="45449-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="45449-123">Para obtener más información, vea [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) y [seguimiento de eventos en ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="45449-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="45449-124">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="45449-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="45449-125">Información general sobre las técnicas de Change Tracking</span><span class="sxs-lookup"><span data-stu-id="45449-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="45449-126">Notificaciones de cambio en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="45449-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="45449-127">Sondear los cambios mediante el control DirSync</span><span class="sxs-lookup"><span data-stu-id="45449-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="45449-128">Sondeo de cambios mediante USNChanged</span><span class="sxs-lookup"><span data-stu-id="45449-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 