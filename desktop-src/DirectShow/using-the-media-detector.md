---
description: Uso del detector de medios
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Uso del detector de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678625"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="6a996-103">Uso del detector de medios</span><span class="sxs-lookup"><span data-stu-id="6a996-103">Using the Media Detector</span></span>

<span data-ttu-id="6a996-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="6a996-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6a996-105">El detector de medios es un objeto auxiliar que puede recuperar información sobre un archivo, como el número de flujos, su tipo y su duración.</span><span class="sxs-lookup"><span data-stu-id="6a996-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="6a996-106">También contiene métodos para recuperar fotogramas de póster de un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a996-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="6a996-107">Expone la interfaz [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="6a996-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="6a996-108">El detector de medios funciona en uno de dos modos.</span><span class="sxs-lookup"><span data-stu-id="6a996-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="6a996-109">Cuando se crea una instancia del detector de medios, no se adjunta a un archivo de origen determinado.</span><span class="sxs-lookup"><span data-stu-id="6a996-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="6a996-110">En este modo, puede recuperar la información de la secuencia de varios archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6a996-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="6a996-111">Sin embargo, una vez que use el detector de medios para obtener un fotograma de póster, cambia al *modo de agarre de mapa de bits*.</span><span class="sxs-lookup"><span data-stu-id="6a996-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="6a996-112">En el modo de captura de mapa de bits, el detector de medios se adjunta a una secuencia de vídeo específica y los métodos de información de la secuencia ya no funcionan.</span><span class="sxs-lookup"><span data-stu-id="6a996-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="6a996-113">Además, no hay forma de volver a cambiar el detector de medios a su modo de inicio.</span><span class="sxs-lookup"><span data-stu-id="6a996-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="6a996-114">Por lo tanto, obtenga cualquier información de flujo que necesite antes de recuperar fotogramas de póster, o bien cree nuevas instancias del detector de medios para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="6a996-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="6a996-115">Para obtener información de la secuencia, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a996-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="6a996-116">Llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT con el nombre del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6a996-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="6a996-117">Llame a [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de flujos en el origen.</span><span class="sxs-lookup"><span data-stu-id="6a996-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="6a996-118">Especifique un número de secuencia con [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="6a996-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="6a996-119">A continuación, llame a uno o varios de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a996-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="6a996-120">[**IMediaDet:: get \_ StreamType**](imediadet-get-streamtype.md): recupera el tipo de archivo multimedia de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6a996-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="6a996-121">[**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md): recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6a996-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="6a996-122">[**IMediaDet:: get \_ Velocidad de**](imediadet-get-framerate.md)fotogramas: recupera la velocidad de fotogramas de un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a996-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="6a996-123">Para obtener un fotograma de póster, especifique el número de secuencia, como en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="6a996-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="6a996-124">Después, llame a [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), que copia un fotograma de póster en un búfer o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), que guarda un fotograma de póster en un archivo.</span><span class="sxs-lookup"><span data-stu-id="6a996-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a996-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a996-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a996-126">Trabajar con orígenes</span><span class="sxs-lookup"><span data-stu-id="6a996-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



