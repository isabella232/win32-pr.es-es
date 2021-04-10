---
description: Interfaces de codificación y descodificación de archivos
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfaces de codificación y descodificación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152694"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="7d999-103">Interfaces de codificación y descodificación de archivos</span><span class="sxs-lookup"><span data-stu-id="7d999-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="7d999-104">Estas interfaces admiten la codificación y descodificación de archivos.</span><span class="sxs-lookup"><span data-stu-id="7d999-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="7d999-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="7d999-105">Interface</span></span>                                                    | <span data-ttu-id="7d999-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d999-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d999-107">**IAMMediaContent**</span><span class="sxs-lookup"><span data-stu-id="7d999-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="7d999-108">Recuperar metadatos de un flujo, como el autor y el título.</span><span class="sxs-lookup"><span data-stu-id="7d999-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="7d999-109">**IAMOpenProgress**</span><span class="sxs-lookup"><span data-stu-id="7d999-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="7d999-110">Determine el progreso de una operación de apertura de archivos.</span><span class="sxs-lookup"><span data-stu-id="7d999-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="7d999-111">**IAMParse**</span><span class="sxs-lookup"><span data-stu-id="7d999-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="7d999-112">Consultar y establecer el tiempo de análisis para la posición actual en una secuencia MPEG.</span><span class="sxs-lookup"><span data-stu-id="7d999-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="7d999-113">**IAMStreamSelect**</span><span class="sxs-lookup"><span data-stu-id="7d999-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="7d999-114">Controlar qué secuencias lógicas se reproducen y recuperar información sobre ellas.</span><span class="sxs-lookup"><span data-stu-id="7d999-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="7d999-115">**IAMVfwCompressDialogs**</span><span class="sxs-lookup"><span data-stu-id="7d999-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="7d999-116">Mostrar cuadros de diálogo proporcionados por códecs VFW.</span><span class="sxs-lookup"><span data-stu-id="7d999-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="7d999-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="7d999-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="7d999-118">Establecer parámetros de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7d999-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="7d999-119">**IConfigAsfWriter**</span><span class="sxs-lookup"><span data-stu-id="7d999-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="7d999-120">Controlar cómo el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) escribe archivos de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="7d999-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="7d999-121">**IConfigAviMux**</span><span class="sxs-lookup"><span data-stu-id="7d999-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="7d999-122">Controlar el modo en que el filtro de [AVI](avi-mux-filter.md) no escribe archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="7d999-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="7d999-123">**IConfigInterleaving**</span><span class="sxs-lookup"><span data-stu-id="7d999-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="7d999-124">Configurar la intercalación cuando el filtro de AVI MUX escribe archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="7d999-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="7d999-125">**IDVEnc**</span><span class="sxs-lookup"><span data-stu-id="7d999-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="7d999-126">Establezca la resolución de codificación en el filtro del [codificador de vídeo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7d999-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="7d999-127">**IDVSplitter**</span><span class="sxs-lookup"><span data-stu-id="7d999-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="7d999-128">Degradar la velocidad de fotogramas en una secuencia de vídeo digital (DV)</span><span class="sxs-lookup"><span data-stu-id="7d999-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="7d999-129">**IIPDVDec**</span><span class="sxs-lookup"><span data-stu-id="7d999-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="7d999-130">Establezca la resolución de descodificación en el filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7d999-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="7d999-131">**IPersistMediaPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="7d999-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="7d999-132">Establezca y recupere información y DISP fragmentos en secuencias AVI.</span><span class="sxs-lookup"><span data-stu-id="7d999-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7d999-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d999-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d999-134">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7d999-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



