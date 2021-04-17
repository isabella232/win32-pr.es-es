---
description: Las propiedades de subimagen de DVD controlan el color, el contraste y la salida de la pantalla de la imagen.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propiedades de subimagen de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680444"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="ffded-103">Conjunto de propiedades de subimagen de DVD</span><span class="sxs-lookup"><span data-stu-id="ffded-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="ffded-104">Las propiedades de subimagen de DVD controlan el color, el contraste y la salida de la pantalla de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ffded-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="ffded-105">La siguiente información presenta las constantes y los tipos de datos necesarios para usar en esta propiedad establecida en llamadas a métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="ffded-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="ffded-106">Proporciona valores para los parámetros **GUID** (*GUIDPROPSET*), ID. de propiedad (*dwPropID*) y tipo de datos de propiedad (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="ffded-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="ffded-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="ffded-107">Property Set GUID</span></span> | <span data-ttu-id="ffded-108">\_DvdSubPic KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="ffded-108">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="ffded-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffded-109">Property ID</span></span>                           | <span data-ttu-id="ffded-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffded-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffded-111">\_propiedad AM \_ DVDSUBPIC \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffded-111">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="ffded-112">Propiedad de solo establecimiento que habilita o deshabilita la presentación de la subimagen.</span><span class="sxs-lookup"><span data-stu-id="ffded-112">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="ffded-113">DirectShow define la **\_ propiedad \_ de AM composiciones \_ en** el tipo de datos booleano para esta propiedad, así como la propiedad de PAM componer \_ \_ \_ en como un puntero a este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ffded-113">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="ffded-114">**True** indica que se muestra la subimagen, **false** indica deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="ffded-114">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="ffded-115">Para obtener más información, consulte la parte WDM del DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="ffded-115">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="ffded-116">\_propiedad AM \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="ffded-116">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="ffded-117">Propiedad de solo establecimiento que especifica un rectángulo de subimagen o pantalla cuyo color o contraste se van a cambiar.</span><span class="sxs-lookup"><span data-stu-id="ffded-117">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="ffded-118">El tipo de datos es la [**\_ propiedad AM \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="ffded-118">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="ffded-119">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ffded-119">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="ffded-120">\_propiedad AM \_ DVDSUBPIC \_ paleta</span><span class="sxs-lookup"><span data-stu-id="ffded-120">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="ffded-121">Establece la paleta para una subimagen.</span><span class="sxs-lookup"><span data-stu-id="ffded-121">Sets the palette for a subpicture.</span></span> <span data-ttu-id="ffded-122">El tipo de datos es la [**\_ propiedad AM \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="ffded-122">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="ffded-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffded-123">Remarks</span></span>

<span data-ttu-id="ffded-124">La propiedad AM de la propiedad **\_ \_ DVDSUBPIC \_ HLI** es de solo configuración.</span><span class="sxs-lookup"><span data-stu-id="ffded-124">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="ffded-125">Especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiará.</span><span class="sxs-lookup"><span data-stu-id="ffded-125">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="ffded-126">Esto difiere de la especificación de DVD-Video, en que el navegador de DVD de Microsoft analiza toda la información del botón y del teclado, y pasa solo un rectángulo de resaltado al descodificador de la subimagen en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="ffded-126">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="ffded-127">Como resultado, la información de resaltado se envía al descodificador con más frecuencia de la que se encuentra en la secuencia de DVD.</span><span class="sxs-lookup"><span data-stu-id="ffded-127">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="ffded-128">La información de resaltado llega asincrónicamente al flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="ffded-128">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="ffded-129">El descodificador utiliza las marcas de tiempo de inicio y finalización de resaltado para correlacionar la información de resaltado con la información de la subimagen correspondiente, si existe.</span><span class="sxs-lookup"><span data-stu-id="ffded-129">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="ffded-130">Si el descodificador no ha recibido ninguna información de flujo de subimagen para las marcas de tiempo solicitadas, el descodificador supone que la información de resaltado es independiente y no se aplica a una subimagen.</span><span class="sxs-lookup"><span data-stu-id="ffded-130">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="ffded-131">En este caso, el descodificador supone que la información de color y contraste es todo el mismo color.</span><span class="sxs-lookup"><span data-stu-id="ffded-131">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="ffded-132">Los datos no tienen un formato de disco completo en DVD.</span><span class="sxs-lookup"><span data-stu-id="ffded-132">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="ffded-133">Microsoft proporciona una estructura adicional de la [**\_ propiedad \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) de tipo AM que se pasa como parámetro a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ffded-133">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="ffded-134">Esta estructura describe el botón seleccionado actualmente de la información de resaltado del DVD.</span><span class="sxs-lookup"><span data-stu-id="ffded-134">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="ffded-135">El navegador de DVD procesa toda la información sobre las pulsaciones de teclas y envía información de resaltado nueva cada vez que cambia el estado de un botón.</span><span class="sxs-lookup"><span data-stu-id="ffded-135">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="ffded-136">La información describe solo un modo de un botón a la vez.</span><span class="sxs-lookup"><span data-stu-id="ffded-136">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="ffded-137">Incluye un rectángulo de presentación en coordenadas en píxeles de la pantalla, o una presentación de la subimagen, si está presente.</span><span class="sxs-lookup"><span data-stu-id="ffded-137">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="ffded-138">La estructura también contiene información sobre el color y el contraste, pero solo para el estado actual del botón seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ffded-138">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="ffded-139">El formato se define en la especificación de DVD.</span><span class="sxs-lookup"><span data-stu-id="ffded-139">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="ffded-140">La información de resaltado contiene marcas de tiempo de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="ffded-140">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="ffded-141">Se encuentran en las mismas unidades que otras marcas de tiempo, con dos excepciones: una marca de hora de inicio de 0xFFFFFFFF significa que la propiedad resaltada es efectiva en la recepción y una marca de hora de finalización de 0xFFFFFFFF significa que la propiedad resaltado es válida hasta que se recibe el siguiente resaltado.</span><span class="sxs-lookup"><span data-stu-id="ffded-141">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="ffded-142">El campo HLISS es como se define en la especificación de DVD.</span><span class="sxs-lookup"><span data-stu-id="ffded-142">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="ffded-143">Un valor de cero indica que todos los resaltados no son válidos y el descodificador debe deshabilitar todos los resaltados.</span><span class="sxs-lookup"><span data-stu-id="ffded-143">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffded-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffded-144">Requirements</span></span>



| <span data-ttu-id="ffded-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffded-145">Requirement</span></span> | <span data-ttu-id="ffded-146">Value</span><span class="sxs-lookup"><span data-stu-id="ffded-146">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffded-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffded-147">Header</span></span><br/> | <dl> <span data-ttu-id="ffded-148"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffded-148"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffded-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffded-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffded-150">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="ffded-150">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




