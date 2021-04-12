---
description: Collection (clase)
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360719"
---
# <a name="collection-object"></a><span data-ttu-id="1a9ed-103">Collection (objeto)</span><span class="sxs-lookup"><span data-stu-id="1a9ed-103">Collection object</span></span>

<span data-ttu-id="1a9ed-104">Collection (clase)</span><span class="sxs-lookup"><span data-stu-id="1a9ed-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="1a9ed-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a9ed-105">Members</span></span>

<span data-ttu-id="1a9ed-106">El objeto de **colección** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a9ed-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="1a9ed-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a9ed-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a9ed-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a9ed-108">Properties</span></span>

<span data-ttu-id="1a9ed-109">El objeto de **colección** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="1a9ed-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a9ed-110">Property</span></span>                                           | <span data-ttu-id="1a9ed-111">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1a9ed-111">Access type</span></span>          | <span data-ttu-id="1a9ed-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a9ed-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="1a9ed-113">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="1a9ed-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="1a9ed-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a9ed-114">Read-only</span></span><br/> | <span data-ttu-id="1a9ed-115">Devuelve el número de miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="1a9ed-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a9ed-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="1a9ed-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a9ed-117">Read-only</span></span><br/> | <span data-ttu-id="1a9ed-118">Devuelve el elemento especificado en la colección.</span><span class="sxs-lookup"><span data-stu-id="1a9ed-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1a9ed-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a9ed-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="1a9ed-120">Funciones de acceso de creación \\</span><span class="sxs-lookup"><span data-stu-id="1a9ed-120">Creation\\Access Functions</span></span>

<span data-ttu-id="1a9ed-121">Use cualquiera de las siguientes opciones para recuperar una referencia al objeto:</span><span class="sxs-lookup"><span data-stu-id="1a9ed-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="1a9ed-122">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="1a9ed-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="1a9ed-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="1a9ed-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="1a9ed-124">**Dispositivos**</span><span class="sxs-lookup"><span data-stu-id="1a9ed-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="1a9ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a9ed-125">Requirements</span></span>



| <span data-ttu-id="1a9ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a9ed-126">Requirement</span></span> | <span data-ttu-id="1a9ed-127">Value</span><span class="sxs-lookup"><span data-stu-id="1a9ed-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a9ed-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a9ed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a9ed-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1a9ed-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a9ed-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a9ed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a9ed-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a9ed-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1a9ed-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a9ed-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a9ed-133"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1a9ed-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




