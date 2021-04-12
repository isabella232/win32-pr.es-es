---
description: Interfaces de streaming de audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538014"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="ea3ac-103">Interfaces de streaming de audio</span><span class="sxs-lookup"><span data-stu-id="ea3ac-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="ea3ac-104">Estas API están en desuso.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-104">These APIs are deprecated.</span></span> <span data-ttu-id="ea3ac-105">Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="ea3ac-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ea3ac-106">Interface</span></span>                                        | <span data-ttu-id="ea3ac-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea3ac-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea3ac-108">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="ea3ac-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="ea3ac-109">Controla los flujos multimedia de audio.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-109">Controls audio media streams.</span></span> <span data-ttu-id="ea3ac-110">Esta interfaz hereda de la interfaz [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y se usa para crear uno o más objetos [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="ea3ac-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="ea3ac-111">También se usa para establecer y recuperar el formato actual de los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="ea3ac-112">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="ea3ac-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="ea3ac-113">Recupera información de los objetos de datos [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subyacentes.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="ea3ac-114">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="ea3ac-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="ea3ac-115">Contiene métodos que establecen y recuperan datos de memoria en objetos de datos de audio.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="ea3ac-116">Los objetos de datos de audio proporcionan los datos subyacentes que tienen acceso a los ejemplos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="ea3ac-117">Esta interfaz proporciona una manera de inicializar los búferes de memoria y establecer la cantidad real de datos de audio en los objetos.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="ea3ac-118">Además, se puede usar el método [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) para recuperar los datos de la memoria de audio.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="ea3ac-119">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="ea3ac-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="ea3ac-120">Proporciona métodos que permiten a las aplicaciones establecer y obtener los datos de audio subyacentes a los que hará referencia las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="ea3ac-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="ea3ac-121">El formato de datos de audio se establece en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ea3ac-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ea3ac-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea3ac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea3ac-123">Lista de interfaces de streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="ea3ac-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
