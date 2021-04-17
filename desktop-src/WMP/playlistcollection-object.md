---
title: Objeto PlaylistCollection
description: El objeto PlaylistCollection proporciona una manera de organizar las listas de reproducción.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Objeto PlaylistCollection Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704833"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="f1c3d-104">Objeto PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="f1c3d-104">PlaylistCollection Object</span></span>

<span data-ttu-id="f1c3d-105">El objeto **PlaylistCollection** proporciona una manera de organizar las listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="f1c3d-106">El objeto **PlaylistCollection** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="f1c3d-107">Método</span><span class="sxs-lookup"><span data-stu-id="f1c3d-107">Method</span></span>                                                  | <span data-ttu-id="f1c3d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1c3d-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1c3d-109">getAll</span><span class="sxs-lookup"><span data-stu-id="f1c3d-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="f1c3d-110">Recupera un objeto [PlaylistArray](playlistarray-object.md) que contiene todas las listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="f1c3d-111">getByName</span><span class="sxs-lookup"><span data-stu-id="f1c3d-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="f1c3d-112">Recupera un objeto [PlaylistArray](playlistarray-object.md) que contiene listas de reproducción con el nombre especificado, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="f1c3d-113">importPlaylist</span><span class="sxs-lookup"><span data-stu-id="f1c3d-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="f1c3d-114">Agrega una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="f1c3d-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="f1c3d-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="f1c3d-116">Recupera un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="f1c3d-117">Reproducción</span><span class="sxs-lookup"><span data-stu-id="f1c3d-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="f1c3d-118">Crea una nueva lista de reproducción en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="f1c3d-119">remove</span><span class="sxs-lookup"><span data-stu-id="f1c3d-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="f1c3d-120">Quita una lista de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="f1c3d-121">setDeleted</span><span class="sxs-lookup"><span data-stu-id="f1c3d-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="f1c3d-122">Mueve una lista de reproducción a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="f1c3d-123">Se tiene acceso al objeto **PlaylistCollection** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="f1c3d-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="f1c3d-124">Object</span><span class="sxs-lookup"><span data-stu-id="f1c3d-124">Object</span></span>                      | <span data-ttu-id="f1c3d-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1c3d-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="f1c3d-126">Reproductor</span><span class="sxs-lookup"><span data-stu-id="f1c3d-126">Player</span></span>](player-object.md) | [<span data-ttu-id="f1c3d-127">playlistCollection</span><span class="sxs-lookup"><span data-stu-id="f1c3d-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="f1c3d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1c3d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3d-129">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="f1c3d-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




