---
title: Plataforma de filtrado de Windows
description: La plataforma de filtrado de Windows (WFP) es un conjunto de servicios de API y de sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plataforma de filtrado de Windows
- Página de inicio de la plataforma de filtrado de Windows, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105665881"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="7e52d-105">Plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="7e52d-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="7e52d-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="7e52d-106">Purpose</span></span>

<span data-ttu-id="7e52d-107">La plataforma de filtrado de Windows (WFP) es un conjunto de servicios de API y de sistema que proporcionan una plataforma para crear aplicaciones de filtrado de red.</span><span class="sxs-lookup"><span data-stu-id="7e52d-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="7e52d-108">La API de WFP permite a los desarrolladores escribir código que interactúa con el procesamiento de paquetes que tiene lugar en varios niveles de la pila de red del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7e52d-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="7e52d-109">Se pueden filtrar y modificar datos de red antes de que lleguen a su destino.</span><span class="sxs-lookup"><span data-stu-id="7e52d-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="7e52d-110">Al proporcionar una plataforma de desarrollo más sencilla, WFP está diseñado para reemplazar las tecnologías de filtrado de paquetes anteriores, como los filtros de Interfaz de controlador de transporte (TDI), los filtros de especificación de interfaz de controlador de red (NDIS) y los proveedores de servicios superpuestos (LSP) de Winsock.</span><span class="sxs-lookup"><span data-stu-id="7e52d-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="7e52d-111">A partir de Windows Server 2008 y Windows Vista, el enlace de firewall y los controladores de enlace de filtros no están disponibles; en su lugar, las aplicaciones que usaban estos controladores deben usar WFP.</span><span class="sxs-lookup"><span data-stu-id="7e52d-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="7e52d-112">Con la API de WFP, los desarrolladores pueden implementar firewalls, sistemas de detección de intrusiones, programas antivirus, herramientas de supervisión de red y controles parentales.</span><span class="sxs-lookup"><span data-stu-id="7e52d-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="7e52d-113">WFP se integra con y proporciona compatibilidad con características de Firewall como la comunicación autenticada y la configuración de Firewall dinámica basada en el uso de las aplicaciones de sockets API (directiva basada en aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="7e52d-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="7e52d-114">WFP también proporciona una infraestructura para la administración de directivas IPsec, notificaciones de cambios, diagnósticos de red y filtrado con estado.</span><span class="sxs-lookup"><span data-stu-id="7e52d-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="7e52d-115">La plataforma de filtrado de Windows es una plataforma de desarrollo y no un firewall.</span><span class="sxs-lookup"><span data-stu-id="7e52d-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="7e52d-116">La aplicación de Firewall integrada en Windows Vista, Windows Server 2008 y los sistemas operativos posteriores Firewall de Windows con seguridad avanzada (WFAS) se implementa mediante WFP.</span><span class="sxs-lookup"><span data-stu-id="7e52d-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="7e52d-117">Por lo tanto, las aplicaciones desarrolladas con la API de WFP o la [API de wfas](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usan la lógica de arbitraje de filtrado común que está integrada en WFP.</span><span class="sxs-lookup"><span data-stu-id="7e52d-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="7e52d-118">La API de WFP se compone de una API de modo usuario y una API de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="7e52d-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="7e52d-119">En esta sección se proporciona información general de la WFP completa y se describe en detalle solo la parte del modo de usuario de la API de WFP.</span><span class="sxs-lookup"><span data-stu-id="7e52d-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="7e52d-120">Para obtener una descripción detallada de la API de WFP en modo kernel, vea la ayuda en pantalla del [Kit de controladores de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="7e52d-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7e52d-121">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="7e52d-121">Developer audience</span></span>

<span data-ttu-id="7e52d-122">La API de la plataforma de filtrado de Windows está diseñada para que la usen los programadores que usan software de desarrollo de C/C++.</span><span class="sxs-lookup"><span data-stu-id="7e52d-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="7e52d-123">Los programadores deben estar familiarizados con los conceptos de red y el diseño de sistemas que usan componentes de modo de usuario y de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="7e52d-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7e52d-124">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7e52d-124">Run-time requirements</span></span>

<span data-ttu-id="7e52d-125">La plataforma de filtrado de Windows se admite en clientes que ejecutan Windows Vista y versiones posteriores, y en servidores que ejecutan Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7e52d-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="7e52d-126">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación específico, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="7e52d-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="7e52d-127">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7e52d-127">In this section</span></span>



| <span data-ttu-id="7e52d-128">Tema</span><span class="sxs-lookup"><span data-stu-id="7e52d-128">Topic</span></span>                                                                                               | <span data-ttu-id="7e52d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e52d-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e52d-130">Novedades de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="7e52d-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="7e52d-131">Información sobre las nuevas características y API de la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="7e52d-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="7e52d-132">Acerca de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="7e52d-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="7e52d-133">Información general sobre la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="7e52d-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="7e52d-134">Uso de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="7e52d-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="7e52d-135">Código de ejemplo que usa la API de la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="7e52d-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="7e52d-136">Referencia de API de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="7e52d-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="7e52d-137">Documentación de las funciones, estructuras y constantes de la plataforma de filtrado de Windows.</span><span class="sxs-lookup"><span data-stu-id="7e52d-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="7e52d-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7e52d-138">Additional resources</span></span>

<span data-ttu-id="7e52d-139">Para formular preguntas y tener discusiones sobre el uso de la API de WFP, visite el foro de la [plataforma de filtrado de Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="7e52d-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e52d-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e52d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e52d-141">API de plataforma de filtrado de Windows de modo kernel: Guía de diseño</span><span class="sxs-lookup"><span data-stu-id="7e52d-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="7e52d-142">API de plataforma de filtrado de Windows de modo kernel-referencia</span><span class="sxs-lookup"><span data-stu-id="7e52d-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="7e52d-143">Firewall de Windows con seguridad avanzada</span><span class="sxs-lookup"><span data-stu-id="7e52d-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="7e52d-144">Clase auxiliar extensible de diagnóstico de WFP</span><span class="sxs-lookup"><span data-stu-id="7e52d-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="7e52d-145">Extensiones Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="7e52d-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

