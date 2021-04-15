---
title: Interfaz IResultVerb (WdsSharedIDL. h)
description: Expone propiedades de verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Interfaz IResultVerb características del entorno heredado de Windows
- Interfaz IResultVerb características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695968"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="5aad8-105">Interfaz IResultVerb</span><span class="sxs-lookup"><span data-stu-id="5aad8-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="5aad8-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5aad8-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5aad8-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5aad8-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5aad8-108">Expone propiedades de verbo.</span><span class="sxs-lookup"><span data-stu-id="5aad8-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="5aad8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5aad8-109">Members</span></span>

<span data-ttu-id="5aad8-110">La interfaz **IResultVerb** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5aad8-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5aad8-111">**IResultVerb** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5aad8-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="5aad8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aad8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5aad8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aad8-113">Properties</span></span>

<span data-ttu-id="5aad8-114">La interfaz **IResultVerb** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5aad8-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="5aad8-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5aad8-115">Property</span></span>                                                             | <span data-ttu-id="5aad8-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5aad8-116">Access type</span></span>           | <span data-ttu-id="5aad8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aad8-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5aad8-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="5aad8-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="5aad8-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aad8-119">Read-only</span></span><br/>  | <span data-ttu-id="5aad8-120">Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo.</span><span class="sxs-lookup"><span data-stu-id="5aad8-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="5aad8-121">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="5aad8-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="5aad8-122">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="5aad8-122">Write-only</span></span><br/> | <span data-ttu-id="5aad8-123">Ejecuta el verbo.</span><span class="sxs-lookup"><span data-stu-id="5aad8-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="5aad8-124">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="5aad8-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="5aad8-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aad8-125">Read-only</span></span><br/>  | <span data-ttu-id="5aad8-126">Esta propiedad devuelve TRUE si el verbo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5aad8-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="5aad8-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="5aad8-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="5aad8-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aad8-128">Read-only</span></span><br/>  | <span data-ttu-id="5aad8-129">Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo.</span><span class="sxs-lookup"><span data-stu-id="5aad8-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="5aad8-130">**Icono**</span><span class="sxs-lookup"><span data-stu-id="5aad8-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="5aad8-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aad8-131">Read-only</span></span><br/>  | <span data-ttu-id="5aad8-132">Esta propiedad devuelve un puntero al identificador del icono opcional asociado al verbo.</span><span class="sxs-lookup"><span data-stu-id="5aad8-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="5aad8-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="5aad8-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="5aad8-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aad8-134">Read-only</span></span><br/>  | <span data-ttu-id="5aad8-135">Esta propiedad devuelve un puntero al nombre de cononical para el verbo, como imprimir, abrir, etc.</span><span class="sxs-lookup"><span data-stu-id="5aad8-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5aad8-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aad8-136">Remarks</span></span>

<span data-ttu-id="5aad8-137">Estos métodos exponen propiedades y acciones aplicables a los verbos.</span><span class="sxs-lookup"><span data-stu-id="5aad8-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aad8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aad8-138">Requirements</span></span>



| <span data-ttu-id="5aad8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aad8-139">Requirement</span></span> | <span data-ttu-id="5aad8-140">Value</span><span class="sxs-lookup"><span data-stu-id="5aad8-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aad8-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aad8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5aad8-142">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5aad8-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5aad8-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aad8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5aad8-144">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="5aad8-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5aad8-145">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5aad8-145">Redistributable</span></span><br/>          | <span data-ttu-id="5aad8-146">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="5aad8-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="5aad8-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aad8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aad8-148"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aad8-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

