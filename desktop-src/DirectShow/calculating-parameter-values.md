---
description: Calcular valores de parámetros
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcular valores de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659275"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="cf987-103">Calcular valores de parámetros</span><span class="sxs-lookup"><span data-stu-id="cf987-103">Calculating Parameter Values</span></span>

<span data-ttu-id="cf987-104">Potencialmente, un búfer de entrada podría ser muy grande.</span><span class="sxs-lookup"><span data-stu-id="cf987-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="cf987-105">Idealmente, cuando DMO procesa el búfer, los parámetros seguirán exactamente sus curvas en todo el lote de datos.</span><span class="sxs-lookup"><span data-stu-id="cf987-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="cf987-106">Sin embargo, un DMO tiene algunos libertad en cómo calcula esos valores.</span><span class="sxs-lookup"><span data-stu-id="cf987-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="cf987-107">El enfoque más preciso consiste en calcular el valor exacto de cada unidad atómica de datos; por ejemplo, cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="cf987-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="cf987-108">Este enfoque es el más costoso.</span><span class="sxs-lookup"><span data-stu-id="cf987-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="cf987-109">Otro enfoque consiste en segmentar los datos en unidades más pequeñas de un tamaño fijo, como ejemplos de 100.</span><span class="sxs-lookup"><span data-stu-id="cf987-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="cf987-110">Este enfoque crea un efecto de "paso de escalera".</span><span class="sxs-lookup"><span data-stu-id="cf987-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="cf987-111">En algunos parámetros, podría ser aceptable.</span><span class="sxs-lookup"><span data-stu-id="cf987-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="cf987-112">En efectos de audio, podría crear artefactos auditivos.</span><span class="sxs-lookup"><span data-stu-id="cf987-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="cf987-113">Un compromiso es usar la técnica anterior, pero dentro de cada lote, realice una interpolación lineal del valor del parámetro para cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cf987-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="cf987-114">Estos problemas son especialmente importantes para el procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="cf987-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="cf987-115">Un segundo de audio puede contener 48.000 muestras de audio por canal, que es una gran cantidad de cálculos para realizar, pero la lengüeta es sensible a los artefactos como el alias.</span><span class="sxs-lookup"><span data-stu-id="cf987-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf987-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf987-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf987-117">Parámetros multimedia</span><span class="sxs-lookup"><span data-stu-id="cf987-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



