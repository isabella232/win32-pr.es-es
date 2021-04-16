---
description: Las siguientes constantes especifican el conjunto válido de propiedades de elemento de analizador de adquisición de imágenes de Windows (WIA).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes de propiedad del elemento WIA del escáner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705679"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="576ed-103">Constantes de propiedad del elemento WIA del escáner</span><span class="sxs-lookup"><span data-stu-id="576ed-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="576ed-104">Las siguientes constantes especifican el conjunto válido de propiedades de elemento de analizador de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="576ed-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="576ed-105">El prefijo "WIA \_ IP \_ " indica una propiedad de elemento para los dispositivos de escáner y es la Convención de nomenclatura utilizada en C/C++.</span><span class="sxs-lookup"><span data-stu-id="576ed-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="576ed-106">Con el fin de crear scripts, estas constantes usan el prefijo "ScannerPicture" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="576ed-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="576ed-107">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="576ed-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="576ed-108">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="576ed-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="576ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="576ed-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="576ed-111">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="576ed-112">Activa o desactiva el dessesgo automático.</span><span class="sxs-lookup"><span data-stu-id="576ed-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="576ed-113">Opcional solo para WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="576ed-114">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="576ed-115">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-116">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-116">Constant</span></span></th>
<th><span data-ttu-id="576ed-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="576ed-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="576ed-119">Active dessesgar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="576ed-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="576ed-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="576ed-121">Desactive dessesgar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="576ed-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="576ed-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-123">Valores de brillo de la imagen disponibles en el escáner.</span><span class="sxs-lookup"><span data-stu-id="576ed-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="576ed-124">Contiene la configuración actual de brillo del hardware para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="576ed-125">Una aplicación establece esta propiedad en el valor de brillo del hardware.</span><span class="sxs-lookup"><span data-stu-id="576ed-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="576ed-126">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-127">Los valores deben estar asignados en un intervalo comprendido entre-1000 y 1000, donde 1000 corresponde al brillo máximo, 0 corresponde al brillo normal y-1000 corresponde al brillo mínimo.</span><span class="sxs-lookup"><span data-stu-id="576ed-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="576ed-128">Se requiere para todos los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-129">Opcional, pero recomendado, para los elementos de WIA_CATEGORY_FINISHED_FILE que admiten vistas previas.</span><span class="sxs-lookup"><span data-stu-id="576ed-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="576ed-130">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="576ed-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-132">Contiene la configuración de contraste de hardware actual para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="576ed-133">Una aplicación establece esta propiedad en el valor de contraste del hardware.</span><span class="sxs-lookup"><span data-stu-id="576ed-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="576ed-134">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-135">Los valores se deben asignar en un intervalo comprendido entre-1000 y 1000, donde-1000 corresponde al contraste mínimo, 0 corresponde al contraste normal y 1000 corresponde al contraste máximo.</span><span class="sxs-lookup"><span data-stu-id="576ed-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="576ed-136">Se requiere para todos los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-137">Opcional, pero recomendado, para los elementos de WIA_CATEGORY_FINISHED_FILE que admiten vistas previas.</span><span class="sxs-lookup"><span data-stu-id="576ed-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="576ed-138">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="576ed-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-140">Contiene la configuración de la intención actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-140">Contains the current intent settings.</span></span> <span data-ttu-id="576ed-141">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-142">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-143">No se admite para elementos de WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-144">Tipo: <strong>VT_I4</strong> acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="576ed-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="576ed-145">El controlador los usa para preestablecer las propiedades de los elementos según el uso previsto de la aplicación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="576ed-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="576ed-146">Esto puede incluir, por ejemplo, la calidad máxima, el tamaño mínimo, etc.</span><span class="sxs-lookup"><span data-stu-id="576ed-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="576ed-147">El controlador elige la profundidad de bits, en puntos por pulgada, y otras opciones que determina son adecuadas para la intención seleccionada.</span><span class="sxs-lookup"><span data-stu-id="576ed-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="576ed-148">Depende de la aplicación leer la configuración actual para determinar qué propiedades se cambiaron.</span><span class="sxs-lookup"><span data-stu-id="576ed-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="576ed-149">Una aplicación establece esta propiedad para establecer automáticamente las propiedades de WIA para un intento de adquisición específico.</span><span class="sxs-lookup"><span data-stu-id="576ed-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="576ed-150">Esta propiedad es necesaria para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="576ed-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="576ed-151">Una aplicación establece esta propiedad para establecer automáticamente las propiedades de WIA para un intento de adquisición específico.</span><span class="sxs-lookup"><span data-stu-id="576ed-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-152">Las marcas se pueden combinar con un operador OR bit a bit, pero una imagen no puede ser de escala de grises <strong>y de color</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-153">Esta propiedad es necesaria para todos los escáneres.</span><span class="sxs-lookup"><span data-stu-id="576ed-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="576ed-154">La tabla siguiente contiene las marcas de tipo de imagen y sus definiciones.</span><span class="sxs-lookup"><span data-stu-id="576ed-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="576ed-155">Estas marcas se usan para establecer el tipo de imagen que se va a usar: color, escala de grises, etc.</span><span class="sxs-lookup"><span data-stu-id="576ed-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-156">Marcas de tipo de imagen previsto</span><span class="sxs-lookup"><span data-stu-id="576ed-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="576ed-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="576ed-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="576ed-159">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="576ed-159">Default value.</span></span> <span data-ttu-id="576ed-160">No se especifica ningún intento.</span><span class="sxs-lookup"><span data-stu-id="576ed-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="576ed-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="576ed-162">La aplicación intenta preparar el dispositivo para un examen de color.</span><span class="sxs-lookup"><span data-stu-id="576ed-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="576ed-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="576ed-164">La aplicación intenta preparar el dispositivo para un análisis de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="576ed-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="576ed-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="576ed-166">La aplicación pretende preparar el dispositivo para el análisis de texto.</span><span class="sxs-lookup"><span data-stu-id="576ed-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="576ed-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="576ed-168">Máscara para todas las marcas de tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="576ed-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="576ed-169">La tabla siguiente contiene las marcas de calidad y tamaño y sus definiciones.</span><span class="sxs-lookup"><span data-stu-id="576ed-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="576ed-170">Estas marcas se utilizan para establecer el nivel de calidad previsto.</span><span class="sxs-lookup"><span data-stu-id="576ed-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-171">Marcas de calidad y tamaño de imagen previsto</span><span class="sxs-lookup"><span data-stu-id="576ed-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="576ed-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="576ed-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="576ed-174">La aplicación intenta preparar el dispositivo para el examen de una imagen que resulta en un examen pequeño.</span><span class="sxs-lookup"><span data-stu-id="576ed-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="576ed-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="576ed-176">La aplicación pretende preparar el dispositivo para el análisis de una imagen de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="576ed-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="576ed-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="576ed-178">Esta marca es una máscara para todas las marcas de tamaño y calidad.</span><span class="sxs-lookup"><span data-stu-id="576ed-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="576ed-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="576ed-180">La aplicación pretende preparar el dispositivo para el análisis de una vista previa.</span><span class="sxs-lookup"><span data-stu-id="576ed-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="576ed-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-182">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-183">Contiene el número de píxeles en la dirección x de WIA_IPS_XPOS a la coordenada x de la esquina superior de la imagen que se va a dessesgar.</span><span class="sxs-lookup"><span data-stu-id="576ed-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="576ed-184">Por lo tanto, describe, junto con WIA_IPS_DESKEW_Y, donde las dos esquinas superiores de la imagen sesgada se encuentran dentro del rectángulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT y WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="576ed-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="576ed-185">el controlador del escáner implementa su propiedad si admite el desfase.</span><span class="sxs-lookup"><span data-stu-id="576ed-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="576ed-186">Los valores válidos para WIA_IPS_DESKEW_X deben estar entre 0 y (WIA_IPS_XEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="576ed-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="576ed-187">Un valor de 0 significa que no se debe realizar ninguna desfase.</span><span class="sxs-lookup"><span data-stu-id="576ed-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="576ed-188">Esta propiedad es opcional para los elementos de las categorías WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM; y no está disponible para los elementos de WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-189">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="576ed-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="576ed-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-191">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-192">Contiene el número de píxeles en la dirección y desde WIA_IPS_YPOS hasta la coordenada y de la esquina izquierda de la imagen que se va a dessesgar.</span><span class="sxs-lookup"><span data-stu-id="576ed-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="576ed-193">Por lo tanto, describe, junto con WIA_IPS_DESKEW_X, donde las dos esquinas superiores de la imagen sesgada se encuentran dentro del rectángulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT y WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="576ed-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="576ed-194">El controlador del escáner implementa esta propiedad si admite la dessesgación.</span><span class="sxs-lookup"><span data-stu-id="576ed-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="576ed-195">Los valores válidos para WIA_IPS_DESKEW_Y deben estar entre 0 y (WIA_IPS_YEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="576ed-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="576ed-196">Un valor de 0 significa que no se debe realizar ninguna desfase.</span><span class="sxs-lookup"><span data-stu-id="576ed-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="576ed-197">Esta propiedad es opcional para los elementos de las categorías WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM; y no está disponible para los elementos de WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-198">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="576ed-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="576ed-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-200">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-201">Contiene el origen y el modo de adquisición del detector actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="576ed-202">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-203">Una aplicación Lee esta propiedad para determinar el origen de adquisición actual del escáner o para escribir esta propiedad para establecer el origen y el modo del escáner.</span><span class="sxs-lookup"><span data-stu-id="576ed-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="576ed-204">Además, las aplicaciones usan esta propiedad para habilitar y deshabilitar la funcionalidad de dúplex.</span><span class="sxs-lookup"><span data-stu-id="576ed-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="576ed-205">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="576ed-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="576ed-206">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-207">Marcas</span><span class="sxs-lookup"><span data-stu-id="576ed-207">Flags</span></span></th>
<th><span data-ttu-id="576ed-208">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-209">D</span><span class="sxs-lookup"><span data-stu-id="576ed-209">DUPLEX</span></span></td>
<td><span data-ttu-id="576ed-210">Digitalice mediante operaciones de dúplex.</span><span class="sxs-lookup"><span data-stu-id="576ed-210">Scan using duplexer operations.</span></span> <span data-ttu-id="576ed-211">Examine ambos lados del documento con la configuración común configurada para el elemento del alimentador (WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="576ed-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="576ed-212">No se pueden establecer dúplex y ADVANCE_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="576ed-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="576ed-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="576ed-214">Digitalice con valores individuales configurados para cada elemento secundario del alimentador (WIA_CATEGORY_FEEDER_FRONT y WIA_CATEGORY_FEEDER_BACK).</span><span class="sxs-lookup"><span data-stu-id="576ed-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="576ed-215">No se pueden establecer dúplex y ADVANCE_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="576ed-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="576ed-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="576ed-217">Busque primero el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="576ed-217">Scan the front of the document first.</span></span> <span data-ttu-id="576ed-218">Este valor es válido cuando se establece DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="576ed-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="576ed-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="576ed-220">Digitalice primero la parte posterior del documento.</span><span class="sxs-lookup"><span data-stu-id="576ed-220">Scan the back of the document first.</span></span> <span data-ttu-id="576ed-221">Este valor es válido cuando se establece DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="576ed-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="576ed-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="576ed-223">Examinar solo la parte frontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="576ed-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="576ed-225">Examinar solo la copia.</span><span class="sxs-lookup"><span data-stu-id="576ed-225">Scan the back only.</span></span> <span data-ttu-id="576ed-226">Este valor es válido cuando se establece DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="576ed-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="576ed-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-228">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-229">Habilita la especificación de un archivo adjunto de análisis de película determinado cuando hay más de uno.</span><span class="sxs-lookup"><span data-stu-id="576ed-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="576ed-230">Esta propiedad es necesaria para los elementos de WIA_CATEGORY_FILM cuando hay varios elementos de examen de película.</span><span class="sxs-lookup"><span data-stu-id="576ed-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="576ed-231">Si el dispositivo admite solo un elemento de película de escáner raíz, esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="576ed-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="576ed-232">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="576ed-233">Valores permitidos: BSTR debe tener el formato @ResourceBinary ,- <ResourceID> para permitir la localización, ya que esta cadena se exponería al usuario a través de la interfaz de usuario de análisis de película.</span><span class="sxs-lookup"><span data-stu-id="576ed-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="576ed-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-235">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-236">Permite configurar el análisis de película actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="576ed-237">Esta propiedad es necesaria para el elemento WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="576ed-238">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-239">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-240">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-240">Constant</span></span></th>
<th><span data-ttu-id="576ed-241">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="576ed-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="576ed-243">Buscar una diapositiva de color.</span><span class="sxs-lookup"><span data-stu-id="576ed-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="576ed-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="576ed-245">Busca un color negativo.</span><span class="sxs-lookup"><span data-stu-id="576ed-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="576ed-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="576ed-247">Busca un negativo en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="576ed-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="576ed-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-249">Reservado para uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="576ed-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="576ed-250">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="576ed-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-252">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-253">Especifica el número de elementos que se almacenan en el elemento de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="576ed-254">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="576ed-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-256">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-257">Activa o desactiva la lámpara del escáner.</span><span class="sxs-lookup"><span data-stu-id="576ed-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="576ed-258">Opcional para los elementos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM, y recomendado para WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-259">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-260">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-261">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-261">Constant</span></span></th>
<th><span data-ttu-id="576ed-262">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="576ed-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="576ed-264">Encienda la lámpara.</span><span class="sxs-lookup"><span data-stu-id="576ed-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="576ed-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="576ed-266">Desactive la lámpara.</span><span class="sxs-lookup"><span data-stu-id="576ed-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="576ed-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-268">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-269">Establece el tiempo máximo durante el cual se mantiene la lámpara cuando no se utiliza el escáner.</span><span class="sxs-lookup"><span data-stu-id="576ed-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="576ed-270">Opcional para los elementos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM, y recomendado para WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-271">Tipo: <strong>VT_UI4</strong>, acceso: lectura/escritura, valores válidos: 0-0xFFF segundos</span><span class="sxs-lookup"><span data-stu-id="576ed-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="576ed-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-273">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-274">Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="576ed-275">Puede ser el ancho del alimentador de la hoja o la cama de digitalización, según el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="576ed-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="576ed-276">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="576ed-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-278">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-279">Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="576ed-280">Puede tratarse del alto del alimentador de la hoja o del Banco de digitalización, según el tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="576ed-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="576ed-281">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="576ed-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-283">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-284">Especifica el ancho mínimo, en milésimas de pulgada, que se examina en el eje horizontal (X) en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="576ed-285">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="576ed-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-287">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-288">Especifica el alto mínimo, en milésimas de pulgada, que se examina en el eje vertical (Y) en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="576ed-289">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="576ed-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-291">Reservado para uso futuro y no se implementa en este momento.</span><span class="sxs-lookup"><span data-stu-id="576ed-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="576ed-292">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="576ed-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-294">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-295">Resolución óptica horizontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="576ed-296">Resolución óptica horizontal más alta admitida en PPP.</span><span class="sxs-lookup"><span data-stu-id="576ed-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="576ed-297">Esta propiedad es un valor único.</span><span class="sxs-lookup"><span data-stu-id="576ed-297">This property is a single value.</span></span> <span data-ttu-id="576ed-298">Esta no es una lista de todas las resoluciones que puede generar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="576ed-299">En su lugar, se trata de la resolución de los medios ópticos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="576ed-300">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="576ed-301">Esta propiedad es necesaria para todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="576ed-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="576ed-302">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="576ed-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-304">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-305">Resolución óptica vertical.</span><span class="sxs-lookup"><span data-stu-id="576ed-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="576ed-306">Resolución óptica vertical más alta admitida en PPP.</span><span class="sxs-lookup"><span data-stu-id="576ed-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="576ed-307">Esta propiedad es un valor único.</span><span class="sxs-lookup"><span data-stu-id="576ed-307">This property is a single value.</span></span> <span data-ttu-id="576ed-308">Esta no es una lista de todas las resoluciones que genera el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="576ed-309">En su lugar, se trata de la resolución de los medios ópticos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="576ed-310">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="576ed-311">Esta propiedad es necesaria para todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="576ed-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="576ed-312">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="576ed-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-314">Especifica la orientación actual de los documentos que se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="576ed-315">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-316">Una aplicación establece esta propiedad para definir la orientación original de una página o imagen que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="576ed-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="576ed-317">Para obtener información sobre cómo usar WIA_IPS_ORIENTATION, vea <strong>WIA_IPS_PAGE_SIZE</strong>.</span><span class="sxs-lookup"><span data-stu-id="576ed-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-318">WIA_IPS_ORIENTATION hace referencia a la posición del documento que se va a examinar en la superficie del escáner o en el alimentador.</span><span class="sxs-lookup"><span data-stu-id="576ed-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="576ed-319">Es la orientación del documento con respecto a la dirección del análisis.</span><span class="sxs-lookup"><span data-stu-id="576ed-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="576ed-320">WIA_IPS_ROTATION hace referencia a la rotación que se aplica a la imagen una vez digitalizada, justo antes de que se transfiera la imagen a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="576ed-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-321">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-322">En la tabla siguiente se muestran las cuatro constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-323">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-323">Value</span></span></th>
<th><span data-ttu-id="576ed-324">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-325">VERTICAL</span><span class="sxs-lookup"><span data-stu-id="576ed-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="576ed-326">0 grados.</span><span class="sxs-lookup"><span data-stu-id="576ed-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-327">HORIZ</span><span class="sxs-lookup"><span data-stu-id="576ed-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="576ed-328">rotación de 90 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="576ed-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="576ed-329">ROT180</span></span></td>
<td><span data-ttu-id="576ed-330">rotación de 180 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="576ed-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="576ed-331">ROT270</span></span></td>
<td><span data-ttu-id="576ed-332">rotación de 270 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</span><span class="sxs-lookup"><span data-stu-id="576ed-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="576ed-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-334">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-335">Contiene el tamaño de la página que está configurada actualmente para su examen.</span><span class="sxs-lookup"><span data-stu-id="576ed-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="576ed-336">Una aplicación establece esta propiedad para seleccionar las dimensiones de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="576ed-337">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-338">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-339">Para las constantes que se pueden usar con esta propiedad, vea las <a href="-wia-wia2-pagesizeconstants.md"><strong>constantes de tamaño de página de WIA 2,0</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="576ed-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="576ed-340">Tenga en cuenta estos tamaños no fijos, en particular:</span><span class="sxs-lookup"><span data-stu-id="576ed-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-341">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-341">Value</span></span></th>
<th><span data-ttu-id="576ed-342">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="576ed-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="576ed-344">Definido por los valores de las propiedades <strong>WIA_IPS_PAGE_HEIGHT</strong> y <strong>WIA_IPS_PAGE_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="576ed-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="576ed-346">El dispositivo determina automáticamente el tamaño de página.</span><span class="sxs-lookup"><span data-stu-id="576ed-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="576ed-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="576ed-348">Tamaño de página personalizado cuyas dimensiones ya conoce la aplicación y el controlador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="576ed-349">El valor de la propiedad <strong>WIA_IPS_ORIENTATION</strong> determina la orientación de la página seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="576ed-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="576ed-350">Las propiedades <strong>WIA_IPS_PAGE_WIDTH</strong> y <strong>WIA_IPS_PAGE_HEIGHT</strong> notifican las dimensiones de la página, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="576ed-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="576ed-351">Estas propiedades deben estar en acuerdo con <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong>, que contienen las dimensiones de la página en píxeles.</span><span class="sxs-lookup"><span data-stu-id="576ed-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-352">Los valores válidos de tipo WIA_PROP_LIST dependen de valores válidos de la propiedad <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="576ed-353">Por ejemplo, si el dispositivo no puede examinar documentos orientados horizontalmente con un valor de WIA_PAGE_A4, WIA_PAGE_A4 no es un valor válido para la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> cuando <strong>WIA_IPS_ORIENTATION</strong> está establecida en horizontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-354">Si una aplicación establece <strong>WIA_IPS_PAGE_SIZE</strong> en cualquier valor distinto de los tres de la tabla anterior, el minicontrolador debe ajustar los valores de <strong>WIA_IPS_PAGE_WIDTH</strong> y <strong>WIA_IPS_PAGE_HEIGHT</strong> a las dimensiones de la página en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="576ed-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="576ed-355">También debe ajustar los valores de <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> a las dimensiones de la página en píxeles.</span><span class="sxs-lookup"><span data-stu-id="576ed-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="576ed-356">Si una configuración de extensión (<strong>WIA_IPS_XEXTENT</strong> o <strong>WIA_IPS_YEXTENT</strong>) se cambia a un valor que no coincide con la configuración de tamaño de página actual, el minicontrolador debe cambiar el valor de la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="576ed-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="576ed-357">El minicontrolador también debe modificar <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> o <strong>WIA_IPS_PAGE_HEIGHT</strong> de acuerdo con la nueva configuración de extensión.</span><span class="sxs-lookup"><span data-stu-id="576ed-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="576ed-358">Si <strong>WIA_IPS_ORIENTATION</strong> está establecido en horizontal, se intercambiará la configuración de la extensión con respecto a sus valores habituales.</span><span class="sxs-lookup"><span data-stu-id="576ed-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="576ed-359">Por ejemplo, si una aplicación establece <strong>WIA_IPS_PAGE_SIZE</strong> en WIA_PAGE_A4, el minicontrolador establece <strong>WIA_IPS_PAGE_WIDTH</strong> en 11692 y <strong>WIA_IPS_PAGE_HEIGHT</strong> en 8267.</span><span class="sxs-lookup"><span data-stu-id="576ed-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="576ed-360">(El minicontrolador también debe ajustar <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> en consecuencia).</span><span class="sxs-lookup"><span data-stu-id="576ed-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-361">Si <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> se establece en WIA_PAGE_CUSTOM, el valor de orientación no se utiliza para determinar las dimensiones de extensión de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-362">El minicontrolador es responsable de garantizar que la propiedad <strong>WIA_IPS_ORIENTATION</strong> está en acuerdo con el área de selección actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="576ed-363">Si una aplicación cambia el valor de <strong>WIA_IPS_ORIENTATION</strong> a uno que no es válido para el tamaño de página seleccionado actualmente, el minicontrolador debe cambiar el valor de <strong>WIA_IPS_PAGE_SIZE</strong> a un tamaño de página compatible con el nuevo valor de orientación.</span><span class="sxs-lookup"><span data-stu-id="576ed-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="576ed-364">Si una aplicación establece la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM, el área de selección actual no se ve afectada.</span><span class="sxs-lookup"><span data-stu-id="576ed-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="576ed-365">El minicontrolador WIA debe obtener el diseño de la imagen actual, a partir de la configuración actual de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="576ed-366">Si la configuración de tamaño de página da como resultado un área de selección que está fuera de la cama del escáner, el minicontrolador debe ajustar automáticamente los valores de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> a una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="576ed-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="576ed-367">Si las propiedades <strong>WIA_IPS_PAGE_SIZE</strong> y <strong>WIA_IPS_ORIENTATION</strong> se establecen al mismo tiempo y no son válidas cuando se aplican en combinación, el minicontrolador debe generar un error en la configuración de la aplicación devolviendo un error en <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="576ed-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="576ed-368">En los cuatro ejemplos siguientes se muestran distintos escenarios de <strong>WIA_IPS_PAGE_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="576ed-369">El controlador informa de la configuración.</span><span class="sxs-lookup"><span data-stu-id="576ed-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="576ed-370">Una aplicación establece la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> en WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="576ed-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="576ed-371">Una aplicación establece la propiedad <strong>WIA_IPS_ORIENTATION</strong> en horizontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="576ed-372">Una aplicación cambia la propiedad <strong>WIA_IPS_XEXTENT</strong> a un valor menor.</span><span class="sxs-lookup"><span data-stu-id="576ed-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="576ed-373"><strong>Ejemplo 1: el minicontrolador informa de la configuración</strong></span><span class="sxs-lookup"><span data-stu-id="576ed-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="576ed-374">En el ejemplo siguiente, el minicontrolador establece un área de selección personalizada antes de que una aplicación establezca las propiedades de WIA.</span><span class="sxs-lookup"><span data-stu-id="576ed-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="576ed-375">En este caso, el área de selección representa todo el plano.</span><span class="sxs-lookup"><span data-stu-id="576ed-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="576ed-376"><strong>Ejemplo 2: una aplicación establece la</strong> <strong></strong><strong>propiedad WIA_IPS_PAGE_SIZE en WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="576ed-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="576ed-377"><strong>Ejemplo 3: una aplicación establece la</strong> <strong></strong><strong>propiedad WIA_IPS_ORIENTATION en horizontal</strong>  </span><span class="sxs-lookup"><span data-stu-id="576ed-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="576ed-378">La cama física debe ser capaz de adquirir una página que estaba originalmente en orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="576ed-379"><strong>Ejemplo 4: una aplicación cambia la</strong> <strong></strong> <strong>propiedad WIA_IPS_XEXTENT a un valor más pequeño</strong></span><span class="sxs-lookup"><span data-stu-id="576ed-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="576ed-380">En el ejemplo siguiente, una aplicación cambia la propiedad <strong>WIA_IPS_XEXTENT</strong> a 1000.</span><span class="sxs-lookup"><span data-stu-id="576ed-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="576ed-381">El minicontrolador debe asumir que el nuevo valor incluido en <strong>WIA_IPS_XEXTENT</strong> ya no es válido para la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> y, por tanto, debe cambiar <strong>WIA_IPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="576ed-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="576ed-382">El minicontrolador también debe ajustar <strong>WIA_IPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="576ed-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="576ed-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-384">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-385">Contiene el alto, en milésimas de pulgada, de la página seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="576ed-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="576ed-386">El minicontrolador crea y mantiene la propiedad <strong>WIA_IPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="576ed-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="576ed-387">Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando.</span><span class="sxs-lookup"><span data-stu-id="576ed-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="576ed-388">Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del alto de la página cuya propiedad <strong>WIA_IPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM (que es un valor de la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="576ed-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="576ed-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> debe estar sincronizada con <strong>WIA_IPS_XEXTENT</strong>, que indica el alto, en píxeles, de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="576ed-390">Esta propiedad es necesaria para los elementos de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="576ed-391">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="576ed-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-393">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-394">Contiene el ancho de la página actual seleccionada, en milésimas de pulgada.</span><span class="sxs-lookup"><span data-stu-id="576ed-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="576ed-395">Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando.</span><span class="sxs-lookup"><span data-stu-id="576ed-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="576ed-396">Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del ancho de la página cuya propiedad <strong>WIA_IPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="576ed-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="576ed-397"><strong>WIA_IPS_PAGE_WIDTH</strong> debe estar sincronizado con el valor de <strong>WIA_IPS_XEXTENT</strong>, que notifica el ancho, en píxeles, de la página que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="576ed-398">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-399">Esta propiedad es necesaria para los elementos de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="576ed-400">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="576ed-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-402">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-403">Contiene el número actual de páginas que se van a adquirir de un alimentador de documentos automático.</span><span class="sxs-lookup"><span data-stu-id="576ed-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="576ed-404">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-405">Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> es cero a través del número máximo de páginas que puede examinar el analizador.</span><span class="sxs-lookup"><span data-stu-id="576ed-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="576ed-406">El valor es ALL_PAGES (= 0) si el escáner puede realizar un análisis continuo.</span><span class="sxs-lookup"><span data-stu-id="576ed-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="576ed-407">Una aplicación Lee esta propiedad para determinar la capacidad de página del alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="576ed-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="576ed-408">La aplicación también establece esta propiedad en el número de páginas que va a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-409">Si el modo dúplex está habilitado (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> está establecido en alimentador | DÚPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> sigue siendo igual al número de páginas que se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-410">Una hoja de papel contendrá automáticamente dos páginas si está habilitada la opción dúplex, incluso si la parte posterior de la página está en blanco.</span><span class="sxs-lookup"><span data-stu-id="576ed-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="576ed-411">Establecer <strong>WIA_IPS_PAGES</strong> en 1 hace que un escáner procese un lado de la página.</span><span class="sxs-lookup"><span data-stu-id="576ed-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="576ed-412">Se recomienda que, si un escáner no puede examinar solo un lado de una página en modo dúplex, cambie el valor de <strong>WIA_IPS_PAGES</strong> del miembro de intervalo del miembro de intervalo de la estructura de WIA_PROPERTY_INFO a 2.</span><span class="sxs-lookup"><span data-stu-id="576ed-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="576ed-413">Este valor indica a la aplicación que debe solicitar páginas en múltiplos de dos.</span><span class="sxs-lookup"><span data-stu-id="576ed-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="576ed-414">Un valor de ALL_PAGES (= 0) significa que <em>todas</em> las páginas que están cargadas actualmente en el alimentador de documentos se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="576ed-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="576ed-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-416">Contiene la configuración actual de los píxeles blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="576ed-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="576ed-417">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-418">Una aplicación Lee este valor para determinar el valor de blanco o negro (dependiendo de lo que esté haciendo la aplicación).</span><span class="sxs-lookup"><span data-stu-id="576ed-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="576ed-419">Se requiere para todos los elementos habilitados o almacenados de adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-420">No se admite para los elementos de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-421">Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="576ed-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="576ed-422">Si el dispositivo se puede establecer en un solo valor, cree un tipo de WIA_PROP_LIST y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="576ed-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="576ed-423">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-424">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-424">Value</span></span></th>
<th><span data-ttu-id="576ed-425">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="576ed-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="576ed-427">El blanco es 0 y el negro es 1.</span><span class="sxs-lookup"><span data-stu-id="576ed-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="576ed-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="576ed-429">El blanco es 1 y el negro es 0.</span><span class="sxs-lookup"><span data-stu-id="576ed-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="576ed-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-431">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-432">Indica el modo de vista previa de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="576ed-433">Una aplicación establece esta propiedad para colocar el dispositivo en modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="576ed-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="576ed-434">Esta propiedad es necesaria para los elementos WIA_CATEGORY_FLATBED y WIA_CATEGORY_FILM, opcional para el elemento de WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="576ed-435">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-436">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-437">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-437">Value</span></span></th>
<th><span data-ttu-id="576ed-438">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="576ed-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="576ed-440">La aplicación realizará un análisis final.</span><span class="sxs-lookup"><span data-stu-id="576ed-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="576ed-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="576ed-442">La aplicación realizará un examen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="576ed-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="576ed-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-444">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-445">Especifica si la imagen de vista previa existente se puede actualizar durante una vista previa de la imagen (en respuesta a un cambio en las propiedades WIA_IPA_DATATYPE o WIA_IPA_DEPTH).</span><span class="sxs-lookup"><span data-stu-id="576ed-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="576ed-446">Esta propiedad es opcional para todos los elementos habilitados para adquisición que admiten exámenes de vista previa. es decir, WIA_IPS_PREVIEW es compatible con WIA_PREVIEW_SCAN.</span><span class="sxs-lookup"><span data-stu-id="576ed-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="576ed-447">Esto incluye elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-448">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="576ed-449">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-450">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-450">Constant</span></span></th>
<th><span data-ttu-id="576ed-451">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="576ed-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="576ed-453">Es posible actualizar la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="576ed-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="576ed-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="576ed-455">Se debe ejecutar otro examen de vista previa porque no es posible actualizar la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="576ed-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="576ed-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-457">Contiene la configuración de rotación actual, si está implementada.</span><span class="sxs-lookup"><span data-stu-id="576ed-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="576ed-458">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-459">Una aplicación establece esta propiedad para informar al controlador de cuánto (si se desea) girar la imagen antes de que el controlador la devuelva a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="576ed-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-460">WIA_IPS_ORIENTATION hace referencia a la posición del documento que se va a examinar en la superficie del escáner o en el alimentador.</span><span class="sxs-lookup"><span data-stu-id="576ed-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="576ed-461">Es la orientación del documento con respecto a la dirección del análisis.</span><span class="sxs-lookup"><span data-stu-id="576ed-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="576ed-462">WIA_IPS_ROTATION hace referencia a la rotación que se aplica a la imagen una vez digitalizada, justo antes de que se transfiera la imagen a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="576ed-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-463">El minicontrolador WIA es responsable de rotar los datos de la imagen antes de enviarlos de nuevo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="576ed-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="576ed-464">La aplicación es responsable de comprobar los encabezados de la imagen para ver los valores que se acaban de girar.</span><span class="sxs-lookup"><span data-stu-id="576ed-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="576ed-465">Existe una gran confusión en la resolución del efecto de la rotación en el área de selección de la imagen actual (definida por las propiedades <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> ).</span><span class="sxs-lookup"><span data-stu-id="576ed-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="576ed-466">El <em>área de selección</em> hace referencia al área seleccionada en el lecho del escáner físico del que se adquiere una imagen.</span><span class="sxs-lookup"><span data-stu-id="576ed-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="576ed-467"><strong>WIA_IPS_ROTATION</strong> no modifica el área de selección.</span><span class="sxs-lookup"><span data-stu-id="576ed-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="576ed-468">El controlador aplica un giro en sentido contrario a las agujas del reloj según <strong>WIA_IPS_ROTATION</strong> solo después de que el controlador haya adquirido el área de selección adecuada.</span><span class="sxs-lookup"><span data-stu-id="576ed-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="576ed-469"><strong>WIA_IPS_ROTATION</strong> afecta a las dimensiones de la imagen de salida, por lo que estas dimensiones deben reflejarse en el encabezado de datos de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="576ed-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="576ed-470">Opcional para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-471">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="576ed-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="576ed-472">Se definen las siguientes constantes de rotación.</span><span class="sxs-lookup"><span data-stu-id="576ed-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-473">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-473">Constant</span></span></th>
<th><span data-ttu-id="576ed-474">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-475">VERTICAL</span><span class="sxs-lookup"><span data-stu-id="576ed-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="576ed-476">El controlador no rotará la imagen.</span><span class="sxs-lookup"><span data-stu-id="576ed-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-477">HORIZ</span><span class="sxs-lookup"><span data-stu-id="576ed-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="576ed-478">El controlador gira la imagen 90 grados en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="576ed-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="576ed-479">ROT180</span></span></td>
<td><span data-ttu-id="576ed-480">El controlador gira la imagen 180 grados en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="576ed-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="576ed-481">ROT270</span></span></td>
<td><span data-ttu-id="576ed-482">El controlador gira la imagen 270 grados en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="576ed-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="576ed-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-484">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-485">Especifica si la aplicación debe usar el filtro de segmentación del controlador para el examen de varias regiones.</span><span class="sxs-lookup"><span data-stu-id="576ed-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="576ed-486">WIA_IPS_SEGMENTATION debe implementarse para los elementos WIA_CATEGORY_FLATBED y WIA_CATEGORY_FILM si admiten la creación de elementos secundarios con un filtro de segmentación o si el propio controlador crea elementos secundarios para marcos fijos.</span><span class="sxs-lookup"><span data-stu-id="576ed-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="576ed-487">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="576ed-488">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-489">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-489">Value</span></span></th>
<th><span data-ttu-id="576ed-490">Definición</span><span class="sxs-lookup"><span data-stu-id="576ed-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="576ed-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="576ed-492">La aplicación debe usar el filtro de segmentación para el examen de varias regiones.</span><span class="sxs-lookup"><span data-stu-id="576ed-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="576ed-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="576ed-494">El controlador crea los propios elementos secundarios para el examen de varias regiones.</span><span class="sxs-lookup"><span data-stu-id="576ed-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="576ed-495">Este suele ser el caso si el escáner usa fotogramas fijos para este fin.</span><span class="sxs-lookup"><span data-stu-id="576ed-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-496">Es posible que un controlador incluya un filtro de segmentación, pero tenga WIA_IPS_SEGMENTATION establecido en WIA_DONT_USE_SEGMENTATION_FILTER para uno de sus elementos (por ejemplo, el elemento WIA_CATEGORY_FILM).</span><span class="sxs-lookup"><span data-stu-id="576ed-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="576ed-497">Este podría ser el caso si el escáner usa fotogramas fijos para el análisis de películas, pero no para el análisis normal de elementos WIA_CATEGORY_FLATBED.</span><span class="sxs-lookup"><span data-stu-id="576ed-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="576ed-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-499">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-500">Contiene el registro, la alineación y la detección de bordes, para los documentos que se colocan en el plano.</span><span class="sxs-lookup"><span data-stu-id="576ed-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="576ed-501">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="576ed-502">Esta propiedad indica cómo se coloca horizontalmente la hoja en el encabezado de digitalización de un escáner de mano o de alimentación de hojas.</span><span class="sxs-lookup"><span data-stu-id="576ed-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="576ed-503">La propiedad se usa para predecir dónde se coloca un documento en el encabezado del examen.</span><span class="sxs-lookup"><span data-stu-id="576ed-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="576ed-504">En el caso de los escáneres que admiten más de un encabezado de examen, esta propiedad es relativa al encabezado de examen superior.</span><span class="sxs-lookup"><span data-stu-id="576ed-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="576ed-505">Esta propiedad es obligatoria para los escáneres de alimentación de hojas, de desplazamiento y de mano.</span><span class="sxs-lookup"><span data-stu-id="576ed-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="576ed-506">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="576ed-507">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-508">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-508">Constant</span></span></th>
<th><span data-ttu-id="576ed-509">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="576ed-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="576ed-511">La hoja se coloca a la izquierda con respecto al encabezado de digitalización.</span><span class="sxs-lookup"><span data-stu-id="576ed-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-512">CENTRADO</span><span class="sxs-lookup"><span data-stu-id="576ed-512">CENTERED</span></span></td>
<td><span data-ttu-id="576ed-513">La hoja está centrada en el encabezado de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="576ed-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="576ed-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="576ed-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="576ed-515">La hoja se coloca a la derecha con respecto al encabezado de digitalización.</span><span class="sxs-lookup"><span data-stu-id="576ed-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="576ed-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-517">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-518">Indica si un elemento necesita un control de vista previa para el usuario.</span><span class="sxs-lookup"><span data-stu-id="576ed-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="576ed-519">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-520">Opcional para todos los elementos habilitados para transferencia.</span><span class="sxs-lookup"><span data-stu-id="576ed-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="576ed-521">Normalmente, se trata solo de elementos de las categorías WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM y WIA_CATEGORY_FINISHED_FILE.</span><span class="sxs-lookup"><span data-stu-id="576ed-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="576ed-522">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="576ed-523">En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="576ed-524">Constante</span><span class="sxs-lookup"><span data-stu-id="576ed-524">Constant</span></span></th>
<th><span data-ttu-id="576ed-525">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ed-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="576ed-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="576ed-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="576ed-527">Mostrar un control de vista previa al usuario, ya que este dispositivo puede realizar una vista previa.</span><span class="sxs-lookup"><span data-stu-id="576ed-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="576ed-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="576ed-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="576ed-529">No muestre un control de vista previa al usuario, ya que este dispositivo no puede realizar una vista previa.</span><span class="sxs-lookup"><span data-stu-id="576ed-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="576ed-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-531">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-532">Especifica si la aplicación (o los filtros) puede crear elementos secundarios bajo el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="576ed-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="576ed-533">Opcional para todas las categorías de elementos habilitadas para transferencia: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e incluso WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="576ed-534">(Si el almacenamiento no admite la carga de nuevos elementos, esta propiedad no se admite o no se admite con el valor <strong>false</strong> ).</span><span class="sxs-lookup"><span data-stu-id="576ed-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="576ed-535">Los elementos que admiten WIA_IPS_SEGMENTATION y WIA_USE_SEGMENTATION_FILTER también deben admitir WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION y establecerse en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="576ed-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="576ed-536">Tipo: <strong>VT_I4</strong>, Access: solo lectura, valores válidos: <strong>true</strong> y <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="576ed-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="576ed-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-538">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-539">Especifica el valor de escala de grises que determina si un píxel se convertirá en blanco o negro cuando una imagen se convierta en monocromática.</span><span class="sxs-lookup"><span data-stu-id="576ed-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="576ed-540">Los píxeles por encima del umbral se convierten en blanco.</span><span class="sxs-lookup"><span data-stu-id="576ed-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="576ed-541">Los píxeles por debajo del umbral se convierten en blanco.</span><span class="sxs-lookup"><span data-stu-id="576ed-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="576ed-542">Esta propiedad es necesaria para los elementos de adquisición que admiten exámenes de 1 BPP y que tienen la propiedad WIA_IPA_DATATYPE establecida en WIA_DATA_THRESHOLD.</span><span class="sxs-lookup"><span data-stu-id="576ed-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="576ed-543">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="576ed-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-545">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-546">Especifica si el controlador es capaz de transferir varios elementos secundarios en una sola llamada de transferencia.</span><span class="sxs-lookup"><span data-stu-id="576ed-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="576ed-547">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="576ed-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="576ed-548">El único valor posible para esta propiedad es WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span><span class="sxs-lookup"><span data-stu-id="576ed-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="576ed-549">Si se establece esta marca, el controlador es capaz de transferir varios elementos secundarios en una sola llamada de transferencia.</span><span class="sxs-lookup"><span data-stu-id="576ed-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="576ed-550">Si no se establece la marca, el servicio WIA recorrerá los elementos secundarios de forma recursiva y, a continuación, transferirá cada uno de esos elementos.</span><span class="sxs-lookup"><span data-stu-id="576ed-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="576ed-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-552">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-553">Especifica el número de bytes que se cargan para el elemento.</span><span class="sxs-lookup"><span data-stu-id="576ed-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="576ed-554">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="576ed-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-556">Especifica el tiempo de preparación máximo, en milisegundos, que necesita el dispositivo antes de iniciar la operación de examen.</span><span class="sxs-lookup"><span data-stu-id="576ed-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="576ed-557">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-558">Una aplicación puede leer esta propiedad para determinar el tiempo de preparación máximo para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="576ed-559">A continuación, puede presentar un &quot; cuadro de diálogo en espera para que el dispositivo se ponga al día &quot; , para que el usuario sepa que se puede producir una espera o una pausa antes de que ocurra algo.</span><span class="sxs-lookup"><span data-stu-id="576ed-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="576ed-560">Esta propiedad es necesaria para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-561">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="576ed-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-563">Contiene el ancho actual, en píxeles, de la imagen seleccionada que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="576ed-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="576ed-564">Una aplicación establece esta propiedad para marcar el ancho de un área de selección que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="576ed-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="576ed-565">Esta propiedad debe estar de acuerdo con la propiedad <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="576ed-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="576ed-566">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-567">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-568">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="576ed-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-570">Contiene la coordenada x, en píxeles, de la esquina superior izquierda de la imagen seleccionada.</span><span class="sxs-lookup"><span data-stu-id="576ed-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="576ed-571">Una aplicación establece esta propiedad para marcar la esquina superior izquierda del área de selección.</span><span class="sxs-lookup"><span data-stu-id="576ed-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="576ed-572">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-573">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-574">No se admite para los elementos de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-575">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="576ed-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-577">Contiene la resolución horizontal actual, en píxeles por pulgada, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="576ed-578">Una aplicación establece esta propiedad para establecer la resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="576ed-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="576ed-579">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-580">Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="576ed-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="576ed-581">También es un caso en el que un valor de resolución depende de otra resolución.</span><span class="sxs-lookup"><span data-stu-id="576ed-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="576ed-582">(La resolución vertical puede depender de la resolución horizontal).</span><span class="sxs-lookup"><span data-stu-id="576ed-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="576ed-583">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-584">No se admite para los elementos de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-585">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="576ed-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="576ed-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-587">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-588">Establece el escalado horizontal, en forma de porcentaje, que se puede aplicar a las imágenes digitalizadas en el dispositivo del escáner o en su controlador.</span><span class="sxs-lookup"><span data-stu-id="576ed-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="576ed-589">Esta propiedad es opcional para todos los elementos habilitados para adquisición; es decir, elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-590">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="576ed-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="576ed-591">Los valores pueden estar comprendidos entre 1 y el VT_I4 máximo (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="576ed-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="576ed-592">Por ejemplo, 100 significa que no hay escala, 050 significa que se va a reducir el tamaño hasta el 50% del tamaño de original, y 200 significa que se va a escalar hasta un máximo del 200% del tamaño original.</span><span class="sxs-lookup"><span data-stu-id="576ed-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="576ed-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-594">Contiene el alto actual, en píxeles, de la imagen seleccionada que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="576ed-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="576ed-595">Una aplicación establece esta propiedad para marcar el alto de un área de selección.</span><span class="sxs-lookup"><span data-stu-id="576ed-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="576ed-596">Esta propiedad debe estar de acuerdo con el valor de la propiedad <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="576ed-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="576ed-597">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-598">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-599">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="576ed-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-601">Coordenada y actual, en píxeles, de la esquina superior izquierda de la imagen seleccionada.</span><span class="sxs-lookup"><span data-stu-id="576ed-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="576ed-602">Una aplicación establece esta propiedad para marcar la esquina superior izquierda del área de selección.</span><span class="sxs-lookup"><span data-stu-id="576ed-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="576ed-603">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-604">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-605">No se admite para los elementos de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-606">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="576ed-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="576ed-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="576ed-608">Contiene la resolución vertical actual, en píxeles por pulgada, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="576ed-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="576ed-609">Una aplicación establece esta propiedad para establecer la resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="576ed-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="576ed-610">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="576ed-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="576ed-611">Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo y coloque el valor válido en él.</span><span class="sxs-lookup"><span data-stu-id="576ed-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="576ed-612">También es un caso en el que un valor de resolución depende de otra resolución.</span><span class="sxs-lookup"><span data-stu-id="576ed-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="576ed-613">(La resolución horizontal puede depender de la resolución vertical).</span><span class="sxs-lookup"><span data-stu-id="576ed-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="576ed-614">Obligatorio para todos los elementos habilitados para adquisición; es decir, los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="576ed-615">No se admite para los elementos de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="576ed-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="576ed-616">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="576ed-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="576ed-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="576ed-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="576ed-618">Esta propiedad solo es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="576ed-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="576ed-619">Establece el escalado vertical, en forma de porcentaje, que se puede aplicar a las imágenes digitalizadas en el dispositivo del escáner o en su controlador.</span><span class="sxs-lookup"><span data-stu-id="576ed-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="576ed-620">Esta propiedad es opcional para todos los elementos habilitados para adquisición; es decir, elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="576ed-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="576ed-621">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="576ed-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="576ed-622">Los valores pueden estar comprendidos entre 1 y el VT_I4 máximo (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="576ed-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="576ed-623">Por ejemplo, 100 significa que no hay escala, 050 significa que se va a reducir el tamaño hasta el 50% del tamaño de original, y 200 significa que se va a escalar hasta un máximo del 200% del tamaño original.</span><span class="sxs-lookup"><span data-stu-id="576ed-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="576ed-624">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576ed-624">Requirements</span></span>



| <span data-ttu-id="576ed-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="576ed-625">Requirement</span></span> | <span data-ttu-id="576ed-626">Value</span><span class="sxs-lookup"><span data-stu-id="576ed-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="576ed-627">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576ed-627">Minimum supported client</span></span><br/> | <span data-ttu-id="576ed-628">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="576ed-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="576ed-629">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576ed-629">Minimum supported server</span></span><br/> | <span data-ttu-id="576ed-630">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="576ed-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="576ed-631">Encabezado</span><span class="sxs-lookup"><span data-stu-id="576ed-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="576ed-632"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="576ed-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




