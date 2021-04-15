---
title: Player. playState
description: La propiedad playState recupera un valor que indica el estado de la operación de Media Player de Windows.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Media Player de Windows Player. playState
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708821"
---
# <a name="playerplaystate"></a><span data-ttu-id="757ad-104">Player. playState</span><span class="sxs-lookup"><span data-stu-id="757ad-104">Player.playState</span></span>

<span data-ttu-id="757ad-105">La propiedad **playState** recupera un valor que indica el estado de la operación de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="757ad-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="757ad-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="757ad-106">Syntax</span></span>

<span data-ttu-id="757ad-107">*reproductor* . **playState**</span><span class="sxs-lookup"><span data-stu-id="757ad-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="757ad-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="757ad-108">Possible Values</span></span>

<span data-ttu-id="757ad-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="757ad-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="757ad-110">La constante de enumeración de estilo C se puede derivar prefijando el valor de estado con "wmpps".</span><span class="sxs-lookup"><span data-stu-id="757ad-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="757ad-111">Por ejemplo, la constante para el estado Playing es **wmppsPlaying**.</span><span class="sxs-lookup"><span data-stu-id="757ad-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="757ad-112">Value</span><span class="sxs-lookup"><span data-stu-id="757ad-112">Value</span></span> | <span data-ttu-id="757ad-113">Estado</span><span class="sxs-lookup"><span data-stu-id="757ad-113">State</span></span>         | <span data-ttu-id="757ad-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="757ad-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="757ad-115">0</span><span class="sxs-lookup"><span data-stu-id="757ad-115">0</span></span>     | <span data-ttu-id="757ad-116">No definido</span><span class="sxs-lookup"><span data-stu-id="757ad-116">Undefined</span></span>     | <span data-ttu-id="757ad-117">Windows Media Player está en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="757ad-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="757ad-118">1</span><span class="sxs-lookup"><span data-stu-id="757ad-118">1</span></span>     | <span data-ttu-id="757ad-119">Detenido</span><span class="sxs-lookup"><span data-stu-id="757ad-119">Stopped</span></span>       | <span data-ttu-id="757ad-120">La reproducción del elemento multimedia actual está detenida.</span><span class="sxs-lookup"><span data-stu-id="757ad-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="757ad-121">2</span><span class="sxs-lookup"><span data-stu-id="757ad-121">2</span></span>     | <span data-ttu-id="757ad-122">En pausa</span><span class="sxs-lookup"><span data-stu-id="757ad-122">Paused</span></span>        | <span data-ttu-id="757ad-123">La reproducción del elemento multimedia actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="757ad-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="757ad-124">Cuando se pausa un elemento multimedia, reanudar la reproducción comienza en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="757ad-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="757ad-125">3</span><span class="sxs-lookup"><span data-stu-id="757ad-125">3</span></span>     | <span data-ttu-id="757ad-126">Reproduciendo</span><span class="sxs-lookup"><span data-stu-id="757ad-126">Playing</span></span>       | <span data-ttu-id="757ad-127">El elemento multimedia actual se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="757ad-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="757ad-128">4</span><span class="sxs-lookup"><span data-stu-id="757ad-128">4</span></span>     | <span data-ttu-id="757ad-129">ScanForward</span><span class="sxs-lookup"><span data-stu-id="757ad-129">ScanForward</span></span>   | <span data-ttu-id="757ad-130">El elemento multimedia actual es el reenvío rápido.</span><span class="sxs-lookup"><span data-stu-id="757ad-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="757ad-131">5</span><span class="sxs-lookup"><span data-stu-id="757ad-131">5</span></span>     | <span data-ttu-id="757ad-132">ScanReverse</span><span class="sxs-lookup"><span data-stu-id="757ad-132">ScanReverse</span></span>   | <span data-ttu-id="757ad-133">El elemento multimedia actual es un rebobinado rápido.</span><span class="sxs-lookup"><span data-stu-id="757ad-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="757ad-134">6</span><span class="sxs-lookup"><span data-stu-id="757ad-134">6</span></span>     | <span data-ttu-id="757ad-135">de respuesta</span><span class="sxs-lookup"><span data-stu-id="757ad-135">Buffering</span></span>     | <span data-ttu-id="757ad-136">El elemento multimedia actual está obteniendo datos adicionales del servidor.</span><span class="sxs-lookup"><span data-stu-id="757ad-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="757ad-137">7</span><span class="sxs-lookup"><span data-stu-id="757ad-137">7</span></span>     | <span data-ttu-id="757ad-138">En espera</span><span class="sxs-lookup"><span data-stu-id="757ad-138">Waiting</span></span>       | <span data-ttu-id="757ad-139">Se establece la conexión, pero el servidor no envía datos.</span><span class="sxs-lookup"><span data-stu-id="757ad-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="757ad-140">Esperando a que se inicie la sesión.</span><span class="sxs-lookup"><span data-stu-id="757ad-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="757ad-141">8</span><span class="sxs-lookup"><span data-stu-id="757ad-141">8</span></span>     | <span data-ttu-id="757ad-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="757ad-142">MediaEnded</span></span>    | <span data-ttu-id="757ad-143">El elemento multimedia ha finalizado la reproducción.</span><span class="sxs-lookup"><span data-stu-id="757ad-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="757ad-144">9</span><span class="sxs-lookup"><span data-stu-id="757ad-144">9</span></span>     | <span data-ttu-id="757ad-145">En transición</span><span class="sxs-lookup"><span data-stu-id="757ad-145">Transitioning</span></span> | <span data-ttu-id="757ad-146">Preparando nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="757ad-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="757ad-147">10</span><span class="sxs-lookup"><span data-stu-id="757ad-147">10</span></span>    | <span data-ttu-id="757ad-148">Ready</span><span class="sxs-lookup"><span data-stu-id="757ad-148">Ready</span></span>         | <span data-ttu-id="757ad-149">Listo para comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="757ad-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="757ad-150">11</span><span class="sxs-lookup"><span data-stu-id="757ad-150">11</span></span>    | <span data-ttu-id="757ad-151">Reconexión</span><span class="sxs-lookup"><span data-stu-id="757ad-151">Reconnecting</span></span>  | <span data-ttu-id="757ad-152">Volver a conectar a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="757ad-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="757ad-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="757ad-153">Remarks</span></span>

<span data-ttu-id="757ad-154">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="757ad-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="757ad-155">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="757ad-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="757ad-156">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="757ad-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="757ad-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="757ad-157">Examples</span></span>

<span data-ttu-id="757ad-158">El siguiente código JScript muestra el uso del *reproductor*. propiedad **playState** .</span><span class="sxs-lookup"><span data-stu-id="757ad-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="757ad-159">Un elemento de texto HTML, denominado "mi texto", muestra el estado actual.</span><span class="sxs-lookup"><span data-stu-id="757ad-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="757ad-160">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="757ad-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="757ad-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757ad-161">Requirements</span></span>



| <span data-ttu-id="757ad-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="757ad-162">Requirement</span></span> | <span data-ttu-id="757ad-163">Value</span><span class="sxs-lookup"><span data-stu-id="757ad-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="757ad-164">Versión</span><span class="sxs-lookup"><span data-stu-id="757ad-164">Version</span></span><br/> | <span data-ttu-id="757ad-165">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="757ad-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="757ad-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="757ad-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="757ad-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757ad-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757ad-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="757ad-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757ad-169">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="757ad-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="757ad-170">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="757ad-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





