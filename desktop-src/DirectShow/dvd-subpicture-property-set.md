---
description: Las propiedades de subapicture de DVD controlan el color, el contraste y la salida de la presentación de la subaspección.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propiedades de subpicture de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909093"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="e6c43-103">Conjunto de propiedades de subpicture de DVD</span><span class="sxs-lookup"><span data-stu-id="e6c43-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="e6c43-104">Las propiedades de subapicture de DVD controlan el color, el contraste y la salida de la presentación de la subaspección.</span><span class="sxs-lookup"><span data-stu-id="e6c43-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="e6c43-105">En la siguiente información se presentan las constantes y los tipos de datos necesarios que se usarán para este conjunto de propiedades en las llamadas a [**métodos IKsPropertySet.**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="e6c43-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="e6c43-106">Proporciona valores para los parámetros **GUID** (*guidPropSet*), property ID (*dwPropID*) y property data type (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="e6c43-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="e6c43-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="e6c43-107">Label</span></span> | <span data-ttu-id="e6c43-108">Value</span><span class="sxs-lookup"><span data-stu-id="e6c43-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="e6c43-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e6c43-109">Property Set GUID</span></span> | <span data-ttu-id="e6c43-110">DVDSubPic de AM \_ KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="e6c43-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="e6c43-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6c43-111">Property ID</span></span>                           | <span data-ttu-id="e6c43-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6c43-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c43-113">AM \_ PROPERTY \_ DVDSUBPIC \_ COMPOSIT \_ ON</span><span class="sxs-lookup"><span data-stu-id="e6c43-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="e6c43-114">Propiedad de solo establecimiento que habilita o deshabilita la presentación de subaspección.</span><span class="sxs-lookup"><span data-stu-id="e6c43-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="e6c43-115">DirectShow define el tipo de datos booleano **\_ AM PROPERTY \_ COMPOSIT \_ ON** para esta propiedad, así como PAM PROPERTY COMPOSIT ON como puntero \_ a este tipo de \_ \_ datos.</span><span class="sxs-lookup"><span data-stu-id="e6c43-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="e6c43-116">**TRUE** indica que muestra la subaspección, **FALSE** indica deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="e6c43-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="e6c43-117">Consulte la parte WDM de Windows DDK para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e6c43-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="e6c43-118">PROPIEDAD \_ AM \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="e6c43-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="e6c43-119">Propiedad de solo establecimiento que especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiarán.</span><span class="sxs-lookup"><span data-stu-id="e6c43-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="e6c43-120">El tipo de datos [**es AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli)</span><span class="sxs-lookup"><span data-stu-id="e6c43-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="e6c43-121">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e6c43-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="e6c43-122">PALETA \_ \_ DVDSUBPIC DE LA \_ PROPIEDAD AM</span><span class="sxs-lookup"><span data-stu-id="e6c43-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="e6c43-123">Establece la paleta para una subaspección.</span><span class="sxs-lookup"><span data-stu-id="e6c43-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="e6c43-124">El tipo de datos [**es AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)</span><span class="sxs-lookup"><span data-stu-id="e6c43-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="e6c43-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6c43-125">Remarks</span></span>

<span data-ttu-id="e6c43-126">La **propiedad DE AM PROPERTY \_ \_ DVDSUBPIC \_ HLI** es de solo establecimiento.</span><span class="sxs-lookup"><span data-stu-id="e6c43-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="e6c43-127">Especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiarán.</span><span class="sxs-lookup"><span data-stu-id="e6c43-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="e6c43-128">Esto difiere de la especificación de DVD-Video, en que el navegador de DVD de Microsoft analiza toda la información del botón y el teclado y pasa solo un rectángulo de resaltado al descodificador de subpicture en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="e6c43-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="e6c43-129">Como resultado, la información de resaltado se envía al descodificador con más frecuencia de la que está presente en la secuencia de DVD.</span><span class="sxs-lookup"><span data-stu-id="e6c43-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="e6c43-130">La información de resaltado llega de forma asincrónica al flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="e6c43-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="e6c43-131">El descodificador usa las marcas de tiempo de inicio y finalización resaltadas para correlacionar la información de resaltado con la información de subespectura pertinente, si existe.</span><span class="sxs-lookup"><span data-stu-id="e6c43-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="e6c43-132">Si el descodificador no ha recibido información de secuencias de subpicture para las marcas de tiempo solicitadas, el descodificador asume que la información de resaltado es independiente y no se aplica a una subapicture.</span><span class="sxs-lookup"><span data-stu-id="e6c43-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="e6c43-133">En este caso, el descodificador asume que la información de color y contraste es del mismo color.</span><span class="sxs-lookup"><span data-stu-id="e6c43-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="e6c43-134">Los datos no están completamente en formato de disco DVD.</span><span class="sxs-lookup"><span data-stu-id="e6c43-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="e6c43-135">Microsoft proporciona una estructura adicional de tipo [**AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) que se pasa como parámetro a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e6c43-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="e6c43-136">Esta estructura describe el botón seleccionado actualmente en la información de resaltado de DVD.</span><span class="sxs-lookup"><span data-stu-id="e6c43-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="e6c43-137">El navegador de DVD procesa toda la información de pulsación de tecla y envía nueva información de resaltado cada vez que cambia el estado de un botón.</span><span class="sxs-lookup"><span data-stu-id="e6c43-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="e6c43-138">La información describe solo un modo de un botón a la vez.</span><span class="sxs-lookup"><span data-stu-id="e6c43-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="e6c43-139">Incluye un rectángulo de presentación en coordenadas de píxeles de la pantalla o una presentación de la subapicture, si está presente.</span><span class="sxs-lookup"><span data-stu-id="e6c43-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="e6c43-140">La estructura también contiene información de color y contraste, pero solo para el estado actual del botón seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e6c43-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="e6c43-141">El formato se define en la especificación de DVD.</span><span class="sxs-lookup"><span data-stu-id="e6c43-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="e6c43-142">La información de resaltado contiene marcas de tiempo de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="e6c43-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="e6c43-143">Se encuentran en las mismas unidades que otras marcas de tiempo, con dos excepciones: una marca de hora de inicio de 0xFFFFFFFF significa que la propiedad de resaltado es efectiva tras la recepción y una marca de hora de finalización de 0xFFFFFFFF significa que la propiedad de resaltado es válida hasta que se recibe el siguiente resaltado.</span><span class="sxs-lookup"><span data-stu-id="e6c43-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="e6c43-144">El campo HLISS se define en la especificación de DVD.</span><span class="sxs-lookup"><span data-stu-id="e6c43-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="e6c43-145">Un valor de cero indica que todos los resaltados no son válidos y el descodificador debe deshabilitar todos los resaltados.</span><span class="sxs-lookup"><span data-stu-id="e6c43-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c43-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6c43-146">Requirements</span></span>



| <span data-ttu-id="e6c43-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c43-147">Requirement</span></span> | <span data-ttu-id="e6c43-148">Value</span><span class="sxs-lookup"><span data-stu-id="e6c43-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c43-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6c43-149">Header</span></span><br/> | <dl> <span data-ttu-id="e6c43-150"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c43-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c43-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e6c43-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c43-152">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="e6c43-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




