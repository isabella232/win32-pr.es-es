---
title: Objeto Playlist
description: El objeto Playlist proporciona una manera de organizar los elementos multimedia de una lista para facilitar su manipulación mediante el uso de las siguientes propiedades y métodos.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Objeto de lista de reproducción Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076522"
---
# <a name="playlist-object"></a><span data-ttu-id="85c19-104">Objeto Playlist</span><span class="sxs-lookup"><span data-stu-id="85c19-104">Playlist Object</span></span>

<span data-ttu-id="85c19-105">El objeto **playlist** proporciona una manera de organizar los elementos multimedia de una lista para facilitar su manipulación mediante el uso de las siguientes propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="85c19-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="85c19-106">El objeto de **lista de reproducción** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="85c19-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="85c19-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85c19-107">Property</span></span>                                      | <span data-ttu-id="85c19-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c19-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="85c19-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="85c19-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="85c19-110">Recupera el número de atributos asociados a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="85c19-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="85c19-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="85c19-112">Recupera el nombre de un atributo especificado por un índice.</span><span class="sxs-lookup"><span data-stu-id="85c19-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="85c19-113">count</span><span class="sxs-lookup"><span data-stu-id="85c19-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="85c19-114">Recupera el número de elementos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="85c19-115">name</span><span class="sxs-lookup"><span data-stu-id="85c19-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="85c19-116">Especifica o recupera el nombre de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="85c19-117">El objeto de **lista de reproducción** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="85c19-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="85c19-118">Método</span><span class="sxs-lookup"><span data-stu-id="85c19-118">Method</span></span>                                  | <span data-ttu-id="85c19-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c19-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85c19-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="85c19-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="85c19-121">Agrega un elemento multimedia al final de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="85c19-122">**clear**</span><span class="sxs-lookup"><span data-stu-id="85c19-122">**clear**</span></span>                               | <span data-ttu-id="85c19-123">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="85c19-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="85c19-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="85c19-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="85c19-125">Recupera el valor de un atributo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="85c19-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="85c19-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="85c19-127">Inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="85c19-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="85c19-128">isIdentical</span><span class="sxs-lookup"><span data-stu-id="85c19-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="85c19-129">Recupera un valor que indica si el objeto de **lista de reproducción** proporcionado es idéntico al actual.</span><span class="sxs-lookup"><span data-stu-id="85c19-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="85c19-130">item</span><span class="sxs-lookup"><span data-stu-id="85c19-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="85c19-131">Recupera el elemento multimedia en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="85c19-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="85c19-132">moveItem</span><span class="sxs-lookup"><span data-stu-id="85c19-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="85c19-133">Cambia la ubicación de un elemento en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="85c19-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="85c19-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="85c19-135">Quita el elemento especificado de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="85c19-136">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="85c19-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="85c19-137">Especifica el valor de un atributo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="85c19-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="85c19-138">Se tiene acceso al objeto de **lista de reproducción** a través de las siguientes propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="85c19-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="85c19-139">Object</span><span class="sxs-lookup"><span data-stu-id="85c19-139">Object</span></span>                                              | <span data-ttu-id="85c19-140">Propiedad o método</span><span class="sxs-lookup"><span data-stu-id="85c19-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85c19-141">-</span><span class="sxs-lookup"><span data-stu-id="85c19-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="85c19-142">automáticas</span><span class="sxs-lookup"><span data-stu-id="85c19-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="85c19-143">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="85c19-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="85c19-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="85c19-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="85c19-145">Reproductor</span><span class="sxs-lookup"><span data-stu-id="85c19-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="85c19-146">[currentPlaylist](player-currentplaylist.md), [reproducción](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="85c19-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="85c19-147">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="85c19-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="85c19-148">item</span><span class="sxs-lookup"><span data-stu-id="85c19-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="85c19-149">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="85c19-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="85c19-150">Reproducción</span><span class="sxs-lookup"><span data-stu-id="85c19-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="85c19-151">Dado que es el medio de acceso más común, *Player*. **currentPlaylist** se usa con fines ilustrativos en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="85c19-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="85c19-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="85c19-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c19-153">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="85c19-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




