---
title: Interfaz IWMPMedia (VB y C) (WMP. h)
description: Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia. La interfaz IWMPMedia expone las siguientes propiedades.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB y C) interfaz de Windows Media Player
- IWMPMedia (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690772"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="adc1c-105">Interfaz IWMPMedia (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="adc1c-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="adc1c-106">Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="adc1c-107">La interfaz **IWMPMedia** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="adc1c-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="adc1c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="adc1c-108">Members</span></span>

<span data-ttu-id="adc1c-109">La interfaz **IWMPMedia (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="adc1c-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="adc1c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="adc1c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="adc1c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="adc1c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="adc1c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="adc1c-112">Methods</span></span>

<span data-ttu-id="adc1c-113">La interfaz **IWMPMedia (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="adc1c-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="adc1c-114">Método</span><span class="sxs-lookup"><span data-stu-id="adc1c-114">Method</span></span>                                                                             | <span data-ttu-id="adc1c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="adc1c-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adc1c-116">**getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="adc1c-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="adc1c-117">Devuelve el nombre del atributo correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="adc1c-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="adc1c-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="adc1c-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="adc1c-119">Devuelve el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="adc1c-120">**getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="adc1c-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="adc1c-121">Devuelve el valor del atributo con el número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="adc1c-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="adc1c-122">**getMarkerName**</span><span class="sxs-lookup"><span data-stu-id="adc1c-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="adc1c-123">Devuelve el nombre del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="adc1c-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="adc1c-124">**getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="adc1c-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="adc1c-125">Devuelve la hora del marcador en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="adc1c-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="adc1c-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="adc1c-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="adc1c-127">Devuelve un valor que indica si el elemento multimedia especificado es un miembro de la lista de reproducción especificada.</span><span class="sxs-lookup"><span data-stu-id="adc1c-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="adc1c-128">**isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="adc1c-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="adc1c-129">Devuelve un valor que indica si se pueden editar los atributos del elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="adc1c-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="adc1c-130">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="adc1c-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="adc1c-131">Establece el valor del atributo especificado para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="adc1c-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="adc1c-132">Properties</span></span>

<span data-ttu-id="adc1c-133">La interfaz **IWMPMedia (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="adc1c-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="adc1c-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="adc1c-134">Property</span></span>                                                                                      | <span data-ttu-id="adc1c-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="adc1c-135">Access type</span></span>          | <span data-ttu-id="adc1c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="adc1c-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adc1c-137">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="adc1c-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="adc1c-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-138">Read-only</span></span><br/> | <span data-ttu-id="adc1c-139">Obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="adc1c-140">**Duration**</span><span class="sxs-lookup"><span data-stu-id="adc1c-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="adc1c-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-141">Read-only</span></span><br/> | <span data-ttu-id="adc1c-142">Obtiene la duración en segundos del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="adc1c-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="adc1c-143">**durationString**</span><span class="sxs-lookup"><span data-stu-id="adc1c-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="adc1c-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-144">Read-only</span></span><br/> | <span data-ttu-id="adc1c-145">Obtiene un valor que indica la duración del elemento multimedia actual en formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="adc1c-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="adc1c-146">**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="adc1c-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="adc1c-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-147">Read-only</span></span><br/> | <span data-ttu-id="adc1c-148">Obtiene el alto del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="adc1c-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="adc1c-149">**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="adc1c-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="adc1c-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-150">Read-only</span></span><br/> | <span data-ttu-id="adc1c-151">Obtiene el ancho del elemento multimedia actual en píxeles.</span><span class="sxs-lookup"><span data-stu-id="adc1c-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="adc1c-152">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="adc1c-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="adc1c-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-153">Read-only</span></span><br/> | <span data-ttu-id="adc1c-154">Obtiene un valor que indica si el elemento multimedia especificado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="adc1c-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="adc1c-155">En C#, este es el método **Get \_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="adc1c-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="adc1c-156">**markerCount**</span><span class="sxs-lookup"><span data-stu-id="adc1c-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="adc1c-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-157">Read-only</span></span><br/> | <span data-ttu-id="adc1c-158">Obtiene el número de marcadores del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="adc1c-159">**name**</span><span class="sxs-lookup"><span data-stu-id="adc1c-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="adc1c-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-160">Read-only</span></span><br/> | <span data-ttu-id="adc1c-161">Obtiene o establece el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="adc1c-162">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="adc1c-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="adc1c-163">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="adc1c-163">Read-only</span></span><br/> | <span data-ttu-id="adc1c-164">Obtiene la dirección URL del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="adc1c-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="adc1c-165">Obtenga una interfaz **IWMPMedia** con las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.</span><span class="sxs-lookup"><span data-stu-id="adc1c-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="adc1c-166">Objeto o interfaz</span><span class="sxs-lookup"><span data-stu-id="adc1c-166">Object or interface</span></span>                                               | <span data-ttu-id="adc1c-167">Propiedad o método</span><span class="sxs-lookup"><span data-stu-id="adc1c-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adc1c-168">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="adc1c-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="adc1c-169">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="adc1c-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="adc1c-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="adc1c-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="adc1c-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="adc1c-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="adc1c-172">**IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="adc1c-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="adc1c-173">[**Elemento**](iwmpplaylist-item--vb-and-c.md) (obtener \_ elemento en C#)</span><span class="sxs-lookup"><span data-stu-id="adc1c-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="adc1c-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adc1c-174">Requirements</span></span>



| <span data-ttu-id="adc1c-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc1c-175">Requirement</span></span> | <span data-ttu-id="adc1c-176">Value</span><span class="sxs-lookup"><span data-stu-id="adc1c-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="adc1c-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adc1c-177">Header</span></span><br/> | <dl> <span data-ttu-id="adc1c-178"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc1c-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc1c-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="adc1c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc1c-180">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="adc1c-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="adc1c-181">**Interfaz IWMPMedia2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="adc1c-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="adc1c-182">**Interfaz IWMPMedia3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="adc1c-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





