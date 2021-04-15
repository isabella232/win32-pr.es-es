---
description: 'Más información sobre: eventos de seguimiento de la administración de memoria'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de seguimiento de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669934"
---
# <a name="memory-management-tracing-events"></a><span data-ttu-id="0fd32-103">Eventos de seguimiento de administración de memoria</span><span class="sxs-lookup"><span data-stu-id="0fd32-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="0fd32-104">En esta sección se describe información detallada sobre los detalles del evento de seguimiento de administración de memoria específico.</span><span class="sxs-lookup"><span data-stu-id="0fd32-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="0fd32-105">El seguimiento de la administración de memoria es una característica de solución de problemas que se puede habilitar en los archivos binarios comerciales para realizar un seguimiento de determinados eventos de administración de memoria con una sobrecarga mínima.</span><span class="sxs-lookup"><span data-stu-id="0fd32-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="0fd32-106">Esta característica permite mejorar las capacidades de diagnóstico de los desarrolladores y del soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="0fd32-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="0fd32-107">El seguimiento de eventos de administración de memoria admite operaciones de asignación, reasignación y liberación del montón de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="0fd32-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="0fd32-108">El seguimiento de eventos de administración de memoria utiliza el seguimiento de eventos para Windows (ETW), un servicio de seguimiento de uso general y de alta velocidad proporcionado por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0fd32-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="0fd32-109">ETW proporciona un mecanismo de seguimiento para los eventos generados por las aplicaciones de modo de usuario y los controladores de dispositivos de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0fd32-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="0fd32-110">ETW puede habilitar y deshabilitar el registro de forma dinámica, lo que facilita la realización de seguimientos detallados en entornos de producción sin necesidad de reinicios o reinicios de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0fd32-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="0fd32-111">El seguimiento de eventos de administración de memoria con ETW es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0fd32-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="0fd32-112">Para obtener información general sobre ETW, vea [mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="0fd32-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="0fd32-113">La lista siguiente proporciona información detallada para cada evento de seguimiento de administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="0fd32-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="0fd32-114">Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="0fd32-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="0fd32-115">Nombre del evento</span><span class="sxs-lookup"><span data-stu-id="0fd32-115">Event Name</span></span>                                                  | <span data-ttu-id="0fd32-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fd32-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="0fd32-117">**\_asignación de \_ eventos del montón ETW \_**</span><span class="sxs-lookup"><span data-stu-id="0fd32-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="0fd32-118">Evento de seguimiento de administración de memoria para una operación de asignación de montón.</span><span class="sxs-lookup"><span data-stu-id="0fd32-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="0fd32-119">**\_evento de montón ETW \_ \_ Free**</span><span class="sxs-lookup"><span data-stu-id="0fd32-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="0fd32-120">Evento de traza de administración de memoria para una operación libre del montón.</span><span class="sxs-lookup"><span data-stu-id="0fd32-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="0fd32-121">**\_evento de montón ETW \_ \_ REALLOC**</span><span class="sxs-lookup"><span data-stu-id="0fd32-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="0fd32-122">Evento de traza de administración de memoria para una operación de reasignación del montón.</span><span class="sxs-lookup"><span data-stu-id="0fd32-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0fd32-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0fd32-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd32-124">Mejorar la depuración y el ajuste del rendimiento con ETW</span><span class="sxs-lookup"><span data-stu-id="0fd32-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
