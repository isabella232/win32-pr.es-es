---
description: Cambios en el formato dinámico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Cambios en el formato dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677126"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="e5211-103">Cambios en el formato dinámico</span><span class="sxs-lookup"><span data-stu-id="e5211-103">Dynamic Format Changes</span></span>

<span data-ttu-id="e5211-104">Cuando dos filtros se conectan, coinciden con un tipo de medio, que describe el formato de los datos que proporcionará el filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e5211-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="e5211-105">En la mayoría de los casos, el tipo de medio es fijo para la duración de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e5211-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="e5211-106">Sin embargo, DirectShow ofrece compatibilidad limitada para los filtros con el fin de cambiar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e5211-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="e5211-107">Cuando un filtro cambia los tipos de medios, se denomina *cambio de formato dinámico*.</span><span class="sxs-lookup"><span data-stu-id="e5211-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="e5211-108">Si está escribiendo un filtro de DirectShow, debe tener en cuenta los mecanismos para los cambios de formato dinámico.</span><span class="sxs-lookup"><span data-stu-id="e5211-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="e5211-109">Incluso si el filtro no admite estos cambios, debe responder correctamente si otro filtro solicita un nuevo formato.</span><span class="sxs-lookup"><span data-stu-id="e5211-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="e5211-110">DirectShow define varios mecanismos distintos para los cambios de formato dinámico, según el estado del gráfico de filtro y el tipo de cambio necesario.</span><span class="sxs-lookup"><span data-stu-id="e5211-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="e5211-111">Si se detiene el gráfico, los pin pueden volver a conectarse y negociar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e5211-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="e5211-112">Para obtener más información, consulte [reconexión de PIN](reconnecting-pins.md).</span><span class="sxs-lookup"><span data-stu-id="e5211-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="e5211-113">Algunos filtros pueden volver a conectar los pin incluso mientras el gráfico esté activo (en ejecución o en pausa).</span><span class="sxs-lookup"><span data-stu-id="e5211-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="e5211-114">Para obtener más información sobre este mecanismo, vea [reconexión dinámica](dynamic-reconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e5211-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="e5211-115">De lo contrario, si el gráfico está activo, pero los filtros en cuestión no admiten las reconexiones dinámicas de PIN, existen tres mecanismos posibles para cambiar el formato:</span><span class="sxs-lookup"><span data-stu-id="e5211-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="e5211-116">[QueryAccept (Downstream)](queryaccept--downstream.md) se usa cuando un terminal de salida propone un cambio de formato a su elemento inferior del mismo nivel, pero solo si el nuevo formato no requiere un búfer mayor.</span><span class="sxs-lookup"><span data-stu-id="e5211-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="e5211-117">[QueryAccept (upstream)](queryaccept--upstream.md) se usa cuando un PIN de entrada propone un cambio de formato a su par de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e5211-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="e5211-118">El nuevo formato puede tener el mismo tamaño o puede ser mayor.</span><span class="sxs-lookup"><span data-stu-id="e5211-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="e5211-119">[ReceiveConnection](receiveconnection.md) se usa cuando un terminal de salida propone un cambio de formato a su par inferior y el nuevo formato requiere un búfer mayor.</span><span class="sxs-lookup"><span data-stu-id="e5211-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5211-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5211-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5211-121">Control de los cambios de formato del representador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5211-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



