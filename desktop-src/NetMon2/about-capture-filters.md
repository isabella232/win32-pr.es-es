---
description: Un filtro de captura es un elemento de una aplicación NPP que indica al controlador de Monitor de red (Nmnt.sys) qué tramas de datos de red se van a conservar y qué fotogramas se deben omitir.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Acerca de los filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667128"
---
# <a name="about-capture-filters"></a><span data-ttu-id="03542-103">Acerca de los filtros de captura</span><span class="sxs-lookup"><span data-stu-id="03542-103">About Capture Filters</span></span>

<span data-ttu-id="03542-104">Un filtro de captura es un elemento de una aplicación NPP que indica al controlador de Monitor de red (Nmnt.sys) qué tramas de datos de red se van a conservar y qué fotogramas se deben omitir.</span><span class="sxs-lookup"><span data-stu-id="03542-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="03542-105">La ventaja de configurar un filtro de captura es mayor eficiencia.</span><span class="sxs-lookup"><span data-stu-id="03542-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="03542-106">No tiene que examinar los fotogramas capturados; el controlador de Monitor de red los examina.</span><span class="sxs-lookup"><span data-stu-id="03542-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="03542-107">Este enfoque elimina la copia de fotogramas, lo que proporciona una ventaja de uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="03542-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="03542-108">Estructura del filtro de captura</span><span class="sxs-lookup"><span data-stu-id="03542-108">Capture Filter Structure</span></span>

<span data-ttu-id="03542-109">Los filtros de captura se componen de tres elementos:</span><span class="sxs-lookup"><span data-stu-id="03542-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="03542-110">Configuración de ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="03542-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="03542-111">Dirección</span><span class="sxs-lookup"><span data-stu-id="03542-111">Address</span></span>
-   <span data-ttu-id="03542-112">Coincidencia de patrones</span><span class="sxs-lookup"><span data-stu-id="03542-112">Pattern match</span></span>

<span data-ttu-id="03542-113">Juntos, estos elementos evalúan lógicamente los fotogramas que se van a incluir o excluir durante la operación de una aplicación NPP.</span><span class="sxs-lookup"><span data-stu-id="03542-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="03542-114">El filtro de captura proporciona coincidencias complejas y exclusiones de elementos Frame a la aplicación NPP.</span><span class="sxs-lookup"><span data-stu-id="03542-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="03542-115">Monitor de red implementa el filtro de captura a través de una estructura de datos, [**CAPTUREFILTER**](the-capturefilter-structure.md), pasada a NPP y, a continuación, se pasa al controlador de monitor de red cuando se inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="03542-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="03542-116">Para obtener más información sobre las operaciones NPP y la funcionalidad BLOB, consulte [proveedores de paquetes de red](network-packet-providers.md) y [blobs monitor de red](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="03542-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



