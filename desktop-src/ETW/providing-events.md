---
description: Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Proporcionar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984478"
---
# <a name="providing-events"></a><span data-ttu-id="eaf6c-103">Proporcionar eventos</span><span class="sxs-lookup"><span data-stu-id="eaf6c-103">Providing Events</span></span>

<span data-ttu-id="eaf6c-104">Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="eaf6c-105">Después de que un proveedor se registra a sí mismo, un controlador puede habilitar o deshabilitar el seguimiento de eventos en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="eaf6c-106">El proveedor define su interpretación de que está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="eaf6c-107">Normalmente, un proveedor habilitado genera eventos y un proveedor deshabilitado no lo hace.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="eaf6c-108">Esto le permite agregar seguimiento de eventos a la aplicación sin necesidad de que genere eventos en todo momento.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="eaf6c-109">Esta sección le muestra cómo:</span><span class="sxs-lookup"><span data-stu-id="eaf6c-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="eaf6c-110">Escritura de eventos</span><span class="sxs-lookup"><span data-stu-id="eaf6c-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="eaf6c-111">Escribir eventos relacionados</span><span class="sxs-lookup"><span data-stu-id="eaf6c-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="eaf6c-112">Publicar el esquema de eventos para compartirlo con los consumidores</span><span class="sxs-lookup"><span data-stu-id="eaf6c-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="eaf6c-113">Para obtener información sobre cómo controlar las sesiones de seguimiento de eventos, vea [controlar las sesiones de seguimiento de eventos](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="eaf6c-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="eaf6c-114">Para obtener información sobre cómo consumir eventos de un proveedor de seguimiento de eventos, vea [consumir eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="eaf6c-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



