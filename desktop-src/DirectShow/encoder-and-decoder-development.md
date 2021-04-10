---
description: Desarrollo del codificador y descodificador
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Desarrollo del codificador y descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152347"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="a08a8-103">Desarrollo del codificador y descodificador</span><span class="sxs-lookup"><span data-stu-id="a08a8-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="a08a8-104">Esta sección contiene artículos sobre el desarrollo de codificadores y descodificadores para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a08a8-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="a08a8-105">Estos temas no son relevantes para los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a08a8-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="a08a8-106">Un descodificador de software que admita DirectX video Acceleration (VA) debe implementarse como un filtro de transformación de copia de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a08a8-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="a08a8-107">Si el descodificador no admite DirectX VA, también puede implementarse como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="a08a8-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="a08a8-108">Un descodificador que se conecta a un representador de vídeo no debe implementarse como un filtro de transbordo en contexto, ya que esto dará lugar a una degradación significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a08a8-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="a08a8-109">Para obtener información sobre cómo escribir un filtro de transformación de copia, consulte [escribir filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a08a8-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="a08a8-110">Los codificadores de software se pueden implementar como filtros de transformación o DMOs.</span><span class="sxs-lookup"><span data-stu-id="a08a8-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="a08a8-111">Los codificadores no usan DirectX VA, ya que actualmente DirectX se usa solo para la descompresión.</span><span class="sxs-lookup"><span data-stu-id="a08a8-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="a08a8-112">La especificación de la API del codificador que se describe en esta sección es relevante para los codificadores de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="a08a8-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="a08a8-113">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="a08a8-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="a08a8-114">API del codificador</span><span class="sxs-lookup"><span data-stu-id="a08a8-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="a08a8-115">Interfaces y especificaciones del descodificador</span><span class="sxs-lookup"><span data-stu-id="a08a8-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="a08a8-116">Configuración del descodificador para Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="a08a8-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="a08a8-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a08a8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08a8-118">Usar la VMR para desarrolladores de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="a08a8-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



