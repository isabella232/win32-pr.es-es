---
description: Uso de orígenes multimedia con la sesión multimedia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso de orígenes multimedia con la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003352"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="d01bc-103">Uso de orígenes multimedia con la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="d01bc-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="d01bc-104">Si está utilizando la sesión multimedia para controlar la reproducción, se restringe el conjunto de métodos que debe llamar en un origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="d01bc-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="d01bc-105">En esta sección se describe cómo usar el origen de medios junto con la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="d01bc-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="d01bc-106">Estos son los pasos básicos que realizará la aplicación:</span><span class="sxs-lookup"><span data-stu-id="d01bc-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="d01bc-107">Cree el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d01bc-107">Create the media source.</span></span> <span data-ttu-id="d01bc-108">Para crear un origen multimedia, use la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="d01bc-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="d01bc-109">Para obtener más información, consulte [solucionador de código fuente](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="d01bc-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="d01bc-110">La resolución de origen devuelve un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen.</span><span class="sxs-lookup"><span data-stu-id="d01bc-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="d01bc-111">(Si ha escrito un origen multimedia personalizado, puede proporcionar un método de creación personalizado en su lugar).</span><span class="sxs-lookup"><span data-stu-id="d01bc-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="d01bc-112">Configure la presentación.</span><span class="sxs-lookup"><span data-stu-id="d01bc-112">Configure the presentation.</span></span> <span data-ttu-id="d01bc-113">Para configurar la presentación del origen, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="d01bc-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="d01bc-114">Puede modificar esta copia, pero los cambios no se activan hasta que se inicia la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d01bc-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="d01bc-115">No modifique el descriptor de presentación durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d01bc-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="d01bc-116">Para obtener más información, vea [descriptores de presentación](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d01bc-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="d01bc-117">Cree una topología que contenga el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d01bc-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="d01bc-118">Para obtener más información, vea [topologías](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="d01bc-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="d01bc-119">Utilice la sesión multimedia para controlar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d01bc-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="d01bc-120">La sesión multimedia llama a métodos en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d01bc-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="d01bc-121">En este momento, la aplicación no debe llamar a ningún método en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="d01bc-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="d01bc-122">Antes de liberar el origen multimedia, llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen.</span><span class="sxs-lookup"><span data-stu-id="d01bc-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="d01bc-123">Si usa el origen del secuenciador, el origen del secuenciador controla el cierre de los orígenes del segmento.</span><span class="sxs-lookup"><span data-stu-id="d01bc-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="d01bc-124">Para obtener más información, vea [Sequencer Source](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="d01bc-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="d01bc-125">Si usa la sesión multimedia, los únicos métodos que debe llamar en el origen del medio son [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)y [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="d01bc-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="d01bc-126">En concreto:</span><span class="sxs-lookup"><span data-stu-id="d01bc-126">In particular:</span></span>

-   <span data-ttu-id="d01bc-127">No llamar a [**iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**pausar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**detener**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); solo la sesión multimedia debe llamar a estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d01bc-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="d01bc-128">No llame a ningún método [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .</span><span class="sxs-lookup"><span data-stu-id="d01bc-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="d01bc-129">No recupere eventos directamente desde el origen de medios ni desde ninguna de las secuencias.</span><span class="sxs-lookup"><span data-stu-id="d01bc-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="d01bc-130">La sesión multimedia debe recibir estos eventos para que la canalización funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d01bc-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="d01bc-131">La sesión multimedia reenvía los eventos necesarios para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d01bc-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d01bc-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d01bc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d01bc-133">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="d01bc-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



