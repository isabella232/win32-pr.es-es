---
title: Codificación de velocidad de bits constante (CBR)
description: Codificación de velocidad de bits constante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, codificación CBR
- Windows Media Format SDK, velocidad de bits constante (CBR)
- códecs, codificación CBR
- códecs, velocidad de bits constante (CBR)
- velocidad de bits constante (CBR)
- CBR (velocidad de bits constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419051"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="d7de1-109">Codificación de velocidad de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="d7de1-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="d7de1-110">La codificación de velocidad de bits constante (CBR) es el método predeterminado de codificación con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d7de1-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="d7de1-111">Cuando se usa la codificación CBR, se especifica la velocidad de bits de destino de una secuencia y el códec utiliza cualquier cantidad de compresión necesaria para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="d7de1-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="d7de1-112">Con la codificación CBR, la velocidad de bits y el tamaño de la secuencia codificada se conocen antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="d7de1-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="d7de1-113">Por ejemplo, si está codificando una canción de tres minutos en 32.000 bits por segundo, sabe que el tamaño del archivo será de aproximadamente 704 kilobytes (32.000 BPS x 180 segundos/8 bits por byte/1.024).</span><span class="sxs-lookup"><span data-stu-id="d7de1-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="d7de1-114">También sabe que el ancho de banda necesario para transmitir por secuencias el contenido codificado es aproximadamente 32.000 bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d7de1-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="d7de1-115">La codificación de velocidad de bits variable restringida (descrita en la sección siguiente) también le permite conocer la velocidad de bits antes de la codificación, pero como la velocidad es variable, el archivo resultante no se puede transmitir de forma eficaz como un archivo codificado en modo CBR.</span><span class="sxs-lookup"><span data-stu-id="d7de1-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="d7de1-116">Con CBR, la velocidad de bits a lo largo del tiempo siempre permanece cerca de la velocidad de bits media o de destino, y se puede especificar la cantidad de variación.</span><span class="sxs-lookup"><span data-stu-id="d7de1-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="d7de1-117">La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante.</span><span class="sxs-lookup"><span data-stu-id="d7de1-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="d7de1-118">Dado que el contenido es más difícil de comprimir, las partes de un flujo CBR serán de menor calidad que otras.</span><span class="sxs-lookup"><span data-stu-id="d7de1-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="d7de1-119">Por ejemplo, una película típica tiene algunas escenas que son bastante estáticas y algunas escenas que están llenas de acción.</span><span class="sxs-lookup"><span data-stu-id="d7de1-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="d7de1-120">Si codifica una película con CBR, las escenas que son estáticas y, por lo tanto, resultan fáciles de codificar de forma eficaz, tendrán una mayor calidad que las escenas de acción, que son mucho más difíciles de codificar de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="d7de1-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="d7de1-121">La codificación CBR también puede producir una calidad incoherente de un archivo a otro.</span><span class="sxs-lookup"><span data-stu-id="d7de1-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="d7de1-122">Si usa CBR para codificar varias canciones de géneros diferentes a la misma velocidad de bits, puede observar una diferencia en la calidad entre ellos.</span><span class="sxs-lookup"><span data-stu-id="d7de1-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="d7de1-123">En general, las variaciones en la calidad de un archivo CBR son más pronunciadas a velocidades de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="d7de1-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="d7de1-124">A velocidades de bits más altas, la calidad de un archivo con codificación CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d7de1-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="d7de1-125">Cuando se usa la codificación CBR, se debe establecer el ancho de banda tan alto como permita el escenario de entrega.</span><span class="sxs-lookup"><span data-stu-id="d7de1-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7de1-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7de1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7de1-127">**Elección de un método de codificación**</span><span class="sxs-lookup"><span data-stu-id="d7de1-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="d7de1-128">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="d7de1-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="d7de1-129">**Codificación de velocidad de bits variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="d7de1-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




