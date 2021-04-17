---
title: Interfaz IWMPControls (VB y C) (WMP. h)
description: Proporciona una manera de manipular la reproducción de un elemento multimedia representando los controles de transporte de Windows Media Player, como reproducir, detener y pausar. la interfaz IWMPControls expone las siguientes propiedades.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls (VB y C) interfaz de Windows Media Player
- IWMPControls (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690427"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="9343a-105">Interfaz IWMPControls (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="9343a-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="9343a-106">Proporciona una manera de manipular la reproducción de un elemento multimedia representando los controles de transporte de Windows Media Player, como reproducir, detener y pausar.</span><span class="sxs-lookup"><span data-stu-id="9343a-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="9343a-107">La interfaz **IWMPControls** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="9343a-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="9343a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9343a-108">Members</span></span>

<span data-ttu-id="9343a-109">La interfaz **IWMPControls (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9343a-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="9343a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9343a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9343a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9343a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9343a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9343a-112">Methods</span></span>

<span data-ttu-id="9343a-113">La interfaz **IWMPControls (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9343a-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="9343a-114">Método</span><span class="sxs-lookup"><span data-stu-id="9343a-114">Method</span></span>                                                                       | <span data-ttu-id="9343a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9343a-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9343a-116">**fastForward**</span><span class="sxs-lookup"><span data-stu-id="9343a-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="9343a-117">Inicia la reproducción rápida del elemento multimedia en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="9343a-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="9343a-118">**fastReverse**</span><span class="sxs-lookup"><span data-stu-id="9343a-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="9343a-119">Inicia la reproducción rápida del elemento multimedia en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="9343a-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="9343a-120">**Nueva**</span><span class="sxs-lookup"><span data-stu-id="9343a-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="9343a-121">Establece el elemento siguiente de la lista de reproducción como el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="9343a-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="9343a-122">**temporalmente**</span><span class="sxs-lookup"><span data-stu-id="9343a-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="9343a-123">Pausa la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="9343a-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="9343a-124">**reproducción**</span><span class="sxs-lookup"><span data-stu-id="9343a-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="9343a-125">Comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.</span><span class="sxs-lookup"><span data-stu-id="9343a-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="9343a-126">**playItem**</span><span class="sxs-lookup"><span data-stu-id="9343a-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="9343a-127">Reproduce el elemento multimedia especificado.</span><span class="sxs-lookup"><span data-stu-id="9343a-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="9343a-128">**previo**</span><span class="sxs-lookup"><span data-stu-id="9343a-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="9343a-129">Establece el elemento anterior de la lista de reproducción como el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="9343a-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="9343a-130">**detener**</span><span class="sxs-lookup"><span data-stu-id="9343a-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="9343a-131">Detiene la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="9343a-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="9343a-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9343a-132">Properties</span></span>

<span data-ttu-id="9343a-133">La interfaz **IWMPControls (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9343a-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="9343a-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9343a-134">Property</span></span>                                                                                                    | <span data-ttu-id="9343a-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="9343a-135">Access type</span></span>           | <span data-ttu-id="9343a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="9343a-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9343a-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="9343a-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="9343a-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9343a-138">Read/write</span></span><br/> | <span data-ttu-id="9343a-139">Obtiene o establece el elemento multimedia actual en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9343a-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="9343a-140">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="9343a-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="9343a-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9343a-141">Read/write</span></span><br/> | <span data-ttu-id="9343a-142">Obtiene o establece el número de marcador actual.</span><span class="sxs-lookup"><span data-stu-id="9343a-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="9343a-143">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="9343a-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="9343a-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9343a-144">Read/write</span></span><br/> | <span data-ttu-id="9343a-145">Obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.</span><span class="sxs-lookup"><span data-stu-id="9343a-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="9343a-146">**currentPositionString**</span><span class="sxs-lookup"><span data-stu-id="9343a-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="9343a-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9343a-147">Read-only</span></span><br/>  | <span data-ttu-id="9343a-148">Obtiene la posición actual en el elemento multimedia como **System. String**.</span><span class="sxs-lookup"><span data-stu-id="9343a-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="9343a-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="9343a-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="9343a-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9343a-150">Read-only</span></span><br/>  | <span data-ttu-id="9343a-151">Obtiene un valor que indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="9343a-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="9343a-152">En C#, este es el método **Get \_ isavailable** .</span><span class="sxs-lookup"><span data-stu-id="9343a-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="9343a-153">Obtenga una interfaz **IWMPControls** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="9343a-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="9343a-154">Object</span><span class="sxs-lookup"><span data-stu-id="9343a-154">Object</span></span>                                                                   | <span data-ttu-id="9343a-155">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9343a-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="9343a-156">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9343a-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="9343a-157">**Ctlcontrols**</span><span class="sxs-lookup"><span data-stu-id="9343a-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="9343a-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9343a-158">Requirements</span></span>



| <span data-ttu-id="9343a-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="9343a-159">Requirement</span></span> | <span data-ttu-id="9343a-160">Value</span><span class="sxs-lookup"><span data-stu-id="9343a-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9343a-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9343a-161">Header</span></span><br/> | <dl> <span data-ttu-id="9343a-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="9343a-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9343a-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="9343a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9343a-164">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="9343a-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="9343a-165">**Interfaz IWMPControls2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9343a-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9343a-166">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9343a-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





