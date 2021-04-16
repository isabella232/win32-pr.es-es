---
title: Interfaz IWMPMediaCollection2 (VB y C) (WMP. h)
description: Proporciona métodos que complementan la interfaz IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB y C) interfaz de Windows Media Player
- IWMPMediaCollection2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690524"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="36b7b-105">Interfaz IWMPMediaCollection2 (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="36b7b-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="36b7b-106">Proporciona métodos que complementan la interfaz **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="36b7b-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="36b7b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="36b7b-107">Members</span></span>

<span data-ttu-id="36b7b-108">La interfaz **IWMPMediaCollection2 (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36b7b-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="36b7b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="36b7b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36b7b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="36b7b-110">Methods</span></span>

<span data-ttu-id="36b7b-111">La interfaz **IWMPMediaCollection2 (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="36b7b-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="36b7b-112">Método</span><span class="sxs-lookup"><span data-stu-id="36b7b-112">Method</span></span>                                                                                                                     | <span data-ttu-id="36b7b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="36b7b-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36b7b-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="36b7b-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="36b7b-115">Devuelve una interfaz **IWMPQuery** que representa una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="36b7b-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="36b7b-116">**getByAttributeAndMediaType**</span><span class="sxs-lookup"><span data-stu-id="36b7b-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="36b7b-117">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.</span><span class="sxs-lookup"><span data-stu-id="36b7b-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="36b7b-118">**getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="36b7b-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="36b7b-119">Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="36b7b-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="36b7b-120">**getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="36b7b-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="36b7b-121">Devuelve una interfaz **IWMPStringCollection** que proporciona acceso al conjunto de todos los valores de cadena para un atributo especificado que coinciden con las condiciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="36b7b-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="36b7b-122">Obtenga una interfaz **IWMPMediaCollection2** convirtiendo el valor devuelto por la propiedad [**AxWindowsMediaPlayer. mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) o el valor devuelto por la propiedad [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="36b7b-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b7b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b7b-123">Requirements</span></span>



| <span data-ttu-id="36b7b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b7b-124">Requirement</span></span> | <span data-ttu-id="36b7b-125">Value</span><span class="sxs-lookup"><span data-stu-id="36b7b-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36b7b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36b7b-126">Header</span></span><br/> | <dl> <span data-ttu-id="36b7b-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="36b7b-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b7b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="36b7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b7b-129">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="36b7b-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="36b7b-130">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="36b7b-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





