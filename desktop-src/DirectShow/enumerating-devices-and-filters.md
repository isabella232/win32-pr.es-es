---
description: Enumerar dispositivos y filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerar dispositivos y filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906758"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="5b095-103">Enumerar dispositivos y filtros</span><span class="sxs-lookup"><span data-stu-id="5b095-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="5b095-104">A veces, una aplicación necesita buscar un filtro determinado en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b095-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="5b095-105">Por ejemplo, una aplicación de captura de vídeo puede mostrar una lista de dispositivos de captura disponibles.</span><span class="sxs-lookup"><span data-stu-id="5b095-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="5b095-106">Dado que DirectShow usa una arquitectura basada en componentes, no puede saber en tiempo de diseño qué filtros están instalados en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b095-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="5b095-107">Esto es especialmente cierto para los filtros que representan dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="5b095-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="5b095-108">DirectShow proporciona dos componentes que buscan los filtros registrados:</span><span class="sxs-lookup"><span data-stu-id="5b095-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="5b095-109">El [enumerador de dispositivos del sistema](system-device-enumerator.md) busca filtros por su categoría.</span><span class="sxs-lookup"><span data-stu-id="5b095-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="5b095-110">El [asignador de filtros](filter-mapper.md) busca filtros según los criterios de búsqueda proporcionados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b095-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="5b095-111">Los enumeradores descritos en esta sección siguen el formato estándar que utilizan las interfaces de enumeración COM.</span><span class="sxs-lookup"><span data-stu-id="5b095-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="5b095-112">Para obtener más información, vea el tema "IEnumXXXX" en el kit de desarrollo de software (SDK) de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5b095-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="5b095-113">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="5b095-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5b095-114">Usar el enumerador de dispositivos del sistema</span><span class="sxs-lookup"><span data-stu-id="5b095-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="5b095-115">Usar el asignador de filtros</span><span class="sxs-lookup"><span data-stu-id="5b095-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="5b095-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b095-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b095-117">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b095-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



