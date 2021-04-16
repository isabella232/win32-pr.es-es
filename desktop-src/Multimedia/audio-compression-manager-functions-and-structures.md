---
title: Funciones y estructuras del administrador de compresión de audio
description: Funciones y estructuras del administrador de compresión de audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimedia, funciones ACM
- audio, funciones ACM
- Administrador de compresión de audio (ACM), funciones
- ACM (Administrador de compresión de audio), funciones
- audio multimedia, estructuras ACM
- estructuras de audio y ACM
- Administrador de compresión de audio (ACM), estructuras
- ACM (Administrador de compresión de audio), estructuras
- Estructuras ACM
- Funciones ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651348"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="cfc23-113">Funciones y estructuras del administrador de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="cfc23-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="cfc23-114">Las funciones ACM se dividen en varias categorías.</span><span class="sxs-lookup"><span data-stu-id="cfc23-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="cfc23-115">Las convenciones de nomenclatura para las funciones facilitan la identificación de estas categorías.</span><span class="sxs-lookup"><span data-stu-id="cfc23-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="cfc23-116">Los nombres de función (con dos excepciones) tienen el formato *acmGroupFunction*, donde *Group* designa la categoría ACM (como "driver", "format", "FormatTag", "Filter", "FilterTag" o "Stream") y la *función* describe la acción que realiza la función.</span><span class="sxs-lookup"><span data-stu-id="cfc23-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="cfc23-117">Las funciones de los grupos filtro y formato son muy similares.</span><span class="sxs-lookup"><span data-stu-id="cfc23-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="cfc23-118">Casi todas las funciones que actúan en filtros tienen una función paralela que actúa en formatos.</span><span class="sxs-lookup"><span data-stu-id="cfc23-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="cfc23-119">En el grupo formato, algunas funciones usan etiquetas de formato de audio de forma de onda (el miembro **wFormatTag** de una estructura [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), mientras que otras requieren formatos de audio de forma de onda completos (la estructura de **WaveFormatEx** completa).</span><span class="sxs-lookup"><span data-stu-id="cfc23-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="cfc23-120">(Para obtener información de referencia sobre la estructura **WAVEFORMATEX** , vea [error](error.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc23-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="cfc23-121">En el grupo filtro, algunas funciones usan etiquetas de filtro de audio de onda (el miembro **dwFilterTag** de la estructura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), mientras que otras requieren filtros de audio de onda completa (la estructura **WAVEFILTER** completa).</span><span class="sxs-lookup"><span data-stu-id="cfc23-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="cfc23-122">Las funciones del grupo de secuencias representan los numerosos pasos implicados en una conversión: abrir una instancia de conversión, preparar la conversión, realizar la conversión, limpiar una vez finalizada la conversión y cerrar la instancia de conversión.</span><span class="sxs-lookup"><span data-stu-id="cfc23-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 