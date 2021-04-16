---
description: Origen de archivo AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origen de archivo AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686409"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="d665c-103">Origen de archivo AVI/WAV</span><span class="sxs-lookup"><span data-stu-id="d665c-103">AVI/WAV File Source</span></span>

<span data-ttu-id="d665c-104">(En desuso.</span><span class="sxs-lookup"><span data-stu-id="d665c-104">(Deprecated.</span></span> <span data-ttu-id="d665c-105">En el caso de los archivos AVI y WAV, use el [origen de archivo (Async)](file-source--async--filter.md) y el [divisor de AVI](avi-splitter-filter.md) o el [analizador de onda](wave-parser-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="d665c-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="d665c-106">El filtro de origen de archivo AVI/WAV Lee los archivos de código fuente AVI y WAV y genera los pin de salida adecuados para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="d665c-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="d665c-107">En el caso de los archivos WAV, el filtro crea un PIN de salida de audio, que genera una secuencia de audio que se puede conectar a un filtro de representación de audio o a un filtro de transformación de audio intermedio.</span><span class="sxs-lookup"><span data-stu-id="d665c-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="d665c-108">En el caso de los archivos AVI, el filtro crea un PIN de salida de vídeo, que genera una secuencia AVI comprimida para el filtro de códec AVI y un PIN de salida de audio, que genera una secuencia de audio adecuada para un filtro de representación de audio o un filtro de transformación de audio intermedio.</span><span class="sxs-lookup"><span data-stu-id="d665c-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d665c-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d665c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d665c-110">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d665c-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



