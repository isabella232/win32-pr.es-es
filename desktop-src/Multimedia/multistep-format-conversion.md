---
title: Conversión de formato multipaso
description: Conversión de formato multipaso
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Administrador de compresión de audio (ACM), convertir datos
- ACM (Administrador de compresión de audio), convertir datos
- Ejemplos de ACM, convertir datos
- convertir datos
- acmFormatSuggest función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994284"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="3ee1e-108">Conversión de formato multipaso</span><span class="sxs-lookup"><span data-stu-id="3ee1e-108">Multistep Format Conversion</span></span>

<span data-ttu-id="3ee1e-109">A veces, el ACM no puede convertir datos de un formato a otro en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="3ee1e-110">Por ejemplo, es posible que una aplicación necesite convertir datos estéreo de 16 bits de 44 kHz a un ADPCM mono de 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="3ee1e-111">Si el compresor o el descompresor no pueden realizar esta conversión directamente, es posible que la aplicación la intente en dos pasos.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="3ee1e-112">Normalmente, esto significa hacer una conversión entre dos formatos PCM y, a continuación, otra conversión al tipo de formato final.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="3ee1e-113">Para realizar la conversión en dos pasos, utilice la función [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) para buscar un formato PCM que coincida con el formato ADPCM.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="3ee1e-114">A continuación, use dos flujos de conversión para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="3ee1e-115">Por ejemplo, realice una conversión del PCM estéreo de 16 bits 44-kHz a mono de 16 bits, de 11 kHz, y, a continuación, convierta de 16 bits a un ADPCM mono a 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="3ee1e-116">La conversión en un solo paso también se produce cuando el formato de origen o de destino no es PCM.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="3ee1e-117">Si el formato de origen no es PCM, debe cambiarse a un formato PCM antes de la conversión.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="3ee1e-118">Si el formato de destino no es PCM, el origen debe convertirse a un formato PCM intermedio y, a continuación, convertirse al formato de destino final.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="3ee1e-119">Las conversiones más directas se producen cuando los formatos de origen y destino son ambos formatos PCM.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="3ee1e-120">Cuando el formato de origen o destino no es PCM, la conversión podría requerir un paso adicional.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="3ee1e-121">Si los formatos de origen y destino no son PCM, la conversión normalmente requerirá más de un paso y, en algunos casos, la conversión podría no ser posible.</span><span class="sxs-lookup"><span data-stu-id="3ee1e-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




