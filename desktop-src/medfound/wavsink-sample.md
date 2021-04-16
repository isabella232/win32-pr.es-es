---
description: Ejemplo de WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Ejemplo de WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696859"
---
# <a name="wavsink-sample"></a><span data-ttu-id="6a4ff-103">Ejemplo de WavSink</span><span class="sxs-lookup"><span data-stu-id="6a4ff-103">WavSink Sample</span></span>

<span data-ttu-id="6a4ff-104">Muestra cómo implementar un receptor de multimedia personalizado en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a4ff-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="6a4ff-105">En el ejemplo se implementa un receptor de archivo que escribe audio PCM sin comprimir en un archivo. wav.</span><span class="sxs-lookup"><span data-stu-id="6a4ff-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="6a4ff-106">API mostradas</span><span class="sxs-lookup"><span data-stu-id="6a4ff-106">APIs Demonstrated</span></span>

<span data-ttu-id="6a4ff-107">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="6a4ff-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="6a4ff-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="6a4ff-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="6a4ff-109">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="6a4ff-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="6a4ff-110">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="6a4ff-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="6a4ff-111">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="6a4ff-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="6a4ff-112">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="6a4ff-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="6a4ff-113">Uso</span><span class="sxs-lookup"><span data-stu-id="6a4ff-113">Usage</span></span>

<span data-ttu-id="6a4ff-114">El ejemplo WavSink contiene dos proyectos de Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="6a4ff-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="6a4ff-115">WavSink. vcproj crea una biblioteca estática que contiene la implementación del receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="6a4ff-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="6a4ff-116">WriteWavFile. vcproj crea una aplicación de consola que usa el receptor de medios para generar un archivo. wav.</span><span class="sxs-lookup"><span data-stu-id="6a4ff-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="6a4ff-117">Esta aplicación se vincula a la biblioteca creada por el proyecto WavSink.</span><span class="sxs-lookup"><span data-stu-id="6a4ff-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4ff-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a4ff-118">Requirements</span></span>



| <span data-ttu-id="6a4ff-119">Producto</span><span class="sxs-lookup"><span data-stu-id="6a4ff-119">Product</span></span>                                                        | <span data-ttu-id="6a4ff-120">Versión</span><span class="sxs-lookup"><span data-stu-id="6a4ff-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="6a4ff-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6a4ff-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="6a4ff-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a4ff-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6a4ff-123">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a4ff-123">Downloading the Sample</span></span>

<span data-ttu-id="6a4ff-124">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span><span class="sxs-lookup"><span data-stu-id="6a4ff-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a4ff-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a4ff-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a4ff-126">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a4ff-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="6a4ff-127">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="6a4ff-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



