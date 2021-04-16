---
description: Filtro del mezclador de superposición 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro del mezclador de superposición 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686369"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="54462-103">Filtro del mezclador de superposición 2</span><span class="sxs-lookup"><span data-stu-id="54462-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="54462-104">El filtro del mezclador de superposición 2 es idéntico al filtro de [mezclador de superposición](overlay-mixer-filter.md) , excepto:</span><span class="sxs-lookup"><span data-stu-id="54462-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="54462-105">Solo admite tipos de medios con formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="54462-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="54462-106">Tiene un mérito mayor, lo que permite que se agregue automáticamente a un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="54462-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="54462-107">Se proporciona el mezclador de superposición 2 para que el administrador de gráficos de filtro lo agregue al gráfico cuando represente vídeo MPEG-2 de no DVD.</span><span class="sxs-lookup"><span data-stu-id="54462-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="54462-108">La opción de usar el mezclador de superposición o el mezclador de superposición 2 se controla mediante el componente que genera el gráfico, ya sea el administrador de gráficos de filtro, el generador de gráficos de captura o el generador de gráficos de DVD.</span><span class="sxs-lookup"><span data-stu-id="54462-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="54462-109">Desde la perspectiva de la aplicación, son el mismo filtro, con las mismas interfaces y funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="54462-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="54462-110">La tabla siguiente contiene información específica del mezclador de superposición 2.</span><span class="sxs-lookup"><span data-stu-id="54462-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="54462-111">Para el resto de datos de filtro, consulte la documentación del mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="54462-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54462-112">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="54462-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="54462-113">Tipo de formato: Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="54462-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54462-114">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="54462-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="54462-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="54462-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54462-116"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="54462-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="54462-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="54462-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="54462-118">Windows Vista o posterior: MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="54462-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="54462-119">En Windows Vista o posterior, el mérito del filtro del mezclador de superposición 2 es el mérito \_ \_ no se \_ usa, ya que los representadores de vídeo más recientes (VMR-7, VMR-9 y EVR) admiten formatos de **VIDEOINFOHEADER2** y, por tanto, no es necesario usar el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="54462-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54462-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54462-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54462-121">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="54462-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



