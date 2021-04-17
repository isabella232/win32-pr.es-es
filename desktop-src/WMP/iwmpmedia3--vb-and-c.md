---
title: Interfaz IWMPMedia3 (VB y C) (WMP. h)
description: Proporciona métodos adicionales para tener acceso a las propiedades de un elemento multimedia.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- IWMPMedia3 (VB y C) interfaz de Windows Media Player
- IWMPMedia3 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689982"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a><span data-ttu-id="d36be-105">Interfaz IWMPMedia3 (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="d36be-105">IWMPMedia3 (VB and C#) interface</span></span>

<span data-ttu-id="d36be-106">Proporciona métodos adicionales para tener acceso a las propiedades de un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="d36be-106">Provides additional methods to access the properties of a media item.</span></span>

## <a name="members"></a><span data-ttu-id="d36be-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d36be-107">Members</span></span>

<span data-ttu-id="d36be-108">La interfaz **IWMPMedia3 (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d36be-108">The **IWMPMedia3 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="d36be-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d36be-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d36be-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d36be-110">Methods</span></span>

<span data-ttu-id="d36be-111">La interfaz **IWMPMedia3 (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d36be-111">The **IWMPMedia3 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="d36be-112">Método</span><span class="sxs-lookup"><span data-stu-id="d36be-112">Method</span></span>                                                                                           | <span data-ttu-id="d36be-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d36be-113">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d36be-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="d36be-114">**getAttributeCountByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="d36be-115">Devuelve el número de atributos asociados al tipo de atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="d36be-115">Returns the number of attributes associated with the specified attribute type.</span></span><br/>              |
| [<span data-ttu-id="d36be-116">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="d36be-116">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="d36be-117">Devuelve el valor del atributo correspondiente al tipo de atributo y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="d36be-117">Returns the value of the attribute corresponding to the specified attribute type and index.</span></span><br/> |



 

<span data-ttu-id="d36be-118">Obtenga una interfaz **IWMPMedia3** convirtiendo el valor devuelto por una de las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.</span><span class="sxs-lookup"><span data-stu-id="d36be-118">Get an **IWMPMedia3** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="d36be-119">Objeto o interfaz</span><span class="sxs-lookup"><span data-stu-id="d36be-119">Object or interface</span></span>                                               | <span data-ttu-id="d36be-120">Propiedad o método</span><span class="sxs-lookup"><span data-stu-id="d36be-120">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d36be-121">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="d36be-121">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="d36be-122">currentItem</span><span class="sxs-lookup"><span data-stu-id="d36be-122">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="d36be-123">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d36be-123">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="d36be-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="d36be-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="d36be-125">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="d36be-125">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="d36be-126">[Elemento](iwmpplaylist-item--vb-and-c.md) ( **obtener \_ elemento** en C#)</span><span class="sxs-lookup"><span data-stu-id="d36be-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="d36be-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d36be-127">Requirements</span></span>



| <span data-ttu-id="d36be-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d36be-128">Requirement</span></span> | <span data-ttu-id="d36be-129">Value</span><span class="sxs-lookup"><span data-stu-id="d36be-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d36be-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d36be-130">Header</span></span><br/> | <dl> <span data-ttu-id="d36be-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d36be-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d36be-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d36be-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36be-133">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="d36be-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="d36be-134">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d36be-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d36be-135">**Interfaz IWMPMedia2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d36be-135">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





