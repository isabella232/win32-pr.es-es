---
title: La base de información de administración (MIB) de SNMP
description: Una base de datos de información de administración (MIB) describe un conjunto de objetos administrados. Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene una DLL de agente de extensión que admite la MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774364"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="1c4a2-104">La base de información de administración (MIB) de SNMP</span><span class="sxs-lookup"><span data-stu-id="1c4a2-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="1c4a2-105">Una base de datos de información de administración (MIB) describe un conjunto de objetos administrados.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="1c4a2-106">Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene una DLL de agente de extensión que admite la MIB.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="1c4a2-107">Cada objeto administrado en una MIB tiene un identificador único.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="1c4a2-108">El identificador incluye el tipo del objeto (como contador, cadena, medidor o dirección), el nivel de acceso del objeto (como lectura o lectura/escritura), restricciones de tamaño e información de intervalo.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="1c4a2-109">La tabla siguiente contiene una lista parcial de las MIB que se incluyen con el sistema.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="1c4a2-110">Se instalan con el servicio SNMP en el directorio% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="1c4a2-111">Para obtener una lista completa de las MIB, consulte el kit de recursos de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="1c4a2-112">MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-112">MIB</span></span>         | <span data-ttu-id="1c4a2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c4a2-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4a2-114">DHCP. MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-114">DHCP.MIB</span></span>    | <span data-ttu-id="1c4a2-115">MIB definida por Microsoft que contiene tipos de objeto para supervisar el tráfico de red entre los hosts remotos y los servidores DHCP</span><span class="sxs-lookup"><span data-stu-id="1c4a2-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="1c4a2-116">HOSTMIB. MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="1c4a2-117">Contiene tipos de objeto para la supervisión y administración de recursos de host</span><span class="sxs-lookup"><span data-stu-id="1c4a2-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="1c4a2-118">LMMIB2. MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="1c4a2-119">Trata los servicios de estación de trabajo y servidor</span><span class="sxs-lookup"><span data-stu-id="1c4a2-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="1c4a2-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-120">MIB\_II.MIB</span></span> | <span data-ttu-id="1c4a2-121">Contiene la base de información de administración (MIB-II), que proporciona una arquitectura y un sistema sencillos y factibles para administrar Internet basados en TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="1c4a2-122">DNS. MIB</span><span class="sxs-lookup"><span data-stu-id="1c4a2-122">WINS.MIB</span></span>    | <span data-ttu-id="1c4a2-123">MIB definida por Microsoft para el servicio de nombres Internet de Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="1c4a2-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="1c4a2-124">**Windows NT:** Normalmente, puede copiar una MIB del agente de extensión SNMP que admita la MIB concreta.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="1c4a2-125">En el kit de recursos de Windows NT 4,0 hay disponibles algunas MIB adicionales.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="1c4a2-126">Los archivos DLL del agente de extensión para MIB-II, LAN Manager MIB-II y la MIB de recursos de host se instalan con el servicio SNMP.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="1c4a2-127">Los archivos DLL del agente de extensión para las demás MIB se instalan cuando se instalan sus servicios respectivos.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="1c4a2-128">En el momento de inicio del servicio, el servicio SNMP carga todos los archivos DLL del agente de extensión que se enumeran en el registro.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="1c4a2-129">Los usuarios pueden agregar otros archivos DLL del agente de extensión que implementen MIB adicionales.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="1c4a2-130">Para ello, deben agregar una entrada del registro para el nuevo archivo DLL en el servicio SNMP.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="1c4a2-131">También deben registrar la nueva MIB con la aplicación de consola de administración de SNMP.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="1c4a2-132">Para obtener más información, consulte la documentación que se incluye con la aplicación de consola de administración.</span><span class="sxs-lookup"><span data-stu-id="1c4a2-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="1c4a2-133">Para obtener más información, vea [árbol de nombres de MIB](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="1c4a2-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




