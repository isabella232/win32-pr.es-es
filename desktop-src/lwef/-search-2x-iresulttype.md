---
title: Interfaz IResultType (WdsSharedIDL. h)
description: Expone información de tipo de propiedad.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Interfaz IResultType características del entorno heredado de Windows
- Interfaz IResultType características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490019"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="0f250-105">Interfaz IResultType</span><span class="sxs-lookup"><span data-stu-id="0f250-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="0f250-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0f250-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0f250-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0f250-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0f250-108">Expone información de tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0f250-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="0f250-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f250-109">Members</span></span>

<span data-ttu-id="0f250-110">La interfaz **IResultType** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0f250-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0f250-111">**IResultType** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0f250-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="0f250-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f250-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f250-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f250-113">Properties</span></span>

<span data-ttu-id="0f250-114">La interfaz **IResultType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0f250-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="0f250-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0f250-115">Property</span></span>                                                                 | <span data-ttu-id="0f250-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0f250-116">Access type</span></span>           | <span data-ttu-id="0f250-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f250-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f250-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0f250-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="0f250-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f250-119">Read-only</span></span><br/>  | <span data-ttu-id="0f250-120">Nombre para mostrar localizado del tipo:</span><span class="sxs-lookup"><span data-stu-id="0f250-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="0f250-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="0f250-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="0f250-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0f250-122">Read/write</span></span><br/> | <span data-ttu-id="0f250-123">Esta propiedad contiene información de propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="0f250-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="0f250-124">**PreceivedType**</span><span class="sxs-lookup"><span data-stu-id="0f250-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="0f250-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f250-125">Read-only</span></span><br/>  | <span data-ttu-id="0f250-126">Esta propiedad contiene la cadena que se usa para identificar el tipo en el índice.</span><span class="sxs-lookup"><span data-stu-id="0f250-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="0f250-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="0f250-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="0f250-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f250-128">Read-only</span></span><br/>  | <span data-ttu-id="0f250-129">Esta propiedad contiene el número de propiedades expuestas por el tipo.</span><span class="sxs-lookup"><span data-stu-id="0f250-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="0f250-130">**UID**</span><span class="sxs-lookup"><span data-stu-id="0f250-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="0f250-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f250-131">Read-only</span></span><br/>  | <span data-ttu-id="0f250-132">Esta propiedad contiene el identificador único para el tipo.</span><span class="sxs-lookup"><span data-stu-id="0f250-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="0f250-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f250-133">Remarks</span></span>

<span data-ttu-id="0f250-134">Estos métodos exponen los tipos de información devueltos.</span><span class="sxs-lookup"><span data-stu-id="0f250-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f250-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f250-135">Requirements</span></span>



| <span data-ttu-id="0f250-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f250-136">Requirement</span></span> | <span data-ttu-id="0f250-137">Value</span><span class="sxs-lookup"><span data-stu-id="0f250-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f250-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f250-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0f250-139">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f250-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0f250-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f250-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0f250-141">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="0f250-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f250-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0f250-142">Redistributable</span></span><br/>          | <span data-ttu-id="0f250-143">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0f250-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="0f250-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f250-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f250-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f250-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

