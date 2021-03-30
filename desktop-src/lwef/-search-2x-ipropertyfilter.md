---
title: Interfaz IPropertyFilter (WdsSharedIDL. h)
description: Expone propiedades utilizadas para filtrar la consulta.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Interfaz IPropertyFilter características del entorno heredado de Windows
- Interfaz IPropertyFilter características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534696"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="a87bd-105">Interfaz IPropertyFilter</span><span class="sxs-lookup"><span data-stu-id="a87bd-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="a87bd-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a87bd-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a87bd-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a87bd-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a87bd-108">Expone propiedades utilizadas para filtrar la consulta.</span><span class="sxs-lookup"><span data-stu-id="a87bd-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="a87bd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a87bd-109">Members</span></span>

<span data-ttu-id="a87bd-110">La interfaz **IPropertyFilter** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a87bd-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a87bd-111">**IPropertyFilter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a87bd-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="a87bd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a87bd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a87bd-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a87bd-113">Properties</span></span>

<span data-ttu-id="a87bd-114">La interfaz **IPropertyFilter** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a87bd-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="a87bd-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a87bd-115">Property</span></span>                                                                                      | <span data-ttu-id="a87bd-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a87bd-116">Access type</span></span>           | <span data-ttu-id="a87bd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a87bd-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="a87bd-118">**IPropertyFilter::IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="a87bd-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="a87bd-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a87bd-119">Read/write</span></span><br/> | <span data-ttu-id="a87bd-120">Nombre de columna indizada de la propiedad por la que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="a87bd-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="a87bd-121">**IPropertyFilter::LogicOperator**</span><span class="sxs-lookup"><span data-stu-id="a87bd-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="a87bd-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a87bd-122">Read/write</span></span><br/> | <span data-ttu-id="a87bd-123">Operador lógico que se va a usar al aplicar el filtro.</span><span class="sxs-lookup"><span data-stu-id="a87bd-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="a87bd-124">**IPropertyFilter::NestingDepth**</span><span class="sxs-lookup"><span data-stu-id="a87bd-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="a87bd-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a87bd-125">Read/write</span></span><br/> | <span data-ttu-id="a87bd-126">Filtra la profundidad dentro de un conjunto anidado de paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a87bd-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="a87bd-127">**IPropertyFilter:: Text**</span><span class="sxs-lookup"><span data-stu-id="a87bd-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="a87bd-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a87bd-128">Read/write</span></span><br/> | <span data-ttu-id="a87bd-129">Texto del filtro.</span><span class="sxs-lookup"><span data-stu-id="a87bd-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="a87bd-130">**IPropertyFilter:: UID**</span><span class="sxs-lookup"><span data-stu-id="a87bd-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="a87bd-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a87bd-131">Read/write</span></span><br/> | <span data-ttu-id="a87bd-132">UID de la propiedad por la que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="a87bd-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="a87bd-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a87bd-133">Remarks</span></span>

<span data-ttu-id="a87bd-134">Estas propiedades se usan para filtrar la consulta.</span><span class="sxs-lookup"><span data-stu-id="a87bd-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87bd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a87bd-135">Requirements</span></span>



| <span data-ttu-id="a87bd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a87bd-136">Requirement</span></span> | <span data-ttu-id="a87bd-137">Value</span><span class="sxs-lookup"><span data-stu-id="a87bd-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a87bd-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a87bd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a87bd-139">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a87bd-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a87bd-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a87bd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a87bd-141">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="a87bd-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a87bd-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a87bd-142">Redistributable</span></span><br/>          | <span data-ttu-id="a87bd-143">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a87bd-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="a87bd-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a87bd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a87bd-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a87bd-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

