---
title: Interfaz IPropertyFilterCollection (WdsSharedIDL. h)
description: Expone las propiedades de la colección devuelta basándose en la consulta enviada.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows
- Interfaz IPropertyFilterCollection características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359769"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="edac0-105">Interfaz IPropertyFilterCollection</span><span class="sxs-lookup"><span data-stu-id="edac0-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="edac0-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="edac0-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="edac0-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="edac0-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="edac0-108">Expone las propiedades de la colección devuelta basándose en la consulta enviada.</span><span class="sxs-lookup"><span data-stu-id="edac0-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="edac0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="edac0-109">Members</span></span>

<span data-ttu-id="edac0-110">La interfaz **IPropertyFilterCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="edac0-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="edac0-111">**IPropertyFilterCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="edac0-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="edac0-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="edac0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="edac0-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="edac0-113">Properties</span></span>

<span data-ttu-id="edac0-114">La interfaz **IPropertyFilterCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="edac0-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="edac0-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="edac0-115">Property</span></span>                                                                         | <span data-ttu-id="edac0-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="edac0-116">Access type</span></span>           | <span data-ttu-id="edac0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="edac0-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="edac0-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="edac0-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="edac0-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="edac0-119">Read-only</span></span><br/>  | <span data-ttu-id="edac0-120">Agrega un nuevo filtro a la colección.</span><span class="sxs-lookup"><span data-stu-id="edac0-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="edac0-121">**claridad**</span><span class="sxs-lookup"><span data-stu-id="edac0-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="edac0-122">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="edac0-122">Write-only</span></span><br/> | <span data-ttu-id="edac0-123">Borra la colección.</span><span class="sxs-lookup"><span data-stu-id="edac0-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="edac0-124">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="edac0-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="edac0-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="edac0-125">Read-only</span></span><br/>  | <span data-ttu-id="edac0-126">Número de filtros de la colección.</span><span class="sxs-lookup"><span data-stu-id="edac0-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="edac0-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="edac0-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="edac0-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="edac0-128">Read/write</span></span><br/> | <span data-ttu-id="edac0-129">Devuelve un filtro específico dentro de la colección.</span><span class="sxs-lookup"><span data-stu-id="edac0-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="edac0-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="edac0-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="edac0-131">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="edac0-131">Write-only</span></span><br/> | <span data-ttu-id="edac0-132">Quita un filtro específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="edac0-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="edac0-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edac0-133">Remarks</span></span>

<span data-ttu-id="edac0-134">Estas propiedades se usan para filtrar la colección devuelta por la consulta.</span><span class="sxs-lookup"><span data-stu-id="edac0-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="edac0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edac0-135">Requirements</span></span>



| <span data-ttu-id="edac0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="edac0-136">Requirement</span></span> | <span data-ttu-id="edac0-137">Value</span><span class="sxs-lookup"><span data-stu-id="edac0-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="edac0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edac0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="edac0-139">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="edac0-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="edac0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edac0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="edac0-141">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="edac0-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="edac0-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="edac0-142">Redistributable</span></span><br/>          | <span data-ttu-id="edac0-143">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="edac0-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="edac0-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edac0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="edac0-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="edac0-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

