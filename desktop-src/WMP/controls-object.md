---
title: Controls (objeto)
description: El objeto Controls proporciona una manera de manipular la reproducción de archivos multimedia con las siguientes propiedades y métodos.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Objetos de control Media Player de Windows
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103784486"
---
# <a name="controls-object"></a><span data-ttu-id="88cd3-104">Controls (objeto)</span><span class="sxs-lookup"><span data-stu-id="88cd3-104">Controls Object</span></span>

<span data-ttu-id="88cd3-105">El objeto **Controls** proporciona una manera de manipular la reproducción de archivos multimedia con las siguientes propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="88cd3-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="88cd3-106">El objeto **Controls** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="88cd3-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="88cd3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88cd3-107">Property</span></span>                                                            | <span data-ttu-id="88cd3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="88cd3-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88cd3-109">audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="88cd3-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="88cd3-110">Recupera el número de idiomas de audio admitidos.</span><span class="sxs-lookup"><span data-stu-id="88cd3-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="88cd3-111">currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="88cd3-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="88cd3-112">Especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="88cd3-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="88cd3-113">currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="88cd3-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="88cd3-114">Especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="88cd3-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="88cd3-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="88cd3-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="88cd3-116">Especifica o recupera el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="88cd3-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="88cd3-117">currentMarker</span><span class="sxs-lookup"><span data-stu-id="88cd3-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="88cd3-118">Especifica o recupera el número de marcador actual.</span><span class="sxs-lookup"><span data-stu-id="88cd3-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="88cd3-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="88cd3-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="88cd3-120">Especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.</span><span class="sxs-lookup"><span data-stu-id="88cd3-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="88cd3-121">currentPositionString</span><span class="sxs-lookup"><span data-stu-id="88cd3-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="88cd3-122">Recupera la posición actual en el elemento multimedia como una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="88cd3-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="88cd3-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="88cd3-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="88cd3-124">Especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="88cd3-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="88cd3-125">Esta propiedad admite actualmente código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="88cd3-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="88cd3-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="88cd3-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="88cd3-127">Recupera si un tipo de información especificado está disponible o se puede realizar una acción determinada.</span><span class="sxs-lookup"><span data-stu-id="88cd3-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="88cd3-128">El objeto **Controls** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="88cd3-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="88cd3-129">Método</span><span class="sxs-lookup"><span data-stu-id="88cd3-129">Method</span></span>                                                                  | <span data-ttu-id="88cd3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="88cd3-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88cd3-131">fastForward</span><span class="sxs-lookup"><span data-stu-id="88cd3-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="88cd3-132">Inicia la reproducción rápida del elemento multimedia en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="88cd3-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="88cd3-133">fastReverse</span><span class="sxs-lookup"><span data-stu-id="88cd3-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="88cd3-134">Inicia la reproducción rápida del elemento multimedia en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="88cd3-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="88cd3-135">getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="88cd3-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="88cd3-136">Recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.</span><span class="sxs-lookup"><span data-stu-id="88cd3-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="88cd3-137">getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="88cd3-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="88cd3-138">Recupera el LCID para un índice de idioma de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="88cd3-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="88cd3-139">getLanguageName</span><span class="sxs-lookup"><span data-stu-id="88cd3-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="88cd3-140">Recupera el nombre del idioma de audio con el LCID especificado.</span><span class="sxs-lookup"><span data-stu-id="88cd3-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="88cd3-141">siguiente</span><span class="sxs-lookup"><span data-stu-id="88cd3-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="88cd3-142">Establece el elemento actual en el elemento siguiente de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="88cd3-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="88cd3-143">pause</span><span class="sxs-lookup"><span data-stu-id="88cd3-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="88cd3-144">Pausa la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="88cd3-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="88cd3-145">reproducción</span><span class="sxs-lookup"><span data-stu-id="88cd3-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="88cd3-146">Hace que el elemento multimedia empiece a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="88cd3-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="88cd3-147">playItem</span><span class="sxs-lookup"><span data-stu-id="88cd3-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="88cd3-148">Hace que el elemento multimedia actual empiece a reproducir o reanuda la reproducción de un elemento en pausa.</span><span class="sxs-lookup"><span data-stu-id="88cd3-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="88cd3-149">previous</span><span class="sxs-lookup"><span data-stu-id="88cd3-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="88cd3-150">Establece el elemento actual en el elemento anterior de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="88cd3-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="88cd3-151">pasar</span><span class="sxs-lookup"><span data-stu-id="88cd3-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="88cd3-152">Hace que el elemento multimedia de vídeo actual inmovilice la reproducción en el fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="88cd3-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="88cd3-153">stop</span><span class="sxs-lookup"><span data-stu-id="88cd3-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="88cd3-154">Detiene la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="88cd3-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="88cd3-155">Se tiene acceso al objeto de **controles** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="88cd3-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="88cd3-156">Object</span><span class="sxs-lookup"><span data-stu-id="88cd3-156">Object</span></span>                      | <span data-ttu-id="88cd3-157">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88cd3-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="88cd3-158">Reproductor</span><span class="sxs-lookup"><span data-stu-id="88cd3-158">Player</span></span>](player-object.md) | [<span data-ttu-id="88cd3-159">permite</span><span class="sxs-lookup"><span data-stu-id="88cd3-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="88cd3-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="88cd3-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cd3-161">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="88cd3-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




