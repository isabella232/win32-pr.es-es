---
title: Interfaz IWMPMedia2 (VB y C) (WMP. h)
description: Proporciona acceso a una propiedad de elemento multimedia adicional.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB y C) interfaz de Windows Media Player
- IWMPMedia2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689983"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="361b8-105">Interfaz IWMPMedia2 (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="361b8-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="361b8-106">Proporciona acceso a una propiedad de elemento multimedia adicional.</span><span class="sxs-lookup"><span data-stu-id="361b8-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="361b8-107">Además de las propiedades y los métodos heredados de **IWMPMedia**, la interfaz **IWMPMedia2** expone la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="361b8-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="361b8-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="361b8-108">Property</span></span>                                                 | <span data-ttu-id="361b8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="361b8-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="361b8-110">Error</span><span class="sxs-lookup"><span data-stu-id="361b8-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="361b8-111">Obtiene una interfaz **IWMPErrorItem** si el elemento multimedia tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="361b8-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="361b8-112">Obtenga una interfaz **IWMPMedia2** convirtiendo el valor devuelto por una de las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.</span><span class="sxs-lookup"><span data-stu-id="361b8-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="361b8-113">Objeto o interfaz</span><span class="sxs-lookup"><span data-stu-id="361b8-113">Object or interface</span></span>                                               | <span data-ttu-id="361b8-114">Propiedad o método</span><span class="sxs-lookup"><span data-stu-id="361b8-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="361b8-115">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="361b8-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="361b8-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="361b8-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="361b8-117">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="361b8-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="361b8-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="361b8-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="361b8-119">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="361b8-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="361b8-120">[Elemento](iwmpplaylist-item--vb-and-c.md) ( **obtener \_ elemento** en C#)</span><span class="sxs-lookup"><span data-stu-id="361b8-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="361b8-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="361b8-121">Members</span></span>

<span data-ttu-id="361b8-122">La interfaz **IWMPMedia2 (VB y C#)** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="361b8-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="361b8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="361b8-123">Requirements</span></span>



| <span data-ttu-id="361b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="361b8-124">Requirement</span></span> | <span data-ttu-id="361b8-125">Value</span><span class="sxs-lookup"><span data-stu-id="361b8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="361b8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="361b8-126">Header</span></span><br/> | <dl> <span data-ttu-id="361b8-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="361b8-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="361b8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="361b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361b8-129">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="361b8-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="361b8-130">**IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="361b8-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="361b8-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="361b8-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="361b8-132">**Interfaz IWMPMedia3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="361b8-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





