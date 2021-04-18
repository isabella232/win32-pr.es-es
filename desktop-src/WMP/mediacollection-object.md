---
title: Objeto MediaCollection
description: El objeto MediaCollection proporciona una manera de organizar una colección grande de elementos multimedia. Se puede consultar para que genere listas de reproducción automáticamente.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objeto MediaCollection Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685650"
---
# <a name="mediacollection-object"></a><span data-ttu-id="30a30-105">Objeto MediaCollection</span><span class="sxs-lookup"><span data-stu-id="30a30-105">MediaCollection Object</span></span>

<span data-ttu-id="30a30-106">El objeto **MediaCollection** proporciona una manera de organizar una colección grande de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="30a30-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="30a30-107">Se puede consultar para que genere listas de reproducción automáticamente.</span><span class="sxs-lookup"><span data-stu-id="30a30-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="30a30-108">El objeto **MediaCollection** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="30a30-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="30a30-109">Método</span><span class="sxs-lookup"><span data-stu-id="30a30-109">Method</span></span>                                                                           | <span data-ttu-id="30a30-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="30a30-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30a30-111">add</span><span class="sxs-lookup"><span data-stu-id="30a30-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="30a30-112">Agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="30a30-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="30a30-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="30a30-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="30a30-114">Crea un nuevo objeto de [consulta](query-object.md) .</span><span class="sxs-lookup"><span data-stu-id="30a30-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="30a30-115">getAll</span><span class="sxs-lookup"><span data-stu-id="30a30-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="30a30-116">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="30a30-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="30a30-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="30a30-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="30a30-118">Recupera un objeto [StringCollection](stringcollection-object.md) que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="30a30-119">getByAlbum</span><span class="sxs-lookup"><span data-stu-id="30a30-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="30a30-120">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia del álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="30a30-121">getByAttribute</span><span class="sxs-lookup"><span data-stu-id="30a30-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="30a30-122">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el atributo especificado que tiene el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="30a30-123">getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="30a30-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="30a30-124">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene objetos [multimedia](media-object.md) que tienen el atributo y el tipo de medio especificados.</span><span class="sxs-lookup"><span data-stu-id="30a30-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="30a30-125">getByAuthor</span><span class="sxs-lookup"><span data-stu-id="30a30-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="30a30-126">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia por el autor especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="30a30-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="30a30-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="30a30-128">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el género especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="30a30-129">getByName</span><span class="sxs-lookup"><span data-stu-id="30a30-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="30a30-130">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="30a30-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="30a30-131">getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="30a30-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="30a30-132">Recupera el índice en el que una propiedad especificada reside en el conjunto de propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="30a30-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="30a30-133">getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="30a30-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="30a30-134">Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene objetos [multimedia](media-object.md) que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="30a30-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="30a30-135">getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="30a30-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="30a30-136">Recupera un objeto [StringCollection](stringcollection-object.md) que contiene cadenas que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="30a30-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="30a30-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="30a30-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="30a30-138">Recupera un valor que indica si el elemento multimedia especificado está en la carpeta de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="30a30-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="30a30-139">remove</span><span class="sxs-lookup"><span data-stu-id="30a30-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="30a30-140">Quita un elemento de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="30a30-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="30a30-141">setDeleted</span><span class="sxs-lookup"><span data-stu-id="30a30-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="30a30-142">Mueve el elemento multimedia especificado a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="30a30-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="30a30-143">Se tiene acceso al objeto **MediaCollection** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="30a30-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="30a30-144">Object</span><span class="sxs-lookup"><span data-stu-id="30a30-144">Object</span></span>                      | <span data-ttu-id="30a30-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30a30-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="30a30-146">Reproductor</span><span class="sxs-lookup"><span data-stu-id="30a30-146">Player</span></span>](player-object.md) | [<span data-ttu-id="30a30-147">mediaCollection</span><span class="sxs-lookup"><span data-stu-id="30a30-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="30a30-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="30a30-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a30-149">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="30a30-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




