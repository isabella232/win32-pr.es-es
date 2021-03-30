---
description: Detalles de eventos de seguimiento de Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventos de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154239"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="00f26-103">Eventos de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-103">Winsock Tracing Events</span></span>

<span data-ttu-id="00f26-104">En esta sección se describe la información detallada sobre los detalles específicos de eventos de seguimiento de Winsock.</span><span class="sxs-lookup"><span data-stu-id="00f26-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="00f26-105">El seguimiento de Winsock es una característica de solución de problemas que se puede habilitar en los archivos binarios de venta directa para realizar un seguimiento de determinados eventos de Windows socket con una sobrecarga mínima.</span><span class="sxs-lookup"><span data-stu-id="00f26-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="00f26-106">Esta característica permite mejorar las capacidades de diagnóstico de los desarrolladores y del soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="00f26-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="00f26-107">El seguimiento de eventos de red Winsock admite operaciones de socket de seguimiento para aplicaciones IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="00f26-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="00f26-108">El seguimiento de cambios del catálogo Winsock admite los cambios de seguimiento realizados en el catálogo Winsock por proveedores de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="00f26-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="00f26-109">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="00f26-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="00f26-110">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="00f26-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="00f26-111">El seguimiento de Winsock usa el seguimiento de eventos para Windows (ETW), un servicio de seguimiento de alta velocidad y de uso general que proporciona el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00f26-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="00f26-112">ETW proporciona un mecanismo de seguimiento para los eventos generados por las aplicaciones de modo de usuario y los controladores de dispositivos de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="00f26-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="00f26-113">ETW puede habilitar y deshabilitar el registro de forma dinámica, lo que facilita la realización de seguimientos detallados en entornos de producción sin necesidad de reinicios o reinicios de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="00f26-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="00f26-114">Se ha agregado compatibilidad con el seguimiento de Winsock mediante ETW en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="00f26-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="00f26-115">Para obtener información general sobre ETW, vea [mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="00f26-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="00f26-116">La lista siguiente proporciona información detallada para cada evento de seguimiento de Winsock.</span><span class="sxs-lookup"><span data-stu-id="00f26-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="00f26-117">Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="00f26-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="00f26-118">Nombre del evento</span><span class="sxs-lookup"><span data-stu-id="00f26-118">Event Name</span></span>                                                            | <span data-ttu-id="00f26-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="00f26-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00f26-120">**\_creación de eventos de AFD \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="00f26-121">Evento de seguimiento de red Winsock para una operación de creación de Sockets.</span><span class="sxs-lookup"><span data-stu-id="00f26-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="00f26-122">**\_cierre de evento de AFD \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="00f26-123">Evento de seguimiento de red Winsock para la operación de cierre del socket.</span><span class="sxs-lookup"><span data-stu-id="00f26-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="00f26-124">**\_Instalación de WS2HELP de \_ LSP de Winsock \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="00f26-125">Evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="00f26-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="00f26-126">**\_ \_ Quitar LSP de WS2HELP de Winsock \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="00f26-127">Evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="00f26-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="00f26-128">**Deshabilitación de LSP de WINSOCK \_ WS2HELP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="00f26-129">Evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="00f26-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="00f26-130">**\_Restablecimiento de \_ LSP de WS2HELP de Winsock \_**</span><span class="sxs-lookup"><span data-stu-id="00f26-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="00f26-131">Evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="00f26-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="00f26-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00f26-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f26-133">Mejorar la depuración y el ajuste del rendimiento con ETW</span><span class="sxs-lookup"><span data-stu-id="00f26-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="00f26-134">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="00f26-135">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="00f26-136">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="00f26-137">Detalles de seguimiento de eventos de red Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="00f26-138">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="00f26-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
