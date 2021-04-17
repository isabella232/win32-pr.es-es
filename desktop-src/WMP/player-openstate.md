---
title: Player. openState
description: La propiedad openState recupera un valor que indica el estado del origen de contenido.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Media Player de Windows Player. openState
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708214"
---
# <a name="playeropenstate"></a><span data-ttu-id="0547f-104">Player. openState</span><span class="sxs-lookup"><span data-stu-id="0547f-104">Player.openState</span></span>

<span data-ttu-id="0547f-105">La propiedad **openState** recupera un valor que indica el estado del origen de contenido.</span><span class="sxs-lookup"><span data-stu-id="0547f-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="0547f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0547f-106">Syntax</span></span>

<span data-ttu-id="0547f-107">*reproductor* . **openState**</span><span class="sxs-lookup"><span data-stu-id="0547f-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0547f-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0547f-108">Possible Values</span></span>

<span data-ttu-id="0547f-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0547f-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="0547f-110">La constante de enumeración de estilo C se puede derivar prefijando el valor de estado con "wmpos".</span><span class="sxs-lookup"><span data-stu-id="0547f-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="0547f-111">Por ejemplo, la constante para el estado PlaylistOpening es **wmposPlaylistOpening**.</span><span class="sxs-lookup"><span data-stu-id="0547f-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="0547f-112">Value</span><span class="sxs-lookup"><span data-stu-id="0547f-112">Value</span></span> | <span data-ttu-id="0547f-113">Estado</span><span class="sxs-lookup"><span data-stu-id="0547f-113">State</span></span>                   | <span data-ttu-id="0547f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0547f-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0547f-115">0</span><span class="sxs-lookup"><span data-stu-id="0547f-115">0</span></span>     | <span data-ttu-id="0547f-116">No definido</span><span class="sxs-lookup"><span data-stu-id="0547f-116">Undefined</span></span>               | <span data-ttu-id="0547f-117">Windows Media Player está en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="0547f-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="0547f-118">1</span><span class="sxs-lookup"><span data-stu-id="0547f-118">1</span></span>     | <span data-ttu-id="0547f-119">PlaylistChanging</span><span class="sxs-lookup"><span data-stu-id="0547f-119">PlaylistChanging</span></span>        | <span data-ttu-id="0547f-120">La nueva lista de reproducción está a punto de cargarse.</span><span class="sxs-lookup"><span data-stu-id="0547f-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="0547f-121">2</span><span class="sxs-lookup"><span data-stu-id="0547f-121">2</span></span>     | <span data-ttu-id="0547f-122">PlaylistLocating</span><span class="sxs-lookup"><span data-stu-id="0547f-122">PlaylistLocating</span></span>        | <span data-ttu-id="0547f-123">Windows Media Player está intentando localizar la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0547f-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="0547f-124">La lista de reproducción puede ser local (biblioteca o metarchivo con una extensión de nombre de archivo. ASX) o remota.</span><span class="sxs-lookup"><span data-stu-id="0547f-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="0547f-125">3</span><span class="sxs-lookup"><span data-stu-id="0547f-125">3</span></span>     | <span data-ttu-id="0547f-126">PlaylistConnecting</span><span class="sxs-lookup"><span data-stu-id="0547f-126">PlaylistConnecting</span></span>      | <span data-ttu-id="0547f-127">Conectando con la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="0547f-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="0547f-128">4</span><span class="sxs-lookup"><span data-stu-id="0547f-128">4</span></span>     | <span data-ttu-id="0547f-129">PlaylistLoading</span><span class="sxs-lookup"><span data-stu-id="0547f-129">PlaylistLoading</span></span>         | <span data-ttu-id="0547f-130">La lista de reproducción se ha encontrado y ahora se está recuperando.</span><span class="sxs-lookup"><span data-stu-id="0547f-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="0547f-131">5</span><span class="sxs-lookup"><span data-stu-id="0547f-131">5</span></span>     | <span data-ttu-id="0547f-132">PlaylistOpening</span><span class="sxs-lookup"><span data-stu-id="0547f-132">PlaylistOpening</span></span>         | <span data-ttu-id="0547f-133">La lista de reproducción se ha recuperado y ahora se está analizando y cargando.</span><span class="sxs-lookup"><span data-stu-id="0547f-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="0547f-134">6</span><span class="sxs-lookup"><span data-stu-id="0547f-134">6</span></span>     | <span data-ttu-id="0547f-135">PlaylistOpenNoMedia</span><span class="sxs-lookup"><span data-stu-id="0547f-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="0547f-136">La lista de reproducción está abierta.</span><span class="sxs-lookup"><span data-stu-id="0547f-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="0547f-137">7</span><span class="sxs-lookup"><span data-stu-id="0547f-137">7</span></span>     | <span data-ttu-id="0547f-138">PlaylistChanged</span><span class="sxs-lookup"><span data-stu-id="0547f-138">PlaylistChanged</span></span>         | <span data-ttu-id="0547f-139">Se ha asignado una nueva lista de reproducción a **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="0547f-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="0547f-140">8</span><span class="sxs-lookup"><span data-stu-id="0547f-140">8</span></span>     | <span data-ttu-id="0547f-141">MediaChanging</span><span class="sxs-lookup"><span data-stu-id="0547f-141">MediaChanging</span></span>           | <span data-ttu-id="0547f-142">Se va a cargar un nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0547f-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="0547f-143">9</span><span class="sxs-lookup"><span data-stu-id="0547f-143">9</span></span>     | <span data-ttu-id="0547f-144">MediaLocating</span><span class="sxs-lookup"><span data-stu-id="0547f-144">MediaLocating</span></span>           | <span data-ttu-id="0547f-145">Windows Media Player está localizando el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0547f-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="0547f-146">El archivo puede ser local o remoto.</span><span class="sxs-lookup"><span data-stu-id="0547f-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="0547f-147">10</span><span class="sxs-lookup"><span data-stu-id="0547f-147">10</span></span>    | <span data-ttu-id="0547f-148">MediaConnecting</span><span class="sxs-lookup"><span data-stu-id="0547f-148">MediaConnecting</span></span>         | <span data-ttu-id="0547f-149">Conectando con el servidor que contiene el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0547f-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="0547f-150">11</span><span class="sxs-lookup"><span data-stu-id="0547f-150">11</span></span>    | <span data-ttu-id="0547f-151">MediaLoading</span><span class="sxs-lookup"><span data-stu-id="0547f-151">MediaLoading</span></span>            | <span data-ttu-id="0547f-152">El elemento multimedia se ha encontrado y ahora se está recuperando.</span><span class="sxs-lookup"><span data-stu-id="0547f-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="0547f-153">12</span><span class="sxs-lookup"><span data-stu-id="0547f-153">12</span></span>    | <span data-ttu-id="0547f-154">MediaOpening</span><span class="sxs-lookup"><span data-stu-id="0547f-154">MediaOpening</span></span>            | <span data-ttu-id="0547f-155">El elemento multimedia se ha recuperado y ahora se está abriendo.</span><span class="sxs-lookup"><span data-stu-id="0547f-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="0547f-156">13</span><span class="sxs-lookup"><span data-stu-id="0547f-156">13</span></span>    | <span data-ttu-id="0547f-157">MediaOpen</span><span class="sxs-lookup"><span data-stu-id="0547f-157">MediaOpen</span></span>               | <span data-ttu-id="0547f-158">El elemento multimedia está abierto ahora.</span><span class="sxs-lookup"><span data-stu-id="0547f-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="0547f-159">14</span><span class="sxs-lookup"><span data-stu-id="0547f-159">14</span></span>    | <span data-ttu-id="0547f-160">BeginCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="0547f-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="0547f-161">Iniciando la adquisición del códec.</span><span class="sxs-lookup"><span data-stu-id="0547f-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="0547f-162">15</span><span class="sxs-lookup"><span data-stu-id="0547f-162">15</span></span>    | <span data-ttu-id="0547f-163">EndCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="0547f-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="0547f-164">Se completó la adquisición del códec.</span><span class="sxs-lookup"><span data-stu-id="0547f-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="0547f-165">16</span><span class="sxs-lookup"><span data-stu-id="0547f-165">16</span></span>    | <span data-ttu-id="0547f-166">BeginLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="0547f-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="0547f-167">Adquirir una licencia para reproducir contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="0547f-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="0547f-168">17</span><span class="sxs-lookup"><span data-stu-id="0547f-168">17</span></span>    | <span data-ttu-id="0547f-169">EndLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="0547f-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="0547f-170">Se ha adquirido una licencia para reproducir contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="0547f-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="0547f-171">18</span><span class="sxs-lookup"><span data-stu-id="0547f-171">18</span></span>    | <span data-ttu-id="0547f-172">BeginIndividualization</span><span class="sxs-lookup"><span data-stu-id="0547f-172">BeginIndividualization</span></span>  | <span data-ttu-id="0547f-173">Iniciar la individualización de DRM.</span><span class="sxs-lookup"><span data-stu-id="0547f-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="0547f-174">19</span><span class="sxs-lookup"><span data-stu-id="0547f-174">19</span></span>    | <span data-ttu-id="0547f-175">EndIndividualization</span><span class="sxs-lookup"><span data-stu-id="0547f-175">EndIndividualization</span></span>    | <span data-ttu-id="0547f-176">Se completó la individualización de DRM.</span><span class="sxs-lookup"><span data-stu-id="0547f-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="0547f-177">20</span><span class="sxs-lookup"><span data-stu-id="0547f-177">20</span></span>    | <span data-ttu-id="0547f-178">MediaWaiting</span><span class="sxs-lookup"><span data-stu-id="0547f-178">MediaWaiting</span></span>            | <span data-ttu-id="0547f-179">Esperando el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="0547f-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="0547f-180">21</span><span class="sxs-lookup"><span data-stu-id="0547f-180">21</span></span>    | <span data-ttu-id="0547f-181">OpeningUnknownURL</span><span class="sxs-lookup"><span data-stu-id="0547f-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="0547f-182">Abrir una dirección URL con un tipo desconocido.</span><span class="sxs-lookup"><span data-stu-id="0547f-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0547f-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0547f-183">Remarks</span></span>

<span data-ttu-id="0547f-184">No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="0547f-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="0547f-185">Además, no todos los Estados se producen necesariamente durante una secuencia de eventos.</span><span class="sxs-lookup"><span data-stu-id="0547f-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="0547f-186">No debe escribir código que se base en el orden de los Estados.</span><span class="sxs-lookup"><span data-stu-id="0547f-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="0547f-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0547f-187">Requirements</span></span>



| <span data-ttu-id="0547f-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="0547f-188">Requirement</span></span> | <span data-ttu-id="0547f-189">Value</span><span class="sxs-lookup"><span data-stu-id="0547f-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0547f-190">Versión</span><span class="sxs-lookup"><span data-stu-id="0547f-190">Version</span></span><br/> | <span data-ttu-id="0547f-191">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0547f-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0547f-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0547f-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="0547f-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0547f-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0547f-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="0547f-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0547f-195">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="0547f-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0547f-196">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="0547f-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





