---
description: Ejemplo de lista de reproducción
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Ejemplo de lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715509"
---
# <a name="playlist-sample"></a><span data-ttu-id="09384-103">Ejemplo de lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="09384-103">Playlist Sample</span></span>

<span data-ttu-id="09384-104">Muestra cómo utilizar Microsoft Media Foundation para reproducir una secuencia de archivos de audio en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="09384-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="09384-105">En el ejemplo se usa el [origen del secuenciador](sequencer-source.md) para crear y administrar la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="09384-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="09384-106">Este ejemplo ya no se incluye en el SDK de.</span><span class="sxs-lookup"><span data-stu-id="09384-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="09384-107">API mostradas</span><span class="sxs-lookup"><span data-stu-id="09384-107">APIs Demonstrated</span></span>

<span data-ttu-id="09384-108">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="09384-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="09384-109">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="09384-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="09384-110">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="09384-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="09384-111">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="09384-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="09384-112">Uso</span><span class="sxs-lookup"><span data-stu-id="09384-112">Usage</span></span>

<span data-ttu-id="09384-113">El ejemplo de lista de reproducción crea una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="09384-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="09384-114">Para crear una nueva lista de reproducción, seleccione **Agregar a lista de reproducción** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="09384-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="09384-115">En el cuadro de diálogo **Abrir archivo** , seleccione uno o más archivos de audio.</span><span class="sxs-lookup"><span data-stu-id="09384-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="09384-116">Los archivos se agregan a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="09384-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="09384-117">Para reproducir la secuencia, haga clic en **reproducir**.</span><span class="sxs-lookup"><span data-stu-id="09384-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="09384-118">Para pausar el segmento actual, haga clic en **pausar**.</span><span class="sxs-lookup"><span data-stu-id="09384-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="09384-119">Para detener el segmento actual, haga clic en **detener**.</span><span class="sxs-lookup"><span data-stu-id="09384-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="09384-120">Para ir a un archivo, haga doble clic en el elemento en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="09384-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="09384-121">Para eliminar un archivo de la lista de reproducción, seleccione el elemento en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="09384-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="09384-122">A continuación, seleccione **quitar de la lista de reproducción** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="09384-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="09384-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09384-123">Requirements</span></span>



| <span data-ttu-id="09384-124">Producto</span><span class="sxs-lookup"><span data-stu-id="09384-124">Product</span></span>                                                        | <span data-ttu-id="09384-125">Versión</span><span class="sxs-lookup"><span data-stu-id="09384-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="09384-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="09384-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="09384-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09384-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="09384-128">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="09384-128">Downloading the Sample</span></span>

<span data-ttu-id="09384-129">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="09384-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="09384-130">Location</span><span class="sxs-lookup"><span data-stu-id="09384-130">Location</span></span>                                                     | <span data-ttu-id="09384-131">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="09384-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="09384-132">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="09384-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="09384-133">*Raíz* \\ del SDK Ejemplo \\ de \\ lista de reproducción multimedia mediafoundation \\</span><span class="sxs-lookup"><span data-stu-id="09384-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09384-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09384-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="09384-135">[Ejemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09384-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="09384-136">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09384-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="09384-137">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="09384-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
