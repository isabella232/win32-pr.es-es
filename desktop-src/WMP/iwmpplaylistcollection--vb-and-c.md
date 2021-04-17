---
title: Interfaz IWMPPlaylistCollection (VB y C) (WMP. h)
description: Proporciona métodos para manipular interfaces IWMPPlaylist y IWMPPlaylistArray en una colección.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB y C) interfaz de Windows Media Player
- IWMPPlaylistCollection (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698676"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="5c967-105">Interfaz IWMPPlaylistCollection (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="5c967-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="5c967-106">Proporciona métodos para manipular interfaces **IWMPPlaylist** y **IWMPPlaylistArray** en una colección.</span><span class="sxs-lookup"><span data-stu-id="5c967-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="5c967-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c967-107">Members</span></span>

<span data-ttu-id="5c967-108">La interfaz **IWMPPlaylistCollection (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c967-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="5c967-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c967-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c967-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c967-110">Methods</span></span>

<span data-ttu-id="5c967-111">La interfaz **IWMPPlaylistCollection (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5c967-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="5c967-112">Método</span><span class="sxs-lookup"><span data-stu-id="5c967-112">Method</span></span>                                                                                                 | <span data-ttu-id="5c967-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c967-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c967-114">**getAll**</span><span class="sxs-lookup"><span data-stu-id="5c967-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="5c967-115">Devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a todas las listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c967-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="5c967-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="5c967-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="5c967-117">Devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="5c967-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="5c967-118">**importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="5c967-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="5c967-119">Agrega una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c967-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="5c967-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="5c967-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="5c967-121">Devuelve un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="5c967-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="5c967-122">**Reproducción**</span><span class="sxs-lookup"><span data-stu-id="5c967-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="5c967-123">Devuelve una interfaz **IWMPPlaylist** para una nueva lista de reproducción vacía en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c967-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="5c967-124">**retirar**</span><span class="sxs-lookup"><span data-stu-id="5c967-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="5c967-125">Quita una lista de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c967-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="5c967-126">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="5c967-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="5c967-127">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="5c967-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="5c967-128">Obtenga una interfaz **IWMPPlaylistCollection** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c967-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="5c967-129">Object</span><span class="sxs-lookup"><span data-stu-id="5c967-129">Object</span></span>                                                                   | <span data-ttu-id="5c967-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c967-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c967-131">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="5c967-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="5c967-132">**playlistCollection**</span><span class="sxs-lookup"><span data-stu-id="5c967-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="5c967-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c967-133">Requirements</span></span>



| <span data-ttu-id="5c967-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c967-134">Requirement</span></span> | <span data-ttu-id="5c967-135">Value</span><span class="sxs-lookup"><span data-stu-id="5c967-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5c967-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c967-136">Header</span></span><br/> | <dl> <span data-ttu-id="5c967-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c967-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c967-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c967-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c967-139">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="5c967-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c967-140">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5c967-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c967-141">**Interfaz IWMPPlaylistArray (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5c967-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





