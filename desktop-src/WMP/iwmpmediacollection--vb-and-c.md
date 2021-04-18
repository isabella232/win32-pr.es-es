---
title: Interfaz IWMPMediaCollection (VB y C) (WMP. h)
description: Proporciona métodos que se pueden utilizar para organizar una colección grande de elementos multimedia.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection (VB y C) interfaz de Windows Media Player
- IWMPMediaCollection (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691086"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="cd466-105">Interfaz IWMPMediaCollection (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="cd466-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="cd466-106">Proporciona métodos que se pueden utilizar para organizar una colección grande de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="cd466-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="cd466-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd466-107">Members</span></span>

<span data-ttu-id="cd466-108">La interfaz **IWMPMediaCollection (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd466-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="cd466-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd466-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd466-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd466-110">Methods</span></span>

<span data-ttu-id="cd466-111">La interfaz **IWMPMediaCollection (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cd466-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="cd466-112">Método</span><span class="sxs-lookup"><span data-stu-id="cd466-112">Method</span></span>                                                                                                                       | <span data-ttu-id="cd466-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd466-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd466-114">**add**</span><span class="sxs-lookup"><span data-stu-id="cd466-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="cd466-115">Agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cd466-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="cd466-116">**getAll**</span><span class="sxs-lookup"><span data-stu-id="cd466-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="cd466-117">Devuelve una interfaz **IWMPPlaylist** que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cd466-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="cd466-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="cd466-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="cd466-119">Devuelve una interfaz **IWMPStringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="cd466-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="cd466-120">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="cd466-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="cd466-121">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="cd466-122">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="cd466-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="cd466-123">Devuelve una interfaz **IWMPPlaylist** que corresponde al atributo especificado que tiene el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="cd466-124">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="cd466-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="cd466-125">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia por el autor especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="cd466-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="cd466-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="cd466-127">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del género especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="cd466-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="cd466-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="cd466-129">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="cd466-130">**getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="cd466-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="cd466-131">Devuelve el índice de un atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="cd466-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="cd466-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="cd466-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="cd466-133">Ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="cd466-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="cd466-134">**retirar**</span><span class="sxs-lookup"><span data-stu-id="cd466-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="cd466-135">Quita el elemento multimedia especificado de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="cd466-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="cd466-136">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="cd466-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="cd466-137">Mueve el elemento multimedia especificado a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="cd466-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="cd466-138">Obtenga una interfaz **IWMPMediaCollection** con las siguientes propiedades a las que se tiene acceso a través del objeto o la interfaz siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd466-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="cd466-139">Objeto o interfaz</span><span class="sxs-lookup"><span data-stu-id="cd466-139">Object or interface</span></span>                                               | <span data-ttu-id="cd466-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd466-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd466-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cd466-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="cd466-142">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="cd466-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="cd466-143">**IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="cd466-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="cd466-144">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="cd466-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="cd466-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd466-145">Requirements</span></span>



| <span data-ttu-id="cd466-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd466-146">Requirement</span></span> | <span data-ttu-id="cd466-147">Value</span><span class="sxs-lookup"><span data-stu-id="cd466-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd466-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd466-148">Header</span></span><br/> | <dl> <span data-ttu-id="cd466-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd466-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd466-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd466-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd466-151">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="cd466-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="cd466-152">**Interfaz IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="cd466-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cd466-153">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cd466-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cd466-154">**Interfaz IWMPStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cd466-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





