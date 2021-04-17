---
title: Interfaz IWMPCdrom (VB y C) (WMP. h)
description: Proporciona una manera de tener acceso a un CD o DVD en su unidad. La interfaz IWMPCdrom expone las siguientes propiedades.
ms.assetid: 2748e64b-b9b7-489a-a6b5-21154aabd312
keywords:
- IWMPCdrom (VB y C) interfaz de Windows Media Player
- IWMPCdrom (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPCdrom (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036411c96b278023d87c37ad48f81e986b9dadcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690433"
---
# <a name="iwmpcdrom-vb-and-c-interface"></a><span data-ttu-id="ff794-105">Interfaz IWMPCdrom (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="ff794-105">IWMPCdrom (VB and C#) interface</span></span>

<span data-ttu-id="ff794-106">Proporciona una manera de tener acceso a un CD o DVD en su unidad.</span><span class="sxs-lookup"><span data-stu-id="ff794-106">Provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="ff794-107">La interfaz **IWMPCdrom** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff794-107">The **IWMPCdrom** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="ff794-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff794-108">Members</span></span>

<span data-ttu-id="ff794-109">La interfaz **IWMPCdrom (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ff794-109">The **IWMPCdrom (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="ff794-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff794-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ff794-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff794-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ff794-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff794-112">Methods</span></span>

<span data-ttu-id="ff794-113">La interfaz **IWMPCdrom (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ff794-113">The **IWMPCdrom (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="ff794-114">Método</span><span class="sxs-lookup"><span data-stu-id="ff794-114">Method</span></span>                                                     | <span data-ttu-id="ff794-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff794-115">Description</span></span>                                     |
|:-----------------------------------------------------------|:------------------------------------------------|
| [<span data-ttu-id="ff794-116">**expulsar**</span><span class="sxs-lookup"><span data-stu-id="ff794-116">**eject**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md) | <span data-ttu-id="ff794-117">Expulsa el CD o DVD de la unidad.</span><span class="sxs-lookup"><span data-stu-id="ff794-117">Ejects the CD or DVD from the drive.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ff794-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff794-118">Properties</span></span>

<span data-ttu-id="ff794-119">La interfaz **IWMPCdrom (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff794-119">The **IWMPCdrom (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="ff794-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff794-120">Property</span></span>                                                                                | <span data-ttu-id="ff794-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ff794-121">Access type</span></span>          | <span data-ttu-id="ff794-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff794-122">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff794-123">**driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="ff794-123">**driveSpecifier**</span></span>](wmplibiwmpcdrom-iwmpcdrom-drivespecifier--vb-and-c.md)<br/> | <span data-ttu-id="ff794-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff794-124">Read-only</span></span><br/> | <span data-ttu-id="ff794-125">Obtiene la letra de unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="ff794-125">Gets the CD or DVD drive letter.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="ff794-126">**Lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="ff794-126">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)<br/>             | <span data-ttu-id="ff794-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff794-127">Read-only</span></span><br/> | <span data-ttu-id="ff794-128">Obtiene una interfaz [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) que representa las pistas de un CD o las entradas de título de nivel de raíz de un DVD.</span><span class="sxs-lookup"><span data-stu-id="ff794-128">Gets an [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) interface representing the tracks on a CD or the root-level title entries for a DVD.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ff794-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff794-129">Requirements</span></span>



| <span data-ttu-id="ff794-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff794-130">Requirement</span></span> | <span data-ttu-id="ff794-131">Value</span><span class="sxs-lookup"><span data-stu-id="ff794-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ff794-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff794-132">Header</span></span><br/> | <dl> <span data-ttu-id="ff794-133"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff794-133"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff794-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff794-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff794-135">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="ff794-135">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="ff794-136">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ff794-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





