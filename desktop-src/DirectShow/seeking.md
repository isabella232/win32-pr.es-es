---
description: Invoca
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Invoca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104567136"
---
# <a name="seeking"></a><span data-ttu-id="e3f5a-103">Invoca</span><span class="sxs-lookup"><span data-stu-id="e3f5a-103">Seeking</span></span>

<span data-ttu-id="e3f5a-104">Los filtros admiten la búsqueda a través de la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="e3f5a-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="e3f5a-105">La aplicación consulta el administrador de gráficos de filtro para **IMediaSeeking** y lo usa para emitir comandos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="e3f5a-106">Filter Graph Manager distribuye cada comando de búsqueda a todos los filtros de representación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="e3f5a-107">Cada representador pasa el comando ascendente, a través de los terminales de salida de los filtros de nivel superior, hasta que alcanza un filtro que puede ejecutar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="e3f5a-108">Normalmente, un filtro de origen o un filtro de analizador, como el [divisor de AVI](avi-splitter-filter.md), lleva a cabo la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="e3f5a-109">Cuando un filtro realiza una operación de búsqueda, vacía los datos pendientes.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="e3f5a-110">El resultado es minimizar la latencia de los comandos de búsqueda, ya que los datos existentes se vacían del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="e3f5a-111">Después de un comando de búsqueda, el tiempo de secuencia se restablece en cero.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="e3f5a-112">En el diagrama siguiente se muestra la secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-112">The following diagram illustrates the sequence of events.</span></span>

![secuencia de eventos](images/seeking.png)

<span data-ttu-id="e3f5a-114">Si un filtro de analizador tiene más de un PIN de salida, normalmente designa uno de ellos para que acepte comandos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="e3f5a-115">Los demás PIN rechazan u omiten cualquier comando de búsqueda que reciban.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="e3f5a-116">De esta manera, el analizador mantiene todas sus secuencias sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="e3f5a-117">Sin embargo, todos los pin de salida deben implementar [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) y [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) para devolver las capacidades de búsqueda del filtro.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="e3f5a-118">Esto garantiza que el administrador de gráficos de filtro devuelva el valor correcto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="e3f5a-119">La interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) está en desuso para los filtros.</span><span class="sxs-lookup"><span data-stu-id="e3f5a-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="e3f5a-120">Los clientes de automatización todavía necesitan usar esta interfaz en el administrador de gráficos de filtro, porque **IMediaSeeking** no es compatible con automatización, pero el administrador de gráficos de filtros traduce todas las llamadas a **IMediaPosition** en llamadas **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="e3f5a-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3f5a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3f5a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f5a-122">Vaciar</span><span class="sxs-lookup"><span data-stu-id="e3f5a-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="e3f5a-123">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e3f5a-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



