---
description: El gráfico de filtro y sus componentes
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: El gráfico de filtro y sus componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688208"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="fb63d-103">El gráfico de filtro y sus componentes</span><span class="sxs-lookup"><span data-stu-id="fb63d-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="fb63d-104">En este artículo se describen los componentes principales de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb63d-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="fb63d-105">Está pensada como una introducción para los desarrolladores de aplicaciones y para los desarrolladores que escriben filtros de DirectShow personalizados.</span><span class="sxs-lookup"><span data-stu-id="fb63d-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="fb63d-106">Normalmente, los desarrolladores de aplicaciones pueden omitir muchos de los detalles de bajo nivel de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb63d-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="fb63d-107">Sin embargo, sigue siendo una buena idea leer esta sección, para tener un conocimiento general de la arquitectura de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb63d-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="fb63d-108">Este artículo contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="fb63d-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="fb63d-109">Acerca de los filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb63d-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="fb63d-110">Acerca del administrador de gráficos de filtros</span><span class="sxs-lookup"><span data-stu-id="fb63d-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="fb63d-111">Acerca de los tipos de medios</span><span class="sxs-lookup"><span data-stu-id="fb63d-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="fb63d-112">Acerca de los ejemplos y asignadores de medios</span><span class="sxs-lookup"><span data-stu-id="fb63d-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="fb63d-113">Cómo participan los dispositivos de hardware en el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="fb63d-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



