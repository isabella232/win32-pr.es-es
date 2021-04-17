---
description: Streaming de subprocesos y Filter Graph Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streaming de subprocesos y Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678151"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="af336-103">Streaming de subprocesos y Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="af336-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="af336-104">Cuando el administrador de gráficos de filtro detiene el gráfico, espera a que se cierren todos los subprocesos de streaming.</span><span class="sxs-lookup"><span data-stu-id="af336-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="af336-105">Esto tiene las implicaciones siguientes para los filtros:</span><span class="sxs-lookup"><span data-stu-id="af336-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="af336-106">Un filtro no debe llamar nunca a los métodos del administrador de gráficos de filtro desde un subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="af336-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="af336-107">Filter Graph Manager usa una sección crítica para sincronizar sus propias operaciones.</span><span class="sxs-lookup"><span data-stu-id="af336-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="af336-108">Si un subproceso de streaming intenta contener esta sección crítica, puede producirse un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="af336-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="af336-109">Por ejemplo: Supongamos que otro subproceso detiene el gráfico.</span><span class="sxs-lookup"><span data-stu-id="af336-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="af336-110">Ese subproceso toma el bloqueo del gráfico de filtro y espera a que el filtro deje de entregar los datos.</span><span class="sxs-lookup"><span data-stu-id="af336-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="af336-111">Si el filtro está esperando el bloqueo, nunca se detendrá, lo que provocará un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="af336-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="af336-112">Un filtro nunca debe **AddRef** o **QueryInterface** para filtrar el administrador de gráficos de un subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="af336-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="af336-113">Si el filtro contiene un recuento de referencias en el administrador de gráficos de filtro (a través de **AddRef** o **QueryInterface**), es posible que se convierta en el último objeto que contiene un recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="af336-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="af336-114">Cuando el filtro llama a **Release**, el administrador de gráficos de filtro se destruye a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="af336-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="af336-115">Dentro de su rutina de limpieza, el administrador de gráficos de filtro intenta detener el gráfico, lo que espera a que se cierre el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="af336-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="af336-116">Sin embargo, está esperando en el subproceso de streaming, por lo que el subproceso de streaming no puede salir.</span><span class="sxs-lookup"><span data-stu-id="af336-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="af336-117">El resultado es un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="af336-117">The result is a deadlock.</span></span>

 

 



