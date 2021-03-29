---
description: Interfaces de streaming multimedia de base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de streaming multimedia de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003436"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="2471d-103">Interfaces de streaming multimedia de base</span><span class="sxs-lookup"><span data-stu-id="2471d-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="2471d-104">Estas API están en desuso.</span><span class="sxs-lookup"><span data-stu-id="2471d-104">These APIs are deprecated.</span></span> <span data-ttu-id="2471d-105">Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2471d-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="2471d-106">Las interfaces de streaming multimedia base proporcionan una manera programática de obtener acceso a las secuencias multimedia.</span><span class="sxs-lookup"><span data-stu-id="2471d-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="2471d-107">Sin embargo, el uso de una interfaz base para tener acceso a un tipo de datos específico puede limitar la cantidad de control que se obtiene sobre los datos, por lo que los desarrolladores de medios deben crear versiones derivadas de estas interfaces que proporcionen un control más eficaz sobre las funcionalidades únicas de su tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2471d-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="2471d-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="2471d-108">Interface</span></span>                                      | <span data-ttu-id="2471d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2471d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2471d-110">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="2471d-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="2471d-111">Define cómo obtener acceso al objeto de flujo multimedia de nivel superior. Este objeto contiene y proporciona acceso a otros objetos de flujo.</span><span class="sxs-lookup"><span data-stu-id="2471d-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="2471d-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) tiene métodos que enumeran o recuperan secuencias específicas, así como la comprobación del tiempo total de la secuencia y la búsqueda en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2471d-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="2471d-113">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="2471d-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="2471d-114">Define un objeto de flujo genérico.</span><span class="sxs-lookup"><span data-stu-id="2471d-114">Defines a generic stream object.</span></span> <span data-ttu-id="2471d-115">Use sus métodos para recuperar un puntero a la secuencia, obtener información sobre la secuencia y crear ejemplos a partir de los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2471d-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="2471d-116">También puede crear ejemplos de secuencias compartidas, a los que varias secuencias pueden tener acceso sin duplicar los datos del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2471d-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="2471d-117">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="2471d-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="2471d-118">Controla el comportamiento de un ejemplo de flujo concreto.</span><span class="sxs-lookup"><span data-stu-id="2471d-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="2471d-119">Puede recuperar la secuencia que creó el ejemplo, comprobar las horas de inicio y finalización del ejemplo, así como el estado de finalización, y realizar una función definida por el usuario en el propio ejemplo (mediante el método [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ).</span><span class="sxs-lookup"><span data-stu-id="2471d-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="2471d-120">Normalmente, el método Update procesa los datos de ejemplo de manera adecuada, como la representación de datos de vídeo o la reproducción de datos de audio.</span><span class="sxs-lookup"><span data-stu-id="2471d-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2471d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2471d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2471d-122">Lista de interfaces de streaming multimedia</span><span class="sxs-lookup"><span data-stu-id="2471d-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



