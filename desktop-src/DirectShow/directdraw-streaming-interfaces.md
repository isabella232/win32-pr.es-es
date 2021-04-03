---
description: Interfaces de streaming de DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079981"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="576f5-103">Interfaces de streaming de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="576f5-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="576f5-104">Estas API están en desuso.</span><span class="sxs-lookup"><span data-stu-id="576f5-104">These APIs are deprecated.</span></span> <span data-ttu-id="576f5-105">Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="576f5-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="576f5-106">Si usa formatos de vídeo compatibles con DirectDraw en las secuencias, las siguientes interfaces proporcionan un control más eficaz sobre los datos que las interfaces base más genéricas.</span><span class="sxs-lookup"><span data-stu-id="576f5-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="576f5-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="576f5-107">Interface</span></span>                                                  | <span data-ttu-id="576f5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="576f5-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="576f5-109">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="576f5-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="576f5-110">Establece y recupera el formato de flujo y el objeto de DirectDraw asociado al flujo multimedia. Esta interfaz se deriva de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span><span class="sxs-lookup"><span data-stu-id="576f5-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="576f5-111">También puede usar esta interfaz para crear ejemplos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="576f5-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="576f5-112">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="576f5-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="576f5-113">Permite adjuntar ejemplos de vídeo a superficies de DirectDraw. Esta interfaz se deriva de la interfaz [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) .</span><span class="sxs-lookup"><span data-stu-id="576f5-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="576f5-114">Cada superficie adjunta incluye un rectángulo de recorte para facilitar la representación.</span><span class="sxs-lookup"><span data-stu-id="576f5-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="576f5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="576f5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="576f5-116">Lista de interfaces de streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="576f5-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



