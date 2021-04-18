---
description: En la infraestructura de WMI, el servicio WMI (WinMgmt) es el componente del sistema operativo que actúa como el mediador entre las aplicaciones de administración y los proveedores de datos de WMI. El repositorio WMI es un área de almacenamiento para los datos estáticos relacionados con WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infraestructura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706151"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="db640-104">Infraestructura WMI</span><span class="sxs-lookup"><span data-stu-id="db640-104">WMI Infrastructure</span></span>

<span data-ttu-id="db640-105">En la infraestructura de WMI, el servicio WMI (WinMgmt) es el componente del sistema operativo que actúa como el mediador entre las aplicaciones de administración y los [*proveedores*](gloss-p.md)de datos de WMI.</span><span class="sxs-lookup"><span data-stu-id="db640-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="db640-106">El [*repositorio WMI*](gloss-w.md) es un área de almacenamiento para los datos estáticos relacionados con WMI.</span><span class="sxs-lookup"><span data-stu-id="db640-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="db640-107">El servicio WMI se implementa como un proceso de servicio dentro de un proceso de host de servicio compartido (SVCHOST).</span><span class="sxs-lookup"><span data-stu-id="db640-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="db640-108">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="db640-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="db640-109">El servicio WMI se inicia cuando la primera aplicación o script de administración realiza una llamada para conectarse a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="db640-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="db640-110">Dependiendo de la configuración, el servicio WMI puede cerrarse o entrar en un perfil de memoria insuficiente cuando una aplicación de administración no lo llama.</span><span class="sxs-lookup"><span data-stu-id="db640-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="db640-111">El servicio WMI interactúa con las aplicaciones de administración a través de la interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="db640-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="db640-112">Cuando una aplicación realiza una solicitud a través de la interfaz, WMI determina si la solicitud es para datos estáticos o dinámicos.</span><span class="sxs-lookup"><span data-stu-id="db640-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="db640-113">Si la solicitud implica datos estáticos, como el nombre de un objeto administrado, WMI recupera los datos del repositorio.</span><span class="sxs-lookup"><span data-stu-id="db640-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="db640-114">Si la solicitud implica datos dinámicos, como la cantidad de memoria que está usando un objeto administrado actualmente, WMI pasa la solicitud a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="db640-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="db640-115">Los proveedores registran su ubicación con el servicio WMI, que permite a WMI enrutar las solicitudes de datos.</span><span class="sxs-lookup"><span data-stu-id="db640-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="db640-116">Un proveedor también registra la compatibilidad con operaciones particulares, como la recuperación de datos, la modificación, la eliminación, la enumeración o el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="db640-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="db640-117">El servicio WMI utiliza la información de registro del proveedor para hacer coincidir las solicitudes de la aplicación con el proveedor adecuado.</span><span class="sxs-lookup"><span data-stu-id="db640-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="db640-118">WMI también usa la información de registro para cargar y descargar los proveedores, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="db640-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="db640-119">Cuando un proveedor finaliza el procesamiento de una solicitud, el proveedor devuelve el resultado al servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="db640-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="db640-120">Después, WMI reenvía el resultado a la aplicación a través de la interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="db640-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="db640-121">Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="db640-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="db640-122">WMI utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) para registrar la actividad del servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="db640-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="db640-123">Dado que la infraestructura controla todo el tráfico entre los proveedores y las aplicaciones de administración, la infraestructura proporciona las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="db640-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="db640-124">Compatibilidad con la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="db640-124">Event Notification Support</span></span>

    <span data-ttu-id="db640-125">Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="db640-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="db640-126">Compatibilidad con el lenguaje de consulta</span><span class="sxs-lookup"><span data-stu-id="db640-126">Query Language Support</span></span>

    <span data-ttu-id="db640-127">Para obtener más información, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="db640-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="db640-128">Compatibilidad con la seguridad</span><span class="sxs-lookup"><span data-stu-id="db640-128">Security Support</span></span>

    <span data-ttu-id="db640-129">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="db640-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="db640-130">Scripting de acceso a los datos del contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="db640-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="db640-131">Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="db640-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db640-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db640-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db640-133">Arquitectura de WMI</span><span class="sxs-lookup"><span data-stu-id="db640-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
