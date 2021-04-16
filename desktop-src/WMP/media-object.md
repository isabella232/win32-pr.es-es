---
title: Objeto multimedia
description: El objeto multimedia proporciona una manera de especificar o recuperar propiedades de un elemento multimedia, utilizando las propiedades y los métodos siguientes.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Media Player de objetos multimedia de Windows
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695506"
---
# <a name="media-object"></a><span data-ttu-id="4937a-104">Objeto multimedia</span><span class="sxs-lookup"><span data-stu-id="4937a-104">Media Object</span></span>

<span data-ttu-id="4937a-105">El objeto **multimedia** proporciona una manera de especificar o recuperar propiedades de un elemento multimedia, utilizando las propiedades y los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4937a-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="4937a-106">El objeto **multimedia** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4937a-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="4937a-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4937a-107">Property</span></span>                                         | <span data-ttu-id="4937a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4937a-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4937a-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="4937a-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="4937a-110">Recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="4937a-111">duration</span><span class="sxs-lookup"><span data-stu-id="4937a-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="4937a-112">Recupera la duración en segundos del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4937a-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="4937a-113">durationString</span><span class="sxs-lookup"><span data-stu-id="4937a-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="4937a-114">Recupera un valor de **cadena** que indica la duración del elemento multimedia actual en formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="4937a-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="4937a-115">error</span><span class="sxs-lookup"><span data-stu-id="4937a-115">error</span></span>](media-error.md)                         | <span data-ttu-id="4937a-116">Recupera un objeto [ErrorItem](erroritem-object.md) si el elemento multimedia tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="4937a-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="4937a-117">imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="4937a-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="4937a-118">Recupera el alto del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4937a-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="4937a-119">imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="4937a-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="4937a-120">Recupera el ancho del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4937a-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="4937a-121">markerCount</span><span class="sxs-lookup"><span data-stu-id="4937a-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="4937a-122">Recupera el número de marcadores del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="4937a-123">name</span><span class="sxs-lookup"><span data-stu-id="4937a-123">name</span></span>](media-name.md)                           | <span data-ttu-id="4937a-124">Especifica o recupera el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="4937a-125">sourceURL</span><span class="sxs-lookup"><span data-stu-id="4937a-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="4937a-126">Recupera la dirección URL del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="4937a-127">El objeto **multimedia** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4937a-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="4937a-128">Método</span><span class="sxs-lookup"><span data-stu-id="4937a-128">Method</span></span>                                                       | <span data-ttu-id="4937a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4937a-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4937a-130">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="4937a-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="4937a-131">Recupera el número de atributos asociados al nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="4937a-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="4937a-132">getAttributeName</span><span class="sxs-lookup"><span data-stu-id="4937a-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="4937a-133">Recupera el nombre del atributo correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4937a-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="4937a-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="4937a-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="4937a-135">Recupera el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="4937a-136">getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="4937a-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="4937a-137">Recupera el valor del atributo con el número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4937a-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="4937a-138">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="4937a-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="4937a-139">Recupera el valor del atributo correspondiente al nombre de atributo, el idioma y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="4937a-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="4937a-140">getMarkerName</span><span class="sxs-lookup"><span data-stu-id="4937a-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="4937a-141">Recupera el nombre del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4937a-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="4937a-142">getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="4937a-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="4937a-143">Recupera la hora del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4937a-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="4937a-144">isIdentical</span><span class="sxs-lookup"><span data-stu-id="4937a-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="4937a-145">Recupera un valor que indica si el objeto proporcionado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="4937a-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="4937a-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="4937a-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="4937a-147">Recupera un valor que indica si el elemento multimedia especificado es un miembro de la lista de reproducción especificada.</span><span class="sxs-lookup"><span data-stu-id="4937a-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="4937a-148">isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="4937a-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="4937a-149">Recupera un valor que indica si se pueden editar los atributos del elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="4937a-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="4937a-150">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="4937a-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="4937a-151">Establece el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4937a-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="4937a-152">Se tiene acceso al objeto **multimedia** a través de las siguientes propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="4937a-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="4937a-153">Object</span><span class="sxs-lookup"><span data-stu-id="4937a-153">Object</span></span>                          | <span data-ttu-id="4937a-154">Propiedad o método</span><span class="sxs-lookup"><span data-stu-id="4937a-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4937a-155">Controles</span><span class="sxs-lookup"><span data-stu-id="4937a-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="4937a-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="4937a-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="4937a-157">Reproductor</span><span class="sxs-lookup"><span data-stu-id="4937a-157">Player</span></span>](player-object.md)     | <span data-ttu-id="4937a-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="4937a-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="4937a-159">Lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="4937a-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="4937a-160">item</span><span class="sxs-lookup"><span data-stu-id="4937a-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="4937a-161">Dado que es el medio de acceso más común, *Player*. **currentMedia** se usa con fines ilustrativos en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="4937a-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="4937a-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="4937a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4937a-163">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="4937a-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




