---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Aspectos de Windows Media Player, elemento PLAYER
- máscaras, elemento PLAYER
- Elemento PLAYER
- referencia de las máscaras, elemento PLAYER
- elementos, reproductor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148831"
---
# <a name="player-element"></a><span data-ttu-id="b7492-108">Elemento PLAYER</span><span class="sxs-lookup"><span data-stu-id="b7492-108">PLAYER Element</span></span>

<span data-ttu-id="b7492-109">El elemento **Player** permite definir controladores de eventos y especificar la propiedad **URL** del objeto **Player** en tiempo de diseño dentro de un archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="b7492-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="b7492-110">En el código de script, se tiene acceso al objeto **Player** a través del atributo global **Player** en lugar de un nombre especificado por un atributo **ID** , que no es compatible con el elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="b7492-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="b7492-111">El elemento **Player** admite el siguiente atributo.</span><span class="sxs-lookup"><span data-stu-id="b7492-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="b7492-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7492-112">Attribute</span></span>             | <span data-ttu-id="b7492-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7492-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="b7492-114">URL</span><span class="sxs-lookup"><span data-stu-id="b7492-114">URL</span></span>](player-url.md) | <span data-ttu-id="b7492-115">Especifica o recupera el nombre del archivo que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="b7492-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="b7492-116">El elemento **Player** puede implementar controladores de eventos para los siguientes eventos desencadenados desde el objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="b7492-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="b7492-117">Evento</span><span class="sxs-lookup"><span data-stu-id="b7492-117">Event</span></span>                                                                                            | <span data-ttu-id="b7492-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7492-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="b7492-119">AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="b7492-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="b7492-120">Se produce cuando cambia el idioma actual del audio.</span><span class="sxs-lookup"><span data-stu-id="b7492-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="b7492-121">de respuesta</span><span class="sxs-lookup"><span data-stu-id="b7492-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="b7492-122">Se produce cuando Windows Media Player inicia o finaliza el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="b7492-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="b7492-123">CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="b7492-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="b7492-124">Se produce cuando cambia el medio del CD.</span><span class="sxs-lookup"><span data-stu-id="b7492-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="b7492-125">CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="b7492-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="b7492-126">Se produce cuando cambia el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="b7492-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="b7492-127">CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="b7492-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="b7492-128">Se produce cuando el elemento multimedia actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="b7492-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="b7492-129">CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="b7492-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="b7492-130">Se produce cuando cambia la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="b7492-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="b7492-131">CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="b7492-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="b7492-132">Se produce cuando el elemento de lista de reproducción actual está disponible.</span><span class="sxs-lookup"><span data-stu-id="b7492-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="b7492-133">DomainChange</span><span class="sxs-lookup"><span data-stu-id="b7492-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="b7492-134">Se produce cuando cambia el dominio del DVD.</span><span class="sxs-lookup"><span data-stu-id="b7492-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="b7492-135">Error</span><span class="sxs-lookup"><span data-stu-id="b7492-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="b7492-136">Se produce cuando el control de Media Player de Windows tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="b7492-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="b7492-137">MarkerHit</span><span class="sxs-lookup"><span data-stu-id="b7492-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="b7492-138">Se produce cuando Windows Media Player encuentra un marcador en el clip.</span><span class="sxs-lookup"><span data-stu-id="b7492-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="b7492-139">MediaChange</span><span class="sxs-lookup"><span data-stu-id="b7492-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="b7492-140">Se produce cuando cambia un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="b7492-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="b7492-141">MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="b7492-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="b7492-142">Se produce cuando se agrega un valor de atributo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b7492-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="b7492-143">MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="b7492-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="b7492-144">Se produce cuando se cambia un valor de atributo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b7492-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="b7492-145">MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="b7492-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="b7492-146">Se produce cuando se quita un valor de atributo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b7492-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="b7492-147">MediaCollectionChange</span><span class="sxs-lookup"><span data-stu-id="b7492-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="b7492-148">Se produce cuando cambia el objeto **MediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="b7492-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="b7492-149">MediaError</span><span class="sxs-lookup"><span data-stu-id="b7492-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="b7492-150">Se produce cuando el objeto **multimedia** tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="b7492-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="b7492-151">ModeChange</span><span class="sxs-lookup"><span data-stu-id="b7492-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="b7492-152">Tiene lugar cuando se cambia entre el modo de orden aleatorio y normal.</span><span class="sxs-lookup"><span data-stu-id="b7492-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="b7492-153">OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="b7492-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="b7492-154">Se produce cuando comienza a reproducirse un título en un DVD.</span><span class="sxs-lookup"><span data-stu-id="b7492-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="b7492-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="b7492-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="b7492-156">Se produce cuando el *reproductor*. **openState** cambios.</span><span class="sxs-lookup"><span data-stu-id="b7492-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="b7492-157">PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="b7492-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="b7492-158">Se produce cuando cambia una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7492-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="b7492-159">PlaylistCollectionChange</span><span class="sxs-lookup"><span data-stu-id="b7492-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="b7492-160">Se produce cuando hay algún cambio en la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7492-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="b7492-161">PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="b7492-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="b7492-162">Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7492-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="b7492-163">PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="b7492-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="b7492-164">Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7492-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="b7492-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="b7492-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="b7492-166">Se produce cuando el *reproductor*. **playState** cambios.</span><span class="sxs-lookup"><span data-stu-id="b7492-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="b7492-167">PositionChange</span><span class="sxs-lookup"><span data-stu-id="b7492-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="b7492-168">Se produce cuando el *reproductor*. *controles*. **currentPosition** cambios.</span><span class="sxs-lookup"><span data-stu-id="b7492-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="b7492-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="b7492-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="b7492-170">Se produce cuando Windows Media Player encuentra un comando de script incrustado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="b7492-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="b7492-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="b7492-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="b7492-172">Se produce cuando cambia el valor de la propiedad **status** .</span><span class="sxs-lookup"><span data-stu-id="b7492-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="b7492-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7492-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7492-174">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="b7492-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b7492-175">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="b7492-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




