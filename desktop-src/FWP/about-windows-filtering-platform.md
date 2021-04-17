---
title: Acerca de la plataforma de filtrado de Windows
description: La plataforma de filtrado de Windows (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado del tráfico de red de Windows XP y Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665824"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="28a30-103">Acerca de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="28a30-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="28a30-104">La plataforma de filtrado de Windows (WFP) es una plataforma de procesamiento de tráfico de red diseñada para reemplazar las interfaces de filtrado del tráfico de red de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="28a30-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="28a30-105">WFP se compone de un conjunto de enlaces en la pila de red y un motor de filtrado que coordina las interacciones de la pila de red.</span><span class="sxs-lookup"><span data-stu-id="28a30-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="28a30-106">Los componentes de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="28a30-107">Motor de filtro</span><span class="sxs-lookup"><span data-stu-id="28a30-107">Filter Engine</span></span>

<span data-ttu-id="28a30-108">La infraestructura de filtrado de varios niveles principal, hospedada en modo de kernel y en modo de usuario, que reemplaza los módulos de filtrado múltiples en el subsistema de redes de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="28a30-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="28a30-109">Filtra el tráfico de red en cualquier capa del sistema sobre cualquier campo de datos que pueda proporcionar una corrección de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="28a30-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="28a30-110">Implementa los filtros de "llamada" mediante la invocación de llamadas durante la clasificación.</span><span class="sxs-lookup"><span data-stu-id="28a30-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="28a30-111">Devuelve las acciones "permitir" o "bloquear" a la corrección de compatibilidad que lo invocó para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="28a30-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="28a30-112">Proporciona arbitraje entre distintos orígenes de directiva.</span><span class="sxs-lookup"><span data-stu-id="28a30-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="28a30-113">Por ejemplo, determina la prioridad cuando una aplicación está configurada para proteger el tráfico de red relacionado con ella, pero el Firewall local está configurado para impedir el tráfico protegido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="28a30-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="28a30-114">Motor de filtrado de base (BFE)</span><span class="sxs-lookup"><span data-stu-id="28a30-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="28a30-115">Un servicio que controla el funcionamiento de la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="28a30-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="28a30-116">Realiza las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="28a30-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="28a30-117">Acepta filtros y otras opciones de configuración para la plataforma.</span><span class="sxs-lookup"><span data-stu-id="28a30-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="28a30-118">Informa del estado actual del sistema, incluidas las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="28a30-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="28a30-119">Aplica el modelo de seguridad para aceptar la configuración en la plataforma.</span><span class="sxs-lookup"><span data-stu-id="28a30-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="28a30-120">Por ejemplo, un administrador local puede Agregar filtros, pero otros usuarios solo pueden verlos.</span><span class="sxs-lookup"><span data-stu-id="28a30-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="28a30-121">Los valores de configuración de las conexiones a otros módulos del sistema.</span><span class="sxs-lookup"><span data-stu-id="28a30-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="28a30-122">Por ejemplo, las directivas de negociación de IPsec van a los módulos de creación de claves IKE/AuthIP, los filtros van al motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="28a30-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="28a30-123">Correcciones</span><span class="sxs-lookup"><span data-stu-id="28a30-123">Shims</span></span>

<span data-ttu-id="28a30-124">Componentes de modo kernel que residen entre la pila de red y el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="28a30-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="28a30-125">Las correcciones de compatibilidad (shim) realizan la decisión de filtrado mediante la clasificación en el motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="28a30-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="28a30-126">A continuación se muestra una lista de las correcciones de compatibilidad (shim) disponibles.</span><span class="sxs-lookup"><span data-stu-id="28a30-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="28a30-127">Corrección de compatibilidad de cumplimiento de nivel de aplicación (ALE).</span><span class="sxs-lookup"><span data-stu-id="28a30-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="28a30-128">Corrección de compatibilidad del módulo de capa de transporte.</span><span class="sxs-lookup"><span data-stu-id="28a30-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="28a30-129">Correcciones de compatibilidad del módulo de capa de red.</span><span class="sxs-lookup"><span data-stu-id="28a30-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="28a30-130">Corrección de errores del Protocolo de mensajes de control de Internet (ICMP).</span><span class="sxs-lookup"><span data-stu-id="28a30-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="28a30-131">Descartar correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="28a30-131">Discard shim.</span></span>
-   <span data-ttu-id="28a30-132">Corrección de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="28a30-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="28a30-133">Llamadas</span><span class="sxs-lookup"><span data-stu-id="28a30-133">Callouts</span></span>

<span data-ttu-id="28a30-134">Conjunto de funciones expuestas por un controlador y utilizadas para el filtrado especializado.</span><span class="sxs-lookup"><span data-stu-id="28a30-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="28a30-135">Además de las acciones básicas de "permitir" y "bloquear", las llamadas pueden modificar y proteger el tráfico de red entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="28a30-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="28a30-136">Consulte el tema controladores de llamadas de la [plataforma de filtrado de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) en la documentación del kit de controladores de Windows (WDK) para obtener más información sobre las llamadas.</span><span class="sxs-lookup"><span data-stu-id="28a30-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="28a30-137">WFP proporciona llamadas integradas que realizan las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="28a30-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="28a30-138">Realizar el procesamiento de IPsec.</span><span class="sxs-lookup"><span data-stu-id="28a30-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="28a30-139">Ajuste el comportamiento del filtrado con estado.</span><span class="sxs-lookup"><span data-stu-id="28a30-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="28a30-140">Realice el filtrado en modo invisible (eliminación silenciosa de los paquetes que no se solicitaron).</span><span class="sxs-lookup"><span data-stu-id="28a30-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="28a30-141">Controlar la descarga de TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="28a30-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="28a30-142">Interactúe con el servicio Teredo.</span><span class="sxs-lookup"><span data-stu-id="28a30-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="28a30-143">El motor de filtro permite que las llamadas de terceros se registren en cada una de sus capas de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="28a30-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="28a30-144">Interfaz de programación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="28a30-144">Application Programming Interface</span></span>

<span data-ttu-id="28a30-145">Conjunto de tipos de datos y funciones disponibles para que los desarrolladores puedan crear y administrar aplicaciones de filtrado de red.</span><span class="sxs-lookup"><span data-stu-id="28a30-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="28a30-146">Estos tipos de datos y funciones se agrupan en varios [conjuntos de API](api-sets.md).</span><span class="sxs-lookup"><span data-stu-id="28a30-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="28a30-147">Características de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-147">WFP Features</span></span>

-   <span data-ttu-id="28a30-148">Proporciona una infraestructura de filtrado de paquetes en la que los fabricantes de software independientes (ISV) pueden complementar módulos de filtrado especializados.</span><span class="sxs-lookup"><span data-stu-id="28a30-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="28a30-149">Funciona con IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="28a30-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="28a30-150">Permite el filtrado, modificación y reinyección de datos.</span><span class="sxs-lookup"><span data-stu-id="28a30-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="28a30-151">Realiza el procesamiento de paquetes y de secuencias.</span><span class="sxs-lookup"><span data-stu-id="28a30-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="28a30-152">Permite habilitar el filtrado de paquetes por aplicación, por usuario y por conexión, además de por interfaz de red o por puerto.</span><span class="sxs-lookup"><span data-stu-id="28a30-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="28a30-153">Proporciona seguridad en tiempo de arranque hasta que se puede iniciar el motor de filtrado de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="28a30-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="28a30-154">Habilita el filtrado de conexiones con estado.</span><span class="sxs-lookup"><span data-stu-id="28a30-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="28a30-155">Controla los datos anteriores y posteriores cifrados con IPsec.</span><span class="sxs-lookup"><span data-stu-id="28a30-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="28a30-156">Permite la integración de directivas de filtrado de firewall y IPsec.</span><span class="sxs-lookup"><span data-stu-id="28a30-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="28a30-157">Proporciona una infraestructura de administración de directivas para determinar cuándo se deben activar filtros específicos.</span><span class="sxs-lookup"><span data-stu-id="28a30-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="28a30-158">Esto incluye la mediación de requisitos conflictivos de varios filtros proporcionados por diferentes proveedores.</span><span class="sxs-lookup"><span data-stu-id="28a30-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="28a30-159">Controla la mayoría del reensamblado de paquetes y el seguimiento del estado.</span><span class="sxs-lookup"><span data-stu-id="28a30-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="28a30-160">Incluye un sistema de notificaciones de usuario genérico que informa a los suscriptores de los cambios en el sistema de filtrado.</span><span class="sxs-lookup"><span data-stu-id="28a30-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="28a30-161">Implementa las funciones de enumeración que informan sobre el estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="28a30-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="28a30-162">Utiliza eventos net para registrar errores de IPsec y caídas de paquetes.</span><span class="sxs-lookup"><span data-stu-id="28a30-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="28a30-163">Admite una clase auxiliar del marco de diagnóstico de redes [(NDF)](/windows/desktop/NDF/extensible-helper-classes).</span><span class="sxs-lookup"><span data-stu-id="28a30-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="28a30-164">Admite las [extensiones de sockets seguros](/windows/desktop/WinSock/winsock-secure-socket-extensions) para la API de Winsock, que permiten a las aplicaciones de red proteger su tráfico mediante la configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="28a30-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="28a30-165">En las capas de aplicación de nivel de aplicación (ALE), afecta de manera mínima al rendimiento de la red al procesar solo el primer paquete de una conexión.</span><span class="sxs-lookup"><span data-stu-id="28a30-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="28a30-166">Integra la descarga de hardware, donde los módulos de llamada en modo kernel pueden usar hardware para realizar una inspección de paquetes específica.</span><span class="sxs-lookup"><span data-stu-id="28a30-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28a30-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28a30-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a30-168">Arquitectura de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="28a30-169">Operación de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="28a30-170">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="28a30-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="28a30-171">Configuración de IPsec</span><span class="sxs-lookup"><span data-stu-id="28a30-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="28a30-172">Configuración de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="28a30-173">Supervisión de WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="28a30-174">API DE WFP</span><span class="sxs-lookup"><span data-stu-id="28a30-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

