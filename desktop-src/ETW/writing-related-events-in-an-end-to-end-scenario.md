---
description: ETW proporciona una manera de agrupar eventos relacionados de más de un componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Escritura de eventos relacionados en un escenario de un extremo a otro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984543"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="025bf-103">Escritura de eventos relacionados en un escenario de un extremo a otro</span><span class="sxs-lookup"><span data-stu-id="025bf-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="025bf-104">ETW proporciona una manera de agrupar eventos relacionados de más de un componente.</span><span class="sxs-lookup"><span data-stu-id="025bf-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="025bf-105">Por ejemplo, si hay varios componentes (en el mismo equipo o en equipos diferentes) implicados en el procesamiento de los mismos datos, y cada componente registra eventos para su parte de la actividad, puede agrupar todos los eventos relacionados.</span><span class="sxs-lookup"><span data-stu-id="025bf-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="025bf-106">Esto permitirá que un consumidor consuma todos los eventos, desde el principio del proceso hasta el final del proceso.</span><span class="sxs-lookup"><span data-stu-id="025bf-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="025bf-107">Para escribir eventos relacionados en un proveedor basado en [manifiestos](about-event-tracing.md) , vea [escribir eventos relacionados en un proveedor basado en manifiestos](writing-related-events-in-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="025bf-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="025bf-108">Para escribir eventos relacionados en un proveedor [clásico](about-event-tracing.md) , consulte [escribir eventos relacionados en un proveedor clásico](tracing-event-instances.md).</span><span class="sxs-lookup"><span data-stu-id="025bf-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



