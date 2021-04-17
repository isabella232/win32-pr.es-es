---
title: Interfaz IResultProperty (WdsSharedIDL. h)
description: Expone las propiedades de los resultados.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Interfaz IResultProperty características del entorno heredado de Windows
- Interfaz IResultProperty características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695972"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="e437a-105">Interfaz IResultProperty</span><span class="sxs-lookup"><span data-stu-id="e437a-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="e437a-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e437a-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e437a-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e437a-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e437a-108">Expone las propiedades de los resultados.</span><span class="sxs-lookup"><span data-stu-id="e437a-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="e437a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e437a-109">Members</span></span>

<span data-ttu-id="e437a-110">La interfaz **IResultProperty** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e437a-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e437a-111">**IResultProperty** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e437a-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="e437a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e437a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e437a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e437a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e437a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e437a-114">Methods</span></span>

<span data-ttu-id="e437a-115">La interfaz **IResultProperty** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e437a-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="e437a-116">Método</span><span class="sxs-lookup"><span data-stu-id="e437a-116">Method</span></span>                                                    | <span data-ttu-id="e437a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e437a-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="e437a-118">**Goback**</span><span class="sxs-lookup"><span data-stu-id="e437a-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="e437a-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="e437a-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="e437a-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="e437a-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="e437a-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="e437a-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e437a-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e437a-122">Properties</span></span>

<span data-ttu-id="e437a-123">La interfaz **IResultProperty** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e437a-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="e437a-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e437a-124">Property</span></span>                                                                   | <span data-ttu-id="e437a-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="e437a-125">Access type</span></span>          | <span data-ttu-id="e437a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e437a-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="e437a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e437a-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="e437a-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-128">Read-only</span></span><br/> | <span data-ttu-id="e437a-129">Un tipo de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e437a-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="e437a-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="e437a-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="e437a-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-131">Read-only</span></span><br/> | <span data-ttu-id="e437a-132">Nombre para mostrar localizado de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e437a-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="e437a-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="e437a-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="e437a-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-134">Read-only</span></span><br/> | <span data-ttu-id="e437a-135">Visability de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e437a-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="e437a-136">**Diversas**</span><span class="sxs-lookup"><span data-stu-id="e437a-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="e437a-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-137">Read-only</span></span><br/> | <span data-ttu-id="e437a-138">Valor especial que se usa para ayudar a la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="e437a-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="e437a-139">**IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="e437a-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="e437a-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-140">Read-only</span></span><br/> | <span data-ttu-id="e437a-141">Nombre de la columna de propiedades en el índice.</span><span class="sxs-lookup"><span data-stu-id="e437a-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="e437a-142">**UID**</span><span class="sxs-lookup"><span data-stu-id="e437a-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="e437a-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e437a-143">Read-only</span></span><br/> | <span data-ttu-id="e437a-144">Identificador único de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e437a-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="e437a-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e437a-145">Remarks</span></span>

<span data-ttu-id="e437a-146">Estas son las propiedades de los elementos devueltos.</span><span class="sxs-lookup"><span data-stu-id="e437a-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="e437a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e437a-147">Requirements</span></span>



| <span data-ttu-id="e437a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e437a-148">Requirement</span></span> | <span data-ttu-id="e437a-149">Value</span><span class="sxs-lookup"><span data-stu-id="e437a-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e437a-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e437a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e437a-151">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e437a-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e437a-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e437a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e437a-153">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="e437a-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e437a-154">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e437a-154">Redistributable</span></span><br/>          | <span data-ttu-id="e437a-155">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e437a-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="e437a-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e437a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e437a-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e437a-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

