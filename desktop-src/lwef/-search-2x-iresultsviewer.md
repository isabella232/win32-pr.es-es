---
title: Interfaz IResultsViewer (WdsSharedIDL. h)
description: Expone métodos y propiedades para la vista de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Interfaz IResultsViewer características del entorno heredado de Windows
- Interfaz IResultsViewer características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534510"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="156ff-105">Interfaz IResultsViewer</span><span class="sxs-lookup"><span data-stu-id="156ff-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="156ff-106">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="156ff-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="156ff-107">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="156ff-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="156ff-108">Expone métodos y propiedades para la vista de resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="156ff-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="156ff-109">Members</span></span>

<span data-ttu-id="156ff-110">La interfaz **IResultsViewer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="156ff-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="156ff-111">**IResultsViewer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="156ff-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="156ff-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="156ff-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="156ff-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="156ff-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="156ff-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="156ff-114">Methods</span></span>

<span data-ttu-id="156ff-115">La interfaz **IResultsViewer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="156ff-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="156ff-116">Método</span><span class="sxs-lookup"><span data-stu-id="156ff-116">Method</span></span>                                                   | <span data-ttu-id="156ff-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="156ff-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="156ff-118">**Goback**</span><span class="sxs-lookup"><span data-stu-id="156ff-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="156ff-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="156ff-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="156ff-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="156ff-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="156ff-122">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="156ff-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="156ff-123">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="156ff-124">**Stop**</span><span class="sxs-lookup"><span data-stu-id="156ff-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="156ff-125">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="156ff-126">**Update**</span><span class="sxs-lookup"><span data-stu-id="156ff-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="156ff-127">Aplica cualquier cambio en la consulta y navega por la vista al nuevo conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="156ff-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="156ff-128">Properties</span></span>

<span data-ttu-id="156ff-129">La interfaz **IResultsViewer** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="156ff-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="156ff-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="156ff-130">Property</span></span>                                                                            | <span data-ttu-id="156ff-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="156ff-131">Access type</span></span>           | <span data-ttu-id="156ff-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="156ff-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="156ff-133">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="156ff-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="156ff-134">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-134">Write-only</span></span><br/> | <span data-ttu-id="156ff-135">Esta propiedad realiza un seguimiento del tipo de contenido que se muestra en la vista de resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="156ff-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="156ff-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="156ff-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="156ff-137">Read-only</span></span><br/>  | <span data-ttu-id="156ff-138">Nombre para mostrar localizado del tipo.</span><span class="sxs-lookup"><span data-stu-id="156ff-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="156ff-139">**EnumSelectedItems**</span><span class="sxs-lookup"><span data-stu-id="156ff-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="156ff-140">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-140">Write-only</span></span><br/> | <span data-ttu-id="156ff-141">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="156ff-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="156ff-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="156ff-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-143">Read/write</span></span><br/> | <span data-ttu-id="156ff-144">Esta propiedad establece o devuelve el nombre del tipo preceived por el que se van a filtrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="156ff-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="156ff-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="156ff-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-146">Read/write</span></span><br/> | <span data-ttu-id="156ff-147">Estilo del encabezado que se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="156ff-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="156ff-148">**IsUpdateNeeded**</span><span class="sxs-lookup"><span data-stu-id="156ff-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="156ff-149">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-149">Write-only</span></span><br/> | <span data-ttu-id="156ff-150">Esto devuelve TRUE si se ha modificado la consulta views y necesita actualizarse.</span><span class="sxs-lookup"><span data-stu-id="156ff-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="156ff-151">**ItemStore**</span><span class="sxs-lookup"><span data-stu-id="156ff-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="156ff-152">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-152">Read/write</span></span><br/> | <span data-ttu-id="156ff-153">Esta propiedad establece o devuelve el nombre del almacén en el que se van a filtrar los resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="156ff-154">**PreviewStyle**</span><span class="sxs-lookup"><span data-stu-id="156ff-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="156ff-155">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-155">Read/write</span></span><br/> | <span data-ttu-id="156ff-156">Controla el modo de presentación del panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="156ff-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="156ff-157">**PropertyFilters**</span><span class="sxs-lookup"><span data-stu-id="156ff-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="156ff-158">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-158">Write-only</span></span><br/> | <span data-ttu-id="156ff-159">Al llamar a la colección de filtros de propiedades, devolverá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="156ff-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="156ff-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="156ff-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="156ff-161">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-161">Read/write</span></span><br/> | <span data-ttu-id="156ff-162">Obtiene o establece el texto de la consulta actual.</span><span class="sxs-lookup"><span data-stu-id="156ff-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="156ff-163">**ResultsStyle**</span><span class="sxs-lookup"><span data-stu-id="156ff-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="156ff-164">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-164">Write-only</span></span><br/> | <span data-ttu-id="156ff-165">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="156ff-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="156ff-166">**SortOrderProperty**</span><span class="sxs-lookup"><span data-stu-id="156ff-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="156ff-167">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-167">Read/write</span></span><br/> | <span data-ttu-id="156ff-168">Esta propiedad establece o devuelve el orden de las columnas por las que se van a ordenar los resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="156ff-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="156ff-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="156ff-170">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="156ff-170">Read/write</span></span><br/> | <span data-ttu-id="156ff-171">Esta propiedad establece o devuelve el IndexColumn de la propiedad por la que se van a ordenar los resultados.</span><span class="sxs-lookup"><span data-stu-id="156ff-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="156ff-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="156ff-172">Remarks</span></span>

<span data-ttu-id="156ff-173">Estos métodos y propiedades se usan para manipular la información que se ve.</span><span class="sxs-lookup"><span data-stu-id="156ff-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="156ff-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="156ff-174">Requirements</span></span>



| <span data-ttu-id="156ff-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="156ff-175">Requirement</span></span> | <span data-ttu-id="156ff-176">Value</span><span class="sxs-lookup"><span data-stu-id="156ff-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="156ff-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="156ff-177">Minimum supported client</span></span><br/> | <span data-ttu-id="156ff-178">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="156ff-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="156ff-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="156ff-179">Minimum supported server</span></span><br/> | <span data-ttu-id="156ff-180">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="156ff-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="156ff-181">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="156ff-181">Redistributable</span></span><br/>          | <span data-ttu-id="156ff-182">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="156ff-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="156ff-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="156ff-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="156ff-184"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="156ff-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

