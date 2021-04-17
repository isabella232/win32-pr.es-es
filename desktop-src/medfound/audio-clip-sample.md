---
description: Muestra cómo usar Microsoft Media Foundation para descodificar el audio de un archivo multimedia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Ejemplo de clip de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686472"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="81a65-103">Ejemplo de clip de audio</span><span class="sxs-lookup"><span data-stu-id="81a65-103">Audio Clip Sample</span></span>

<span data-ttu-id="81a65-104">Muestra cómo usar Microsoft Media Foundation para descodificar el audio de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="81a65-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="81a65-105">La aplicación de ejemplo de clip de audio Lee los datos de audio de un archivo multimedia y escribe el audio sin comprimir en un archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="81a65-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="81a65-106">API mostradas</span><span class="sxs-lookup"><span data-stu-id="81a65-106">APIs Demonstrated</span></span>

<span data-ttu-id="81a65-107">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="81a65-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="81a65-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="81a65-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="81a65-109">Uso</span><span class="sxs-lookup"><span data-stu-id="81a65-109">Usage</span></span>

<span data-ttu-id="81a65-110">Este ejemplo es una aplicación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="81a65-110">This sample is a command-line application.</span></span> <span data-ttu-id="81a65-111">Usa los siguientes argumentos de línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="81a65-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="81a65-112">ArchivoDeEntrada: el nombre de un archivo que contiene una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="81a65-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="81a65-113">OutputFile. wav: nombre del archivo de onda que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="81a65-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a65-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a65-114">Requirements</span></span>



| <span data-ttu-id="81a65-115">Producto</span><span class="sxs-lookup"><span data-stu-id="81a65-115">Product</span></span>                                                        | <span data-ttu-id="81a65-116">Versión</span><span class="sxs-lookup"><span data-stu-id="81a65-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="81a65-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="81a65-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="81a65-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81a65-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="81a65-119">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="81a65-119">Downloading the Sample</span></span>

<span data-ttu-id="81a65-120">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="81a65-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81a65-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81a65-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81a65-122">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81a65-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="81a65-123">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="81a65-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="81a65-124">Tutorial: descodificar audio</span><span class="sxs-lookup"><span data-stu-id="81a65-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



