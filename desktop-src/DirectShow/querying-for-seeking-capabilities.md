---
description: Consulta de funcionalidades de búsqueda
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consulta de funcionalidades de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906743"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="8b8b4-103">Consulta de funcionalidades de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8b8b4-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="8b8b4-104">Microsoft® DirectShow® admite la búsqueda a través de la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="8b8b4-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="8b8b4-105">El administrador de gráficos de filtro expone esta interfaz, pero la funcionalidad de búsqueda siempre se implementa mediante filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="8b8b4-106">No se puede buscar en algunos datos.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-106">Some data cannot be seeked.</span></span> <span data-ttu-id="8b8b4-107">Por ejemplo, no puede buscar una secuencia de vídeo en directo desde una cámara.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="8b8b4-108">Sin embargo, si se puede buscar en una secuencia, es posible que se admitan varios tipos de búsquedas.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="8b8b4-109">Entre ellas se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b8b4-109">These include:</span></span>

-   <span data-ttu-id="8b8b4-110">Buscar una posición arbitraria en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="8b8b4-111">Recuperar la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="8b8b4-112">Recuperar la posición actual dentro de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="8b8b4-113">Reproducir en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-113">Playing in reverse.</span></span>

<span data-ttu-id="8b8b4-114">La interfaz **IMediaSeeking** define un conjunto de marcas, [**que \_ buscan \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), que describen las posibles capacidades de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="8b8b4-115">Para recuperar las capacidades de la secuencia, llame al método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="8b8b4-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="8b8b4-116">El método devuelve una combinación bit a bit de marcas.</span><span class="sxs-lookup"><span data-stu-id="8b8b4-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="8b8b4-117">La aplicación puede probarla mediante el operador & (and bit **a** bit).</span><span class="sxs-lookup"><span data-stu-id="8b8b4-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="8b8b4-118">Por ejemplo, el código siguiente comprueba si el gráfico puede buscar una posición arbitraria:</span><span class="sxs-lookup"><span data-stu-id="8b8b4-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



