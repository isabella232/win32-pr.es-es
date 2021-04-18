---
title: Interfaz IWMPCdromCollection (VB y C) (WMP. h)
description: Proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD. La interfaz IWMPCdromCollection expone la propiedad siguiente.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCdromCollection (VB y C) interfaz de Windows Media Player
- IWMPCdromCollection (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690691"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a><span data-ttu-id="c795b-105">Interfaz IWMPCdromCollection (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="c795b-105">IWMPCdromCollection (VB and C#) interface</span></span>

<span data-ttu-id="c795b-106">Proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c795b-106">Provides a way to organize and access a collection of CD or DVD drives.</span></span>

<span data-ttu-id="c795b-107">La interfaz **IWMPCdromCollection** expone la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="c795b-107">The **IWMPCdromCollection** interface exposes the following property.</span></span>

## <a name="members"></a><span data-ttu-id="c795b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c795b-108">Members</span></span>

<span data-ttu-id="c795b-109">La interfaz **IWMPCdromCollection (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c795b-109">The **IWMPCdromCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="c795b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c795b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c795b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c795b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c795b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c795b-112">Methods</span></span>

<span data-ttu-id="c795b-113">La interfaz **IWMPCdromCollection (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c795b-113">The **IWMPCdromCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="c795b-114">Método</span><span class="sxs-lookup"><span data-stu-id="c795b-114">Method</span></span>                                                                                                     | <span data-ttu-id="c795b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c795b-115">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c795b-116">**getByDriveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="c795b-116">**getByDriveSpecifier**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | <span data-ttu-id="c795b-117">Devuelve una interfaz **IWMPCdrom** asociada a una letra de unidad concreta.</span><span class="sxs-lookup"><span data-stu-id="c795b-117">Returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span><br/> |
| [<span data-ttu-id="c795b-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c795b-118">**Item**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | <span data-ttu-id="c795b-119">Devuelve una interfaz **IWMPCdrom** en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c795b-119">Returns an **IWMPCdrom** interface at the given index.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="c795b-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c795b-120">Properties</span></span>

<span data-ttu-id="c795b-121">La interfaz **IWMPCdromCollection (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c795b-121">The **IWMPCdromCollection (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="c795b-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c795b-122">Property</span></span>                                                                                  | <span data-ttu-id="c795b-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c795b-123">Access type</span></span>          | <span data-ttu-id="c795b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c795b-124">Description</span></span>                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="c795b-125">**contabiliza**</span><span class="sxs-lookup"><span data-stu-id="c795b-125">**count**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | <span data-ttu-id="c795b-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c795b-126">Read-only</span></span><br/> | <span data-ttu-id="c795b-127">Obtiene el número de unidades de CD y DVD disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c795b-127">Gets the number of available CD and DVD drives on the system.</span></span><br/> |



 

<span data-ttu-id="c795b-128">Obtenga una interfaz **IWMPCdromCollection** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="c795b-128">Get an **IWMPCdromCollection** interface by using the following property.</span></span>



| <span data-ttu-id="c795b-129">Object</span><span class="sxs-lookup"><span data-stu-id="c795b-129">Object</span></span>                                                                   | <span data-ttu-id="c795b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c795b-130">Property</span></span>                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c795b-131">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c795b-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="c795b-132">**cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="c795b-132">**cdromCollection**</span></span>](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="c795b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c795b-133">Requirements</span></span>



| <span data-ttu-id="c795b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c795b-134">Requirement</span></span> | <span data-ttu-id="c795b-135">Value</span><span class="sxs-lookup"><span data-stu-id="c795b-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c795b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c795b-136">Header</span></span><br/> | <dl> <span data-ttu-id="c795b-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c795b-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c795b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c795b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c795b-139">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="c795b-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="c795b-140">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c795b-140">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





