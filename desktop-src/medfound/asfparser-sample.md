---
description: Ejemplo de ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Ejemplo de ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275150"
---
# <a name="asfparser-sample"></a><span data-ttu-id="cd73d-103">Ejemplo de ASFParser</span><span class="sxs-lookup"><span data-stu-id="cd73d-103">ASFParser Sample</span></span>

<span data-ttu-id="cd73d-104">Muestra cómo analizar los datos de un archivo de formato de sistema avanzado (ASF) mediante los componentes ASF de bajo nivel en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cd73d-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="cd73d-105">En el ejemplo se muestran las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd73d-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="cd73d-106">Enumerar las secuencias de audio y vídeo en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="cd73d-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="cd73d-107">Seleccionar una secuencia de audio o de vídeo para su análisis.</span><span class="sxs-lookup"><span data-stu-id="cd73d-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="cd73d-108">Buscar un paquete en el momento deseado de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="cd73d-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="cd73d-109">Generar ejemplos comprimidos para la secuencia seleccionada.</span><span class="sxs-lookup"><span data-stu-id="cd73d-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="cd73d-110">Descodificar ejemplos de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="cd73d-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="cd73d-111">API mostradas</span><span class="sxs-lookup"><span data-stu-id="cd73d-111">APIs Demonstrated</span></span>

<span data-ttu-id="cd73d-112">Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="cd73d-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="cd73d-113">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="cd73d-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="cd73d-114">**IMFASFIndexer**</span><span class="sxs-lookup"><span data-stu-id="cd73d-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="cd73d-115">**IMFASFSplitter**</span><span class="sxs-lookup"><span data-stu-id="cd73d-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="cd73d-116">Uso</span><span class="sxs-lookup"><span data-stu-id="cd73d-116">Usage</span></span>

1.  <span data-ttu-id="cd73d-117">Para abrir un archivo ASF, haga clic en el botón **Abrir archivo multimedia...** .</span><span class="sxs-lookup"><span data-stu-id="cd73d-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="cd73d-118">Seleccione un archivo ASF y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="cd73d-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="cd73d-119">En el panel de **información** se muestra información sobre el archivo.</span><span class="sxs-lookup"><span data-stu-id="cd73d-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="cd73d-120">En **configuración del analizador**, seleccione la secuencia que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="cd73d-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="cd73d-121">Para generar ejemplos en orden inverso, seleccione **inverso**.</span><span class="sxs-lookup"><span data-stu-id="cd73d-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="cd73d-122">Para especificar el punto de inicio, arrastre el control deslizante hasta la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="cd73d-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="cd73d-123">Para comenzar el análisis, haga clic en el botón **generar ejemplos** .</span><span class="sxs-lookup"><span data-stu-id="cd73d-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="cd73d-124">En el panel de **información** se muestra información sobre los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="cd73d-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="cd73d-125">Para probar los ejemplos de la secuencia de audio, haga clic en el botón **probar audio** .</span><span class="sxs-lookup"><span data-stu-id="cd73d-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="cd73d-126">Para probar los ejemplos de la secuencia de vídeo, haga clic en el botón **Mostrar mapa de bits** .</span><span class="sxs-lookup"><span data-stu-id="cd73d-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd73d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd73d-127">Requirements</span></span>



| <span data-ttu-id="cd73d-128">Producto</span><span class="sxs-lookup"><span data-stu-id="cd73d-128">Product</span></span>                                                        | <span data-ttu-id="cd73d-129">Versión</span><span class="sxs-lookup"><span data-stu-id="cd73d-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="cd73d-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="cd73d-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="cd73d-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd73d-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cd73d-132">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd73d-132">Downloading the Sample</span></span>

<span data-ttu-id="cd73d-133">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span><span class="sxs-lookup"><span data-stu-id="cd73d-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd73d-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd73d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd73d-135">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd73d-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="cd73d-136">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd73d-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="cd73d-137">Tutorial: lectura de un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="cd73d-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="cd73d-138">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="cd73d-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



