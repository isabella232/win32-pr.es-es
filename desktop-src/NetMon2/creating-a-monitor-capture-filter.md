---
description: La creación de un filtro de captura que funcione con Monitor de red es un proceso de cinco pasos.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Creación de un filtro de captura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677735"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="90b47-103">Creación de un filtro de captura de monitor</span><span class="sxs-lookup"><span data-stu-id="90b47-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="90b47-104">La creación de un filtro de captura que funcione con Monitor de red es un proceso de cinco pasos:</span><span class="sxs-lookup"><span data-stu-id="90b47-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="90b47-105">Establecer el valor de ETYPE o SAP Filter</span><span class="sxs-lookup"><span data-stu-id="90b47-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="90b47-106">Escribiendo filtro de ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="90b47-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="90b47-107">Escribir el filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="90b47-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="90b47-108">Recorte de un fotograma</span><span class="sxs-lookup"><span data-stu-id="90b47-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="90b47-109">Implementar el código de filtro de captura</span><span class="sxs-lookup"><span data-stu-id="90b47-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="90b47-110">Un [*filtro de captura*](c.md) es una serie de adiciones al BLOB NPP que selecciona qué fotogramas se pasan de vuelta al monitor.</span><span class="sxs-lookup"><span data-stu-id="90b47-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="90b47-111">Si un monitor no modifica el BLOB NPP, el NPP pasará al modo promiscuo y enviará todo el tráfico de red al monitor.</span><span class="sxs-lookup"><span data-stu-id="90b47-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="90b47-112">El NPP es más eficaz si puede reducir los datos entregados a un controlador, de modo que un monitor debe crear un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="90b47-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="90b47-113">Un monitor establece su filtro de captura escribiendo en el BLOB NPP en la llamada a la función [Configure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="90b47-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="90b47-114">A continuación, MCSVC llama a NPP con el BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="90b47-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="90b47-115">Consulte [filtros de captura](capture-filters.md) para obtener más detalles sobre el filtro de captura, los [proveedores de paquetes de red](network-packet-providers.md) en NPPs y [monitor de red blobs](network-monitor-blobs.md) en las funciones de BLOB.</span><span class="sxs-lookup"><span data-stu-id="90b47-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



