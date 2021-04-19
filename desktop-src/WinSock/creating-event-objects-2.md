---
description: El \_32.dll Ws2 proporciona funciones para la creación de objetos de eventos en aplicaciones y proveedores de servicios, aunque en la mayoría de los objetos de evento se crearán las aplicaciones.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Crear objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696386"
---
# <a name="creating-event-objects"></a><span data-ttu-id="ecd01-103">Crear objetos de evento</span><span class="sxs-lookup"><span data-stu-id="ecd01-103">Creating Event Objects</span></span>

<span data-ttu-id="ecd01-104">El \_32.dll Ws2 proporciona funciones para la creación de objetos de eventos en aplicaciones y proveedores de servicios, aunque en la mayoría de los objetos de evento se crearán las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ecd01-104">The Ws2\_32.dll provides facilities for event object creation to both applications and service providers, although in most instances event objects will be created by applications.</span></span> <span data-ttu-id="ecd01-105">Los servicios de objetos de eventos se ponen a disposición de los proveedores de servicios de Windows Sockets a través de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplemente como un mecanismo de comodidad para cualquier procesamiento interno que pueda beneficiarse de la misma.</span><span class="sxs-lookup"><span data-stu-id="ecd01-105">Event object services are made available to Windows Sockets service providers through [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simply as a convenience mechanism for any internal processing that may benefit from same.</span></span> <span data-ttu-id="ecd01-106">Tenga en cuenta que el identificador del objeto de evento solo es válido en el contexto del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="ecd01-106">Note that the event object handle is only valid in the context of the calling process.</span></span> <span data-ttu-id="ecd01-107">En entornos Windows, la realización de objetos de eventos se realiza a través de los servicios de eventos nativos proporcionados por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ecd01-107">In Windows environments the realization of event objects is through the native event services provided by the operating system.</span></span>

 

 



