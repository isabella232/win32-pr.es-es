---
title: Codificación de Two-Pass
description: Codificación de Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codificación de dos pasos
- Windows Media Format SDK, codificación de paso 2
- códecs, codificación de dos pasos
- códecs, codificación de 2 pasos
- codificación de dos pasos, acerca de
- 2-paso de codificación, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075482"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="7f28f-109">Codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="7f28f-109">Two-Pass Encoding</span></span>

<span data-ttu-id="7f28f-110">La codificación de dos pasos es un método de codificación disponible con algunos códecs, como el códec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="7f28f-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="7f28f-111">Cuando se usa la codificación de dos pasos, el códec procesa dos veces todos los ejemplos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7f28f-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="7f28f-112">En el primer paso, el códec recopila información sobre el contenido de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7f28f-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="7f28f-113">En el segundo paso, el códec usa la información recopilada en el primer paso para optimizar el proceso de codificación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7f28f-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="7f28f-114">En el modo de codificación de velocidad de bits constante, los archivos codificados en dos fases suelen ser más eficaces que los archivos codificados en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="7f28f-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="7f28f-115">La VBR basada en la calidad, que es una pasada, genera una calidad más coherente que la VBR basada en la velocidad de bits, que es de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="7f28f-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="7f28f-116">No se puede usar la codificación de dos pasos en secuencias en directo.</span><span class="sxs-lookup"><span data-stu-id="7f28f-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f28f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f28f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f28f-118">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="7f28f-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="7f28f-119">**Uso de la codificación de Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="7f28f-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




