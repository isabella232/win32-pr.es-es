---
description: En la lista siguiente se proporcionan descripciones de los elementos de propiedad admitidos por GDI+ de Windows.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descripciones de elementos de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636127"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="2fef2-103">Descripciones de elementos de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-103">Property Item Descriptions</span></span>

<span data-ttu-id="2fef2-104">En la lista siguiente se proporcionan descripciones de los elementos de propiedad admitidos por GDI+ de Windows.</span><span class="sxs-lookup"><span data-stu-id="2fef2-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="2fef2-105">Las descripciones son breves y generales para que se apliquen a una variedad de formatos de archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="2fef2-106">Para obtener una descripción detallada de cómo se usa un elemento de propiedad en un formato de archivo determinado, vea la especificación de ese formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="2fef2-107">Para obtener vínculos a varias especificaciones de archivo y otros documentos que describen los metadatos en detalle, vea [Especificaciones de formato de archivo de imagen](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="2fef2-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="2fef2-108">El formato de archivo de imagen intercambiable (EXIF) es un estándar de la Asociación de desarrollo en el sector electrónico (JEIDA) de Japón, revisado el 1998 de junio como versión 2,1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="2fef2-109">Las partes de la especificación EXIF se usan con el permiso de JEIDA.</span><span class="sxs-lookup"><span data-stu-id="2fef2-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="2fef2-110">PropertyTagGpsVer</span><span class="sxs-lookup"><span data-stu-id="2fef2-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="2fef2-111">Versión de la IFD del sistema de posicionamiento global (GPS), proporcionada como 2.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="2fef2-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="2fef2-112">Esta etiqueta es obligatoria cuando la etiqueta PropertyTagGpsIFD está presente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="2fef2-113">Cuando la versión es 2.0.0.0, el valor de la etiqueta es 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="2fef2-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="2fef2-114">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-114">Property info</span></span> | <span data-ttu-id="2fef2-115">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-116">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-116">Tag</span></span>   | <span data-ttu-id="2fef2-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="2fef2-117">0x0000</span></span>              |
| <span data-ttu-id="2fef2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-118">Type</span></span>  | <span data-ttu-id="2fef2-119">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-120">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-120">Count</span></span> | <span data-ttu-id="2fef2-121">4</span><span class="sxs-lookup"><span data-stu-id="2fef2-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="2fef2-122">PropertyTagGpsLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="2fef2-123">Cadena de caracteres terminada en null que especifica si la latitud es North o South.</span><span class="sxs-lookup"><span data-stu-id="2fef2-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="2fef2-124">`N` especifica North latitud y `S` especifica South latitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="2fef2-125">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-125">Property info</span></span> | <span data-ttu-id="2fef2-126">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-127">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-127">Tag</span></span>   | <span data-ttu-id="2fef2-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="2fef2-128">0x0001</span></span>                                     |
| <span data-ttu-id="2fef2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-129">Type</span></span>  | <span data-ttu-id="2fef2-130">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-131">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-131">Count</span></span> | <span data-ttu-id="2fef2-132">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="2fef2-133">PropertyTagGpsLatitude</span><span class="sxs-lookup"><span data-stu-id="2fef2-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="2fef2-134">Latitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-134">Latitude.</span></span> <span data-ttu-id="2fef2-135">La latitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="2fef2-136">Cuando se expresan los grados, los minutos y los segundos, el formato es DD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="2fef2-137">Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="2fef2-138">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-138">Property info</span></span> | <span data-ttu-id="2fef2-139">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-140">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-140">Tag</span></span>   | <span data-ttu-id="2fef2-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="2fef2-141">0x0002</span></span>                  |
| <span data-ttu-id="2fef2-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-142">Type</span></span>  | <span data-ttu-id="2fef2-143">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-144">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-144">Count</span></span> | <span data-ttu-id="2fef2-145">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="2fef2-146">PropertyTagGpsLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="2fef2-147">Cadena de caracteres terminada en null que especifica si la longitud es East o West longitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="2fef2-148">`E` Especifica la longitud del este y `W` especifica la longitud oeste.</span><span class="sxs-lookup"><span data-stu-id="2fef2-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="2fef2-149">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-149">Property info</span></span> | <span data-ttu-id="2fef2-150">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-151">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-151">Tag</span></span>   | <span data-ttu-id="2fef2-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="2fef2-152">0x0003</span></span>                                     |
| <span data-ttu-id="2fef2-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-153">Type</span></span>  | <span data-ttu-id="2fef2-154">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-155">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-155">Count</span></span> | <span data-ttu-id="2fef2-156">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="2fef2-157">PropertyTagGpsLongitude</span><span class="sxs-lookup"><span data-stu-id="2fef2-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="2fef2-158">Longitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-158">Longitude.</span></span> <span data-ttu-id="2fef2-159">La longitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="2fef2-160">Cuando se expresan grados, minutos y segundos, el formato es DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="2fef2-161">Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="2fef2-162">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-162">Property info</span></span> | <span data-ttu-id="2fef2-163">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-164">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-164">Tag</span></span>   | <span data-ttu-id="2fef2-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="2fef2-165">0x0004</span></span>                  |
| <span data-ttu-id="2fef2-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-166">Type</span></span>  | <span data-ttu-id="2fef2-167">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-168">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-168">Count</span></span> | <span data-ttu-id="2fef2-169">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="2fef2-170">PropertyTagGpsAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="2fef2-171">Altitud de referencia, en metros.</span><span class="sxs-lookup"><span data-stu-id="2fef2-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="2fef2-172">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-172">Property info</span></span> | <span data-ttu-id="2fef2-173">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-174">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-174">Tag</span></span>   | <span data-ttu-id="2fef2-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="2fef2-175">0x0005</span></span>              |
| <span data-ttu-id="2fef2-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-176">Type</span></span>  | <span data-ttu-id="2fef2-177">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-178">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-178">Count</span></span> | <span data-ttu-id="2fef2-179">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="2fef2-180">PropertyTagGpsAltitude</span><span class="sxs-lookup"><span data-stu-id="2fef2-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="2fef2-181">Altitud, en metros, en función de la altitud de referencia especificada por PropertyTagGpsAltitudeRef.</span><span class="sxs-lookup"><span data-stu-id="2fef2-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="2fef2-182">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-182">Property info</span></span> | <span data-ttu-id="2fef2-183">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-184">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-184">Tag</span></span>   | <span data-ttu-id="2fef2-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="2fef2-185">0x0006</span></span>                  |
| <span data-ttu-id="2fef2-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-186">Type</span></span>  | <span data-ttu-id="2fef2-187">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-188">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-188">Count</span></span> | <span data-ttu-id="2fef2-189">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="2fef2-190">PropertyTagGpsGpsTime</span><span class="sxs-lookup"><span data-stu-id="2fef2-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="2fef2-191">Hora en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="2fef2-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2fef2-192">El valor se expresa como tres números racionales que proporcionan la hora, el minuto y el segundo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="2fef2-193">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-193">Property info</span></span> | <span data-ttu-id="2fef2-194">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-195">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-195">Tag</span></span>   | <span data-ttu-id="2fef2-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="2fef2-196">0x0007</span></span>                  |
| <span data-ttu-id="2fef2-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-197">Type</span></span>  | <span data-ttu-id="2fef2-198">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-199">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-199">Count</span></span> | <span data-ttu-id="2fef2-200">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="2fef2-201">PropertyTagGpsGpsSatellites</span><span class="sxs-lookup"><span data-stu-id="2fef2-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="2fef2-202">Cadena de caracteres terminada en null que especifica los satélites de GPS usados para las mediciones.</span><span class="sxs-lookup"><span data-stu-id="2fef2-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="2fef2-203">Esta etiqueta se puede usar para especificar el número de identificación, el ángulo de elevación, Azimuth, SNR y otra información sobre cada satélite.</span><span class="sxs-lookup"><span data-stu-id="2fef2-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="2fef2-204">No se ha especificado el formato.</span><span class="sxs-lookup"><span data-stu-id="2fef2-204">The format is not specified.</span></span> <span data-ttu-id="2fef2-205">Si el receptor de GPS no es capaz de tomar medidas, el valor de la etiqueta debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="2fef2-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="2fef2-206">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-206">Property info</span></span> | <span data-ttu-id="2fef2-207">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-208">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-208">Tag</span></span>   | <span data-ttu-id="2fef2-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="2fef2-209">0x0008</span></span>                                             |
| <span data-ttu-id="2fef2-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-210">Type</span></span>  | <span data-ttu-id="2fef2-211">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-212">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-212">Count</span></span> | <span data-ttu-id="2fef2-213">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="2fef2-214">PropertyTagGpsGpsStatus</span><span class="sxs-lookup"><span data-stu-id="2fef2-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="2fef2-215">Cadena de caracteres terminada en null que especifica el estado del receptor de GPS cuando se graba la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="2fef2-216">`A` significa que la medida está en curso y `V` significa que la medida es la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="2fef2-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="2fef2-217">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-217">Property info</span></span> | <span data-ttu-id="2fef2-218">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-219">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-219">Tag</span></span>   | <span data-ttu-id="2fef2-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="2fef2-220">0x0009</span></span>                                     |
| <span data-ttu-id="2fef2-221">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-221">Type</span></span>  | <span data-ttu-id="2fef2-222">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-223">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-223">Count</span></span> | <span data-ttu-id="2fef2-224">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="2fef2-225">PropertyTagGpsGpsMeasureMode</span><span class="sxs-lookup"><span data-stu-id="2fef2-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="2fef2-226">Cadena de caracteres terminada en null que especifica el modo de medición del GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="2fef2-227">`2` Especifica la medida 2D y `3` especifica la medida 3D.</span><span class="sxs-lookup"><span data-stu-id="2fef2-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="2fef2-228">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-228">Property info</span></span> | <span data-ttu-id="2fef2-229">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-230">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-230">Tag</span></span>   | <span data-ttu-id="2fef2-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="2fef2-231">0x000A</span></span>                                     |
| <span data-ttu-id="2fef2-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-232">Type</span></span>  | <span data-ttu-id="2fef2-233">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-234">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-234">Count</span></span> | <span data-ttu-id="2fef2-235">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="2fef2-236">PropertyTagGpsGpsDop</span><span class="sxs-lookup"><span data-stu-id="2fef2-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="2fef2-237">GPS DOP (grado de datos de precisión).</span><span class="sxs-lookup"><span data-stu-id="2fef2-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="2fef2-238">Un valor HDOP se escribe durante la medida 2D y se escribe un valor PDOP durante la medida 3D.</span><span class="sxs-lookup"><span data-stu-id="2fef2-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="2fef2-239">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-239">Property info</span></span> | <span data-ttu-id="2fef2-240">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-241">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-241">Tag</span></span>   | <span data-ttu-id="2fef2-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="2fef2-242">0x000B</span></span>                  |
| <span data-ttu-id="2fef2-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-243">Type</span></span>  | <span data-ttu-id="2fef2-244">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-245">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-245">Count</span></span> | <span data-ttu-id="2fef2-246">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="2fef2-247">PropertyTagGpsSpeedRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="2fef2-248">Cadena de caracteres terminada en null que especifica la unidad utilizada para expresar la velocidad de movimiento del receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="2fef2-249">`K`, `M` y `N` representan kilómetros por hora, kilómetros por hora y nudos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="2fef2-250">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-250">Property info</span></span> | <span data-ttu-id="2fef2-251">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-252">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-252">Tag</span></span>   | <span data-ttu-id="2fef2-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="2fef2-253">0x000C</span></span>                                     |
| <span data-ttu-id="2fef2-254">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-254">Type</span></span>  | <span data-ttu-id="2fef2-255">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-256">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-256">Count</span></span> | <span data-ttu-id="2fef2-257">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="2fef2-258">PropertyTagGpsSpeed</span><span class="sxs-lookup"><span data-stu-id="2fef2-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="2fef2-259">Velocidad del movimiento del receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="2fef2-260">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-260">Property info</span></span> | <span data-ttu-id="2fef2-261">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-262">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-262">Tag</span></span>   | <span data-ttu-id="2fef2-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="2fef2-263">0x000D</span></span>                  |
| <span data-ttu-id="2fef2-264">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-264">Type</span></span>  | <span data-ttu-id="2fef2-265">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-266">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-266">Count</span></span> | <span data-ttu-id="2fef2-267">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="2fef2-268">PropertyTagGpsTrackRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="2fef2-269">Cadena de caracteres terminada en null que especifica la referencia para ofrecer la dirección del movimiento del receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="2fef2-270">`T` Especifica la dirección verdadera y `M` especifica la dirección magnética.</span><span class="sxs-lookup"><span data-stu-id="2fef2-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="2fef2-271">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-271">Property info</span></span> | <span data-ttu-id="2fef2-272">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-273">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-273">Tag</span></span>   | <span data-ttu-id="2fef2-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="2fef2-274">0x000E</span></span>                                     |
| <span data-ttu-id="2fef2-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-275">Type</span></span>  | <span data-ttu-id="2fef2-276">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-277">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-277">Count</span></span> | <span data-ttu-id="2fef2-278">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="2fef2-279">PropertyTagGpsTrack</span><span class="sxs-lookup"><span data-stu-id="2fef2-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="2fef2-280">Dirección del movimiento del receptor de GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="2fef2-281">El intervalo de valores está comprendido entre 0,00 y 359,99.</span><span class="sxs-lookup"><span data-stu-id="2fef2-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="2fef2-282">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-282">Property info</span></span> | <span data-ttu-id="2fef2-283">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-284">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-284">Tag</span></span>   | <span data-ttu-id="2fef2-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="2fef2-285">0x000F</span></span>                  |
| <span data-ttu-id="2fef2-286">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-286">Type</span></span>  | <span data-ttu-id="2fef2-287">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-288">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-288">Count</span></span> | <span data-ttu-id="2fef2-289">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="2fef2-290">PropertyTagGpsImgDirRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="2fef2-291">Cadena de caracteres terminada en null que especifica la referencia para la dirección de la imagen cuando se captura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="2fef2-292">`T` Especifica la dirección verdadera y `M` especifica la dirección magnética.</span><span class="sxs-lookup"><span data-stu-id="2fef2-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="2fef2-293">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-293">Property info</span></span> | <span data-ttu-id="2fef2-294">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-295">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-295">Tag</span></span>   | <span data-ttu-id="2fef2-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="2fef2-296">0x0010</span></span>                                     |
| <span data-ttu-id="2fef2-297">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-297">Type</span></span>  | <span data-ttu-id="2fef2-298">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-299">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-299">Count</span></span> | <span data-ttu-id="2fef2-300">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="2fef2-301">PropertyTagGpsImgDir</span><span class="sxs-lookup"><span data-stu-id="2fef2-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="2fef2-302">Dirección de la imagen cuando se capturó.</span><span class="sxs-lookup"><span data-stu-id="2fef2-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="2fef2-303">El intervalo de valores está comprendido entre 0,00 y 359,99.</span><span class="sxs-lookup"><span data-stu-id="2fef2-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="2fef2-304">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-304">Property info</span></span> | <span data-ttu-id="2fef2-305">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-306">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-306">Tag</span></span>   | <span data-ttu-id="2fef2-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="2fef2-307">0x0011</span></span>                  |
| <span data-ttu-id="2fef2-308">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-308">Type</span></span>  | <span data-ttu-id="2fef2-309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-310">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-310">Count</span></span> | <span data-ttu-id="2fef2-311">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="2fef2-312">PropertyTagGpsMapDatum</span><span class="sxs-lookup"><span data-stu-id="2fef2-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="2fef2-313">Cadena de caracteres terminada en null que especifica los datos de encuesta de geodésico utilizados por el receptor de GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="2fef2-314">Si los datos de la encuesta están restringidos a Japón, el valor de esta etiqueta es `TOKYO` o `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="2fef2-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="2fef2-315">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-315">Property info</span></span> | <span data-ttu-id="2fef2-316">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-317">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-317">Tag</span></span>   | <span data-ttu-id="2fef2-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="2fef2-318">0x0012</span></span>                                             |
| <span data-ttu-id="2fef2-319">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-319">Type</span></span>  | <span data-ttu-id="2fef2-320">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-321">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-321">Count</span></span> | <span data-ttu-id="2fef2-322">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="2fef2-323">PropertyTagGpsDestLatRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="2fef2-324">Cadena de caracteres terminada en null que especifica si la latitud del punto de destino es North o South latitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="2fef2-325">`N` especifica North latitud y `S` especifica South latitud.</span><span class="sxs-lookup"><span data-stu-id="2fef2-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="2fef2-326">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-326">Property info</span></span> | <span data-ttu-id="2fef2-327">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-328">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-328">Tag</span></span>   | <span data-ttu-id="2fef2-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="2fef2-329">0x0013</span></span>                                     |
| <span data-ttu-id="2fef2-330">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-330">Type</span></span>  | <span data-ttu-id="2fef2-331">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-332">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-332">Count</span></span> | <span data-ttu-id="2fef2-333">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="2fef2-334">PropertyTagGpsDestLat</span><span class="sxs-lookup"><span data-stu-id="2fef2-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="2fef2-335">Latitud del punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-335">Latitude of the destination point.</span></span> <span data-ttu-id="2fef2-336">La latitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="2fef2-337">Cuando se expresan los grados, los minutos y los segundos, el formato es DD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="2fef2-338">Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="2fef2-339">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-339">Property info</span></span> | <span data-ttu-id="2fef2-340">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-341">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-341">Tag</span></span>   | <span data-ttu-id="2fef2-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="2fef2-342">0x0014</span></span>                  |
| <span data-ttu-id="2fef2-343">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-343">Type</span></span>  | <span data-ttu-id="2fef2-344">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-345">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-345">Count</span></span> | <span data-ttu-id="2fef2-346">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="2fef2-347">PropertyTagGpsDestLongRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="2fef2-348">Cadena de caracteres terminada en null que especifica si la longitud del punto de destino es la longitud oriental o oeste.</span><span class="sxs-lookup"><span data-stu-id="2fef2-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="2fef2-349">`E` Especifica la longitud del este y `W` especifica la longitud oeste.</span><span class="sxs-lookup"><span data-stu-id="2fef2-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="2fef2-350">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-350">Property info</span></span> | <span data-ttu-id="2fef2-351">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-352">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-352">Tag</span></span>   | <span data-ttu-id="2fef2-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="2fef2-353">0x0015</span></span>                                     |
| <span data-ttu-id="2fef2-354">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-354">Type</span></span>  | <span data-ttu-id="2fef2-355">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-356">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-356">Count</span></span> | <span data-ttu-id="2fef2-357">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="2fef2-358">PropertyTagGpsDestLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="2fef2-359">Longitud del punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-359">Longitude of the destination point.</span></span> <span data-ttu-id="2fef2-360">La longitud se expresa como tres valores racionales que proporcionan los grados, los minutos y los segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="2fef2-361">Cuando se expresan los grados, los minutos y los segundos, el formato es DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="2fef2-362">Cuando se usan grados y minutos y, por ejemplo, las fracciones de minutos se asignan hasta dos posiciones decimales, el formato es DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="2fef2-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="2fef2-363">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-363">Property info</span></span> | <span data-ttu-id="2fef2-364">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-365">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-365">Tag</span></span>   | <span data-ttu-id="2fef2-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="2fef2-366">0x0016</span></span>                  |
| <span data-ttu-id="2fef2-367">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-367">Type</span></span>  | <span data-ttu-id="2fef2-368">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-369">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-369">Count</span></span> | <span data-ttu-id="2fef2-370">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="2fef2-371">PropertyTagGpsDestBearRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="2fef2-372">Cadena de caracteres terminada en null que especifica la referencia usada para asignar el cojinete al punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="2fef2-373">`T` Especifica la dirección verdadera y `M` especifica la dirección magnética.</span><span class="sxs-lookup"><span data-stu-id="2fef2-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="2fef2-374">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-374">Property info</span></span> | <span data-ttu-id="2fef2-375">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-376">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-376">Tag</span></span>   | <span data-ttu-id="2fef2-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="2fef2-377">0x0017</span></span>                                     |
| <span data-ttu-id="2fef2-378">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-378">Type</span></span>  | <span data-ttu-id="2fef2-379">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-380">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-380">Count</span></span> | <span data-ttu-id="2fef2-381">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="2fef2-382">PropertyTagGpsDestBear</span><span class="sxs-lookup"><span data-stu-id="2fef2-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="2fef2-383">Cojinete hasta el punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-383">Bearing to the destination point.</span></span> <span data-ttu-id="2fef2-384">El intervalo de valores está comprendido entre 0,00 y 359,99.</span><span class="sxs-lookup"><span data-stu-id="2fef2-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="2fef2-385">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-385">Property info</span></span> | <span data-ttu-id="2fef2-386">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-387">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-387">Tag</span></span>   | <span data-ttu-id="2fef2-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="2fef2-388">0x0018</span></span>                  |
| <span data-ttu-id="2fef2-389">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-389">Type</span></span>  | <span data-ttu-id="2fef2-390">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-391">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-391">Count</span></span> | <span data-ttu-id="2fef2-392">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="2fef2-393">PropertyTagGpsDestDistRef</span><span class="sxs-lookup"><span data-stu-id="2fef2-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="2fef2-394">Cadena de caracteres terminada en null que especifica la unidad utilizada para expresar la distancia al punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="2fef2-395">K, M y N representan kilómetros, millas y nudos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="2fef2-396">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-396">Property info</span></span> | <span data-ttu-id="2fef2-397">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="2fef2-398">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-398">Tag</span></span>   | <span data-ttu-id="2fef2-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="2fef2-399">0x0019</span></span>                                     |
| <span data-ttu-id="2fef2-400">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-400">Type</span></span>  | <span data-ttu-id="2fef2-401">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="2fef2-402">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-402">Count</span></span> | <span data-ttu-id="2fef2-403">2 (un carácter más el terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="2fef2-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="2fef2-404">PropertyTagGpsDestDist</span><span class="sxs-lookup"><span data-stu-id="2fef2-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="2fef2-405">Distancia al punto de destino.</span><span class="sxs-lookup"><span data-stu-id="2fef2-405">Distance to the destination point.</span></span>



| <span data-ttu-id="2fef2-406">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-406">Property info</span></span> | <span data-ttu-id="2fef2-407">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-408">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-408">Tag</span></span>   | <span data-ttu-id="2fef2-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="2fef2-409">0x001A</span></span>                  |
| <span data-ttu-id="2fef2-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-410">Type</span></span>  | <span data-ttu-id="2fef2-411">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-412">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-412">Count</span></span> | <span data-ttu-id="2fef2-413">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="2fef2-414">PropertyTagNewSubfileType</span><span class="sxs-lookup"><span data-stu-id="2fef2-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="2fef2-415">Tipo de datos de un subarchivo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="2fef2-416">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-416">Property info</span></span> | <span data-ttu-id="2fef2-417">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-418">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-418">Tag</span></span>   | <span data-ttu-id="2fef2-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="2fef2-419">0x00FE</span></span>              |
| <span data-ttu-id="2fef2-420">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-420">Type</span></span>  | <span data-ttu-id="2fef2-421">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-422">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-422">Count</span></span> | <span data-ttu-id="2fef2-423">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="2fef2-424">PropertyTagSubfileType</span><span class="sxs-lookup"><span data-stu-id="2fef2-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="2fef2-425">Tipo de datos de un subarchivo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="2fef2-426">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-426">Property info</span></span> | <span data-ttu-id="2fef2-427">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-428">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-428">Tag</span></span>   | <span data-ttu-id="2fef2-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="2fef2-429">0x00FF</span></span>               |
| <span data-ttu-id="2fef2-430">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-430">Type</span></span>  | <span data-ttu-id="2fef2-431">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-432">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-432">Count</span></span> | <span data-ttu-id="2fef2-433">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="2fef2-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="2fef2-435">Número de píxeles por fila.</span><span class="sxs-lookup"><span data-stu-id="2fef2-435">Number of pixels per row.</span></span>



| <span data-ttu-id="2fef2-436">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-436">Property info</span></span> | <span data-ttu-id="2fef2-437">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-438">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-438">Tag</span></span>   | <span data-ttu-id="2fef2-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="2fef2-439">0x0100</span></span>                                      |
| <span data-ttu-id="2fef2-440">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-440">Type</span></span>  | <span data-ttu-id="2fef2-441">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-442">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-442">Count</span></span> | <span data-ttu-id="2fef2-443">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="2fef2-444">PropertyTagImageHeight</span><span class="sxs-lookup"><span data-stu-id="2fef2-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="2fef2-445">Número de filas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2fef2-445">Number of pixel rows.</span></span>



| <span data-ttu-id="2fef2-446">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-446">Property info</span></span> | <span data-ttu-id="2fef2-447">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-448">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-448">Tag</span></span>   | <span data-ttu-id="2fef2-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="2fef2-449">0x0101</span></span>                                      |
| <span data-ttu-id="2fef2-450">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-450">Type</span></span>  | <span data-ttu-id="2fef2-451">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-452">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-452">Count</span></span> | <span data-ttu-id="2fef2-453">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="2fef2-454">PropertyTagBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="2fef2-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="2fef2-455">Número de bits por componente de color.</span><span class="sxs-lookup"><span data-stu-id="2fef2-455">Number of bits per color component.</span></span> <span data-ttu-id="2fef2-456">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-457">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-457">Property info</span></span> | <span data-ttu-id="2fef2-458">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-459">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-459">Tag</span></span>   | <span data-ttu-id="2fef2-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="2fef2-460">0x0102</span></span>                                   |
| <span data-ttu-id="2fef2-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-461">Type</span></span>  | <span data-ttu-id="2fef2-462">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-463">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-463">Count</span></span> | <span data-ttu-id="2fef2-464">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="2fef2-465">PropertyTagCompression</span><span class="sxs-lookup"><span data-stu-id="2fef2-465">PropertyTagCompression</span></span>

<span data-ttu-id="2fef2-466">Esquema de compresión utilizado para los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="2fef2-467">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-467">Property info</span></span> | <span data-ttu-id="2fef2-468">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-469">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-469">Tag</span></span>   | <span data-ttu-id="2fef2-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="2fef2-470">0x0103</span></span>               |
| <span data-ttu-id="2fef2-471">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-471">Type</span></span>  | <span data-ttu-id="2fef2-472">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-473">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-473">Count</span></span> | <span data-ttu-id="2fef2-474">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="2fef2-475">PropertyTagPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="2fef2-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="2fef2-476">Cómo se interpretarán los datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2fef2-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="2fef2-477">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-477">Property info</span></span> | <span data-ttu-id="2fef2-478">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-479">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-479">Tag</span></span>   | <span data-ttu-id="2fef2-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="2fef2-480">0x0106</span></span>               |
| <span data-ttu-id="2fef2-481">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-481">Type</span></span>  | <span data-ttu-id="2fef2-482">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-483">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-483">Count</span></span> | <span data-ttu-id="2fef2-484">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="2fef2-485">PropertyTagThreshHolding</span><span class="sxs-lookup"><span data-stu-id="2fef2-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="2fef2-486">Técnica usada para convertir de píxeles grises a píxeles negros y blancos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="2fef2-487">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-487">Property info</span></span> | <span data-ttu-id="2fef2-488">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-489">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-489">Tag</span></span>   | <span data-ttu-id="2fef2-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="2fef2-490">0x0107</span></span>               |
| <span data-ttu-id="2fef2-491">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-491">Type</span></span>  | <span data-ttu-id="2fef2-492">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-493">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-493">Count</span></span> | <span data-ttu-id="2fef2-494">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="2fef2-495">PropertyTagCellWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="2fef2-496">Ancho de la matriz de tramas o semitonos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="2fef2-497">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-497">Property info</span></span> | <span data-ttu-id="2fef2-498">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-499">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-499">Tag</span></span>   | <span data-ttu-id="2fef2-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="2fef2-500">0x0108</span></span>               |
| <span data-ttu-id="2fef2-501">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-501">Type</span></span>  | <span data-ttu-id="2fef2-502">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-503">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-503">Count</span></span> | <span data-ttu-id="2fef2-504">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="2fef2-505">PropertyTagCellHeight</span><span class="sxs-lookup"><span data-stu-id="2fef2-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="2fef2-506">Alto de la matriz de tramas o semitonos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="2fef2-507">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-507">Property info</span></span> | <span data-ttu-id="2fef2-508">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-509">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-509">Tag</span></span>   | <span data-ttu-id="2fef2-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="2fef2-510">0x0109</span></span>               |
| <span data-ttu-id="2fef2-511">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-511">Type</span></span>  | <span data-ttu-id="2fef2-512">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-513">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-513">Count</span></span> | <span data-ttu-id="2fef2-514">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="2fef2-515">PropertyTagFillOrder</span><span class="sxs-lookup"><span data-stu-id="2fef2-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="2fef2-516">Orden lógico de bits en bytes.</span><span class="sxs-lookup"><span data-stu-id="2fef2-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="2fef2-517">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-517">Property info</span></span> | <span data-ttu-id="2fef2-518">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-519">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-519">Tag</span></span>   | <span data-ttu-id="2fef2-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="2fef2-520">0x010A</span></span>               |
| <span data-ttu-id="2fef2-521">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-521">Type</span></span>  | <span data-ttu-id="2fef2-522">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-523">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-523">Count</span></span> | <span data-ttu-id="2fef2-524">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="2fef2-525">PropertyTagDocumentName</span><span class="sxs-lookup"><span data-stu-id="2fef2-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="2fef2-526">Cadena de caracteres terminada en null que especifica el nombre del documento desde el que se examinó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="2fef2-527">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-527">Property info</span></span> | <span data-ttu-id="2fef2-528">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-529">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-529">Tag</span></span>   | <span data-ttu-id="2fef2-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="2fef2-530">0x010D</span></span>                                             |
| <span data-ttu-id="2fef2-531">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-531">Type</span></span>  | <span data-ttu-id="2fef2-532">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-533">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-533">Count</span></span> | <span data-ttu-id="2fef2-534">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="2fef2-535">PropertyTagImageDescription</span><span class="sxs-lookup"><span data-stu-id="2fef2-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="2fef2-536">Cadena de caracteres terminada en null que especifica el título de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="2fef2-537">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-537">Property info</span></span> | <span data-ttu-id="2fef2-538">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-539">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-539">Tag</span></span>   | <span data-ttu-id="2fef2-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="2fef2-540">0x010E</span></span>                                             |
| <span data-ttu-id="2fef2-541">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-541">Type</span></span>  | <span data-ttu-id="2fef2-542">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-543">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-543">Count</span></span> | <span data-ttu-id="2fef2-544">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="2fef2-545">PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="2fef2-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="2fef2-546">Cadena de caracteres terminada en null que especifica el fabricante del equipo usado para grabar la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="2fef2-547">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-547">Property info</span></span> | <span data-ttu-id="2fef2-548">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-549">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-549">Tag</span></span>   | <span data-ttu-id="2fef2-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="2fef2-550">0x010F</span></span>                                             |
| <span data-ttu-id="2fef2-551">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-551">Type</span></span>  | <span data-ttu-id="2fef2-552">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-553">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-553">Count</span></span> | <span data-ttu-id="2fef2-554">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="2fef2-555">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="2fef2-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="2fef2-556">Cadena de caracteres terminada en null que especifica el nombre del modelo o el número de modelo del equipo usado para grabar la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="2fef2-557">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-557">Property info</span></span> | <span data-ttu-id="2fef2-558">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-559">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-559">Tag</span></span>   | <span data-ttu-id="2fef2-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="2fef2-560">0x0110</span></span>                                             |
| <span data-ttu-id="2fef2-561">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-561">Type</span></span>  | <span data-ttu-id="2fef2-562">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-563">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-563">Count</span></span> | <span data-ttu-id="2fef2-564">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="2fef2-565">PropertyTagStripOffsets</span><span class="sxs-lookup"><span data-stu-id="2fef2-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="2fef2-566">Para cada franja, el desplazamiento de bytes de esa franja.</span><span class="sxs-lookup"><span data-stu-id="2fef2-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="2fef2-567">Vea también [PropertyTagRowsPerStrip](#propertytagrowsperstrip) y [PropertyTagStripBytesCount](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="2fef2-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="2fef2-568">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-568">Property info</span></span> | <span data-ttu-id="2fef2-569">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-570">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-570">Tag</span></span>   | <span data-ttu-id="2fef2-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="2fef2-571">0x0111</span></span>                                      |
| <span data-ttu-id="2fef2-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-572">Type</span></span>  | <span data-ttu-id="2fef2-573">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-574">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-574">Count</span></span> | <span data-ttu-id="2fef2-575">Número de bandas</span><span class="sxs-lookup"><span data-stu-id="2fef2-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="2fef2-576">PropertyTagOrientation</span><span class="sxs-lookup"><span data-stu-id="2fef2-576">PropertyTagOrientation</span></span>

<span data-ttu-id="2fef2-577">Orientación de imagen visualizada en términos de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="2fef2-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="2fef2-578">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-578">Tag</span></span>

<span data-ttu-id="2fef2-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="2fef2-579">0x0112</span></span>

<span data-ttu-id="2fef2-580">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-580">Type</span></span>

<span data-ttu-id="2fef2-581">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-582">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-582">Count</span></span>

<span data-ttu-id="2fef2-583">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-583">1</span></span>

<span data-ttu-id="2fef2-584">1: la fila situada en la parte superior de la imagen visual y la columna de la izquierda es el lado izquierdo del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="2fef2-585">2-la fila situada en la parte superior de la imagen y la columna 0 es el lado derecho visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="2fef2-586">3-la fila de la 0 en la parte inferior de la imagen y la columna de la derecha es el lado derecho del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="2fef2-587">4: la fila de la 0 en la parte inferior de la imagen y la columna de la izquierda es el lado izquierdo del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="2fef2-588">5: la fila de la izquierda es el lado izquierdo visual de la imagen y la columna 0 es la parte superior del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="2fef2-589">6-la fila de la derecha es el lado derecho visual de la imagen y la columna 0 es la parte superior del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="2fef2-590">7: la fila de la derecha es el lado derecho visual de la imagen y la columna de la 0 es la parte inferior del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="2fef2-591">8: la fila de la izquierda es el lado izquierdo visual de la imagen y la columna de la derecha es la parte inferior del visual.</span><span class="sxs-lookup"><span data-stu-id="2fef2-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="2fef2-592">PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="2fef2-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="2fef2-593">Número de componentes de color por píxel.</span><span class="sxs-lookup"><span data-stu-id="2fef2-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="2fef2-594">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-594">Property info</span></span> | <span data-ttu-id="2fef2-595">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-596">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-596">Tag</span></span>   | <span data-ttu-id="2fef2-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="2fef2-597">0x0115</span></span>               |
| <span data-ttu-id="2fef2-598">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-598">Type</span></span>  | <span data-ttu-id="2fef2-599">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-600">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-600">Count</span></span> | <span data-ttu-id="2fef2-601">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="2fef2-602">PropertyTagRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="2fef2-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="2fef2-603">Número de filas por franja.</span><span class="sxs-lookup"><span data-stu-id="2fef2-603">Number of rows per strip.</span></span> <span data-ttu-id="2fef2-604">Vea también [PropertyTagStripBytesCount](#propertytagstripbytescount) y [PropertyTagStripOffsets](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="2fef2-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="2fef2-605">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-605">Property info</span></span> | <span data-ttu-id="2fef2-606">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-607">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-607">Tag</span></span>   | <span data-ttu-id="2fef2-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="2fef2-608">0x0116</span></span>                                      |
| <span data-ttu-id="2fef2-609">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-609">Type</span></span>  | <span data-ttu-id="2fef2-610">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-611">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-611">Count</span></span> | <span data-ttu-id="2fef2-612">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="2fef2-613">PropertyTagStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="2fef2-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="2fef2-614">Para cada franja, el número total de bytes de esa franja.</span><span class="sxs-lookup"><span data-stu-id="2fef2-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="2fef2-615">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-615">Property info</span></span> | <span data-ttu-id="2fef2-616">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-617">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-617">Tag</span></span>   | <span data-ttu-id="2fef2-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="2fef2-618">0x0117</span></span>                                      |
| <span data-ttu-id="2fef2-619">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-619">Type</span></span>  | <span data-ttu-id="2fef2-620">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-621">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-621">Count</span></span> | <span data-ttu-id="2fef2-622">Número de bandas</span><span class="sxs-lookup"><span data-stu-id="2fef2-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="2fef2-623">PropertyTagMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="2fef2-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="2fef2-624">Para cada componente de color, el valor mínimo asignado a ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="2fef2-625">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-626">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-626">Property info</span></span> | <span data-ttu-id="2fef2-627">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-628">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-628">Tag</span></span>   | <span data-ttu-id="2fef2-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="2fef2-629">0x0118</span></span>                                   |
| <span data-ttu-id="2fef2-630">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-630">Type</span></span>  | <span data-ttu-id="2fef2-631">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-632">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-632">Count</span></span> | <span data-ttu-id="2fef2-633">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="2fef2-634">PropertyTagMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="2fef2-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="2fef2-635">Para cada componente de color, el valor máximo asignado a ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="2fef2-636">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-637">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-637">Property info</span></span> | <span data-ttu-id="2fef2-638">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-639">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-639">Tag</span></span>   | <span data-ttu-id="2fef2-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="2fef2-640">0x0119</span></span>                                   |
| <span data-ttu-id="2fef2-641">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-641">Type</span></span>  | <span data-ttu-id="2fef2-642">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-643">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-643">Count</span></span> | <span data-ttu-id="2fef2-644">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="2fef2-645">PropertyTagXResolution</span><span class="sxs-lookup"><span data-stu-id="2fef2-645">PropertyTagXResolution</span></span>

<span data-ttu-id="2fef2-646">Número de píxeles por unidad en la dirección de ancho de la imagen (x).</span><span class="sxs-lookup"><span data-stu-id="2fef2-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="2fef2-647">La unidad se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="2fef2-648">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-648">Property info</span></span> | <span data-ttu-id="2fef2-649">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-650">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-650">Tag</span></span>   | <span data-ttu-id="2fef2-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="2fef2-651">0x011A</span></span>                  |
| <span data-ttu-id="2fef2-652">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-652">Type</span></span>  | <span data-ttu-id="2fef2-653">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-654">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-654">Count</span></span> | <span data-ttu-id="2fef2-655">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="2fef2-656">PropertyTagYResolution</span><span class="sxs-lookup"><span data-stu-id="2fef2-656">PropertyTagYResolution</span></span>

<span data-ttu-id="2fef2-657">Número de píxeles por unidad en la dirección del alto de la imagen (y).</span><span class="sxs-lookup"><span data-stu-id="2fef2-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="2fef2-658">La unidad se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="2fef2-659">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-659">Property info</span></span> | <span data-ttu-id="2fef2-660">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-661">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-661">Tag</span></span>   | <span data-ttu-id="2fef2-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="2fef2-662">0x011B</span></span>                  |
| <span data-ttu-id="2fef2-663">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-663">Type</span></span>  | <span data-ttu-id="2fef2-664">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-665">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-665">Count</span></span> | <span data-ttu-id="2fef2-666">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="2fef2-667">PropertyTagPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="2fef2-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="2fef2-668">Si los componentes de píxeles se registran en formato plano o fragmentado.</span><span class="sxs-lookup"><span data-stu-id="2fef2-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="2fef2-669">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-669">Property info</span></span> | <span data-ttu-id="2fef2-670">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-671">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-671">Tag</span></span>   | <span data-ttu-id="2fef2-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="2fef2-672">0x011C</span></span>               |
| <span data-ttu-id="2fef2-673">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-673">Type</span></span>  | <span data-ttu-id="2fef2-674">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-675">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-675">Count</span></span> | <span data-ttu-id="2fef2-676">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="2fef2-677">PropertyTagPageName</span><span class="sxs-lookup"><span data-stu-id="2fef2-677">PropertyTagPageName</span></span>

<span data-ttu-id="2fef2-678">Cadena de caracteres terminada en null que especifica el nombre de la página desde la que se examinó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="2fef2-679">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-679">Property info</span></span> | <span data-ttu-id="2fef2-680">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-681">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-681">Tag</span></span>   | <span data-ttu-id="2fef2-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="2fef2-682">0x011D</span></span>                                             |
| <span data-ttu-id="2fef2-683">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-683">Type</span></span>  | <span data-ttu-id="2fef2-684">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-685">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-685">Count</span></span> | <span data-ttu-id="2fef2-686">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="2fef2-687">PropertyTagXPosition</span><span class="sxs-lookup"><span data-stu-id="2fef2-687">PropertyTagXPosition</span></span>

<span data-ttu-id="2fef2-688">Desplazamiento desde el lado izquierdo de la página hasta el lado izquierdo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="2fef2-689">La unidad de medida se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="2fef2-690">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-690">Property info</span></span> | <span data-ttu-id="2fef2-691">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-692">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-692">Tag</span></span>   | <span data-ttu-id="2fef2-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="2fef2-693">0x011E</span></span>                  |
| <span data-ttu-id="2fef2-694">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-694">Type</span></span>  | <span data-ttu-id="2fef2-695">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-696">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-696">Count</span></span> | <span data-ttu-id="2fef2-697">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="2fef2-698">PropertyTagYPosition</span><span class="sxs-lookup"><span data-stu-id="2fef2-698">PropertyTagYPosition</span></span>

<span data-ttu-id="2fef2-699">Desplazamiento desde la parte superior de la página hasta la parte superior de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="2fef2-700">La unidad de medida se especifica mediante [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="2fef2-701">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-701">Property info</span></span> | <span data-ttu-id="2fef2-702">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-703">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-703">Tag</span></span>   | <span data-ttu-id="2fef2-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="2fef2-704">0x011F</span></span>                  |
| <span data-ttu-id="2fef2-705">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-705">Type</span></span>  | <span data-ttu-id="2fef2-706">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-707">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-707">Count</span></span> | <span data-ttu-id="2fef2-708">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="2fef2-709">PropertyTagFreeOffset</span><span class="sxs-lookup"><span data-stu-id="2fef2-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="2fef2-710">Para cada cadena de bytes contiguos no utilizados, el desplazamiento de bytes de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="2fef2-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="2fef2-711">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-711">Property info</span></span> | <span data-ttu-id="2fef2-712">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="2fef2-713">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-713">Tag</span></span>  | <span data-ttu-id="2fef2-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="2fef2-714">0x0120</span></span>              |
| <span data-ttu-id="2fef2-715">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-715">Type</span></span> | <span data-ttu-id="2fef2-716">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="2fef2-717">PropertyTagFreeByteCounts</span><span class="sxs-lookup"><span data-stu-id="2fef2-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="2fef2-718">Para cada cadena de bytes contiguos no utilizados, el número de bytes de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="2fef2-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="2fef2-719">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-719">Property info</span></span> | <span data-ttu-id="2fef2-720">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="2fef2-721">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-721">Tag</span></span>   | <span data-ttu-id="2fef2-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="2fef2-722">0x0121</span></span>                                        |
| <span data-ttu-id="2fef2-723">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-723">Type</span></span>  | <span data-ttu-id="2fef2-724">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="2fef2-725">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-725">Count</span></span> | <span data-ttu-id="2fef2-726">Número de cadenas de bytes no usados contiguos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="2fef2-727">PropertyTagGrayResponseUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="2fef2-728">Precisión del número especificado por PropertyTagGrayResponseCurve.</span><span class="sxs-lookup"><span data-stu-id="2fef2-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="2fef2-729">1 especifica décimas, 2 especifica centésimas, 3 especifica milésimas, etc.</span><span class="sxs-lookup"><span data-stu-id="2fef2-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="2fef2-730">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-730">Property info</span></span> | <span data-ttu-id="2fef2-731">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-732">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-732">Tag</span></span>   | <span data-ttu-id="2fef2-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="2fef2-733">0x0122</span></span>               |
| <span data-ttu-id="2fef2-734">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-734">Type</span></span>  | <span data-ttu-id="2fef2-735">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-736">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-736">Count</span></span> | <span data-ttu-id="2fef2-737">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="2fef2-738">PropertyTagGrayResponseCurve</span><span class="sxs-lookup"><span data-stu-id="2fef2-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="2fef2-739">Para cada valor de píxel posible de una imagen de escala de grises, la densidad óptica de ese valor de píxel.</span><span class="sxs-lookup"><span data-stu-id="2fef2-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="2fef2-740">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-740">Property info</span></span> | <span data-ttu-id="2fef2-741">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="2fef2-742">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-742">Tag</span></span>   | <span data-ttu-id="2fef2-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="2fef2-743">0x0123</span></span>                          |
| <span data-ttu-id="2fef2-744">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-744">Type</span></span>  | <span data-ttu-id="2fef2-745">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="2fef2-746">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-746">Count</span></span> | <span data-ttu-id="2fef2-747">Número de valores de píxeles posibles</span><span class="sxs-lookup"><span data-stu-id="2fef2-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="2fef2-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="2fef2-748">PropertyTagT4Option</span></span>

<span data-ttu-id="2fef2-749">Conjunto de marcas relacionadas con la codificación T4.</span><span class="sxs-lookup"><span data-stu-id="2fef2-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="2fef2-750">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-750">Property info</span></span> | <span data-ttu-id="2fef2-751">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-752">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-752">Tag</span></span>   | <span data-ttu-id="2fef2-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="2fef2-753">0x0124</span></span>              |
| <span data-ttu-id="2fef2-754">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-754">Type</span></span>  | <span data-ttu-id="2fef2-755">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-756">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-756">Count</span></span> | <span data-ttu-id="2fef2-757">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="2fef2-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="2fef2-758">PropertyTagT6Option</span></span>

<span data-ttu-id="2fef2-759">Conjunto de marcas relacionadas con la codificación T6.</span><span class="sxs-lookup"><span data-stu-id="2fef2-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="2fef2-760">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-760">Property info</span></span> | <span data-ttu-id="2fef2-761">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-762">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-762">Tag</span></span>   | <span data-ttu-id="2fef2-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="2fef2-763">0x0125</span></span>              |
| <span data-ttu-id="2fef2-764">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-764">Type</span></span>  | <span data-ttu-id="2fef2-765">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-766">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-766">Count</span></span> | <span data-ttu-id="2fef2-767">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="2fef2-768">PropertyTagResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="2fef2-769">Unidad de medida para la resolución horizontal y la resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="2fef2-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="2fef2-770">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-770">Tag</span></span>

<span data-ttu-id="2fef2-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="2fef2-771">0x0128</span></span>

<span data-ttu-id="2fef2-772">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-772">Type</span></span>

<span data-ttu-id="2fef2-773">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-774">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-774">Count</span></span>

<span data-ttu-id="2fef2-775">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-775">1</span></span>

<span data-ttu-id="2fef2-776">2 pulgadas 3-centímetro</span><span class="sxs-lookup"><span data-stu-id="2fef2-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="2fef2-777">PropertyTagPageNumber</span><span class="sxs-lookup"><span data-stu-id="2fef2-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="2fef2-778">Número de página de la página desde la que se examinó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="2fef2-779">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-779">Property info</span></span> | <span data-ttu-id="2fef2-780">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-781">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-781">Tag</span></span>   | <span data-ttu-id="2fef2-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="2fef2-782">0x0129</span></span>               |
| <span data-ttu-id="2fef2-783">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-783">Type</span></span>  | <span data-ttu-id="2fef2-784">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-785">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-785">Count</span></span> | <span data-ttu-id="2fef2-786">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="2fef2-787">PropertyTagTransferFunction</span><span class="sxs-lookup"><span data-stu-id="2fef2-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="2fef2-788">Tablas que especifican funciones de transferencia para la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="2fef2-789">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-789">Property info</span></span> | <span data-ttu-id="2fef2-790">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="2fef2-791">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-791">Tag</span></span>   | <span data-ttu-id="2fef2-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="2fef2-792">0x012D</span></span>                                               |
| <span data-ttu-id="2fef2-793">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-793">Type</span></span>  | <span data-ttu-id="2fef2-794">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="2fef2-795">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-795">Count</span></span> | <span data-ttu-id="2fef2-796">Número total de palabras de 16 bits necesarias para las tablas</span><span class="sxs-lookup"><span data-stu-id="2fef2-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="2fef2-797">PropertyTagSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="2fef2-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="2fef2-798">Cadena de caracteres terminada en null que especifica el nombre y la versión del software o firmware del dispositivo usado para generar la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="2fef2-799">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-799">Property info</span></span> | <span data-ttu-id="2fef2-800">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-801">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-801">Tag</span></span>   | <span data-ttu-id="2fef2-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="2fef2-802">0x0131</span></span>                                             |
| <span data-ttu-id="2fef2-803">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-803">Type</span></span>  | <span data-ttu-id="2fef2-804">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-805">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-805">Count</span></span> | <span data-ttu-id="2fef2-806">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="2fef2-807">PropertyTagDateTime</span><span class="sxs-lookup"><span data-stu-id="2fef2-807">PropertyTagDateTime</span></span>

<span data-ttu-id="2fef2-808">Fecha y hora en que se creó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-808">Date and time the image was created.</span></span>



| <span data-ttu-id="2fef2-809">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-809">Property info</span></span> | <span data-ttu-id="2fef2-810">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-811">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-811">Tag</span></span>   | <span data-ttu-id="2fef2-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="2fef2-812">0x0132</span></span>               |
| <span data-ttu-id="2fef2-813">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-813">Type</span></span>  | <span data-ttu-id="2fef2-814">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-815">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-815">Count</span></span> | <span data-ttu-id="2fef2-816">20</span><span class="sxs-lookup"><span data-stu-id="2fef2-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="2fef2-817">PropertyTagArtist</span><span class="sxs-lookup"><span data-stu-id="2fef2-817">PropertyTagArtist</span></span>

<span data-ttu-id="2fef2-818">Cadena de caracteres terminada en null que especifica el nombre de la persona que creó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="2fef2-819">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-819">Property info</span></span> | <span data-ttu-id="2fef2-820">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-821">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-821">Tag</span></span>   | <span data-ttu-id="2fef2-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="2fef2-822">0x013B</span></span>                                             |
| <span data-ttu-id="2fef2-823">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-823">Type</span></span>  | <span data-ttu-id="2fef2-824">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-825">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-825">Count</span></span> | <span data-ttu-id="2fef2-826">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="2fef2-827">PropertyTagHostComputer</span><span class="sxs-lookup"><span data-stu-id="2fef2-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="2fef2-828">Cadena de caracteres terminada en null que especifica el equipo o sistema operativo usado para crear la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="2fef2-829">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-829">Property info</span></span> | <span data-ttu-id="2fef2-830">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-831">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-831">Tag</span></span>   | <span data-ttu-id="2fef2-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="2fef2-832">0x013C</span></span>                                             |
| <span data-ttu-id="2fef2-833">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-833">Type</span></span>  | <span data-ttu-id="2fef2-834">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-835">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-835">Count</span></span> | <span data-ttu-id="2fef2-836">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="2fef2-837">PropertyTagPredictor</span><span class="sxs-lookup"><span data-stu-id="2fef2-837">PropertyTagPredictor</span></span>

<span data-ttu-id="2fef2-838">Tipo de esquema de predicción que se aplicó a los datos de imagen antes de que se aplicara el esquema de codificación.</span><span class="sxs-lookup"><span data-stu-id="2fef2-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="2fef2-839">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-839">Property info</span></span> | <span data-ttu-id="2fef2-840">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-841">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-841">Tag</span></span>   | <span data-ttu-id="2fef2-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="2fef2-842">0x013D</span></span>               |
| <span data-ttu-id="2fef2-843">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-843">Type</span></span>  | <span data-ttu-id="2fef2-844">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-845">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-845">Count</span></span> | <span data-ttu-id="2fef2-846">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="2fef2-847">PropertyTagWhitePoint</span><span class="sxs-lookup"><span data-stu-id="2fef2-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="2fef2-848">Cromaticidad del punto blanco de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="2fef2-849">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-849">Property info</span></span> | <span data-ttu-id="2fef2-850">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-851">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-851">Tag</span></span>   | <span data-ttu-id="2fef2-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="2fef2-852">0x013E</span></span>                  |
| <span data-ttu-id="2fef2-853">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-853">Type</span></span>  | <span data-ttu-id="2fef2-854">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-855">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-855">Count</span></span> | <span data-ttu-id="2fef2-856">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="2fef2-857">PropertyTagPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="2fef2-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="2fef2-858">Para cada uno de los tres colores primarios de la imagen, la cromaticidad de ese color.</span><span class="sxs-lookup"><span data-stu-id="2fef2-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="2fef2-859">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-859">Property info</span></span> | <span data-ttu-id="2fef2-860">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-861">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-861">Tag</span></span>   | <span data-ttu-id="2fef2-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="2fef2-862">0x013F</span></span>                  |
| <span data-ttu-id="2fef2-863">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-863">Type</span></span>  | <span data-ttu-id="2fef2-864">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-865">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-865">Count</span></span> | <span data-ttu-id="2fef2-866">6</span><span class="sxs-lookup"><span data-stu-id="2fef2-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="2fef2-867">PropertyTagColorMap</span><span class="sxs-lookup"><span data-stu-id="2fef2-867">PropertyTagColorMap</span></span>

<span data-ttu-id="2fef2-868">Paleta de colores (tabla de búsqueda) para una imagen indizada en una paleta.</span><span class="sxs-lookup"><span data-stu-id="2fef2-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="2fef2-869">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-869">Property info</span></span> | <span data-ttu-id="2fef2-870">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="2fef2-871">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-871">Tag</span></span>   | <span data-ttu-id="2fef2-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="2fef2-872">0x0140</span></span>                                          |
| <span data-ttu-id="2fef2-873">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-873">Type</span></span>  | <span data-ttu-id="2fef2-874">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="2fef2-875">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-875">Count</span></span> | <span data-ttu-id="2fef2-876">Número de palabras de 16 bits necesarias para la paleta</span><span class="sxs-lookup"><span data-stu-id="2fef2-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="2fef2-877">PropertyTagHalftoneHints</span><span class="sxs-lookup"><span data-stu-id="2fef2-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="2fef2-878">Información usada por la función de semitono</span><span class="sxs-lookup"><span data-stu-id="2fef2-878">Information used by the halftone function</span></span>



| <span data-ttu-id="2fef2-879">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-879">Property info</span></span> | <span data-ttu-id="2fef2-880">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-881">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-881">Tag</span></span>   | <span data-ttu-id="2fef2-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="2fef2-882">0x0141</span></span>               |
| <span data-ttu-id="2fef2-883">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-883">Type</span></span>  | <span data-ttu-id="2fef2-884">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-885">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-885">Count</span></span> | <span data-ttu-id="2fef2-886">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="2fef2-887">PropertyTagTileWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="2fef2-888">Número de columnas de píxeles en cada mosaico.</span><span class="sxs-lookup"><span data-stu-id="2fef2-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="2fef2-889">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-889">Property info</span></span> | <span data-ttu-id="2fef2-890">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-891">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-891">Tag</span></span>   | <span data-ttu-id="2fef2-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="2fef2-892">0x0142</span></span>                                      |
| <span data-ttu-id="2fef2-893">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-893">Type</span></span>  | <span data-ttu-id="2fef2-894">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-895">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-895">Count</span></span> | <span data-ttu-id="2fef2-896">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="2fef2-897">PropertyTagTileLength</span><span class="sxs-lookup"><span data-stu-id="2fef2-897">PropertyTagTileLength</span></span>

<span data-ttu-id="2fef2-898">Número de filas de píxeles en cada mosaico.</span><span class="sxs-lookup"><span data-stu-id="2fef2-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="2fef2-899">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-899">Property info</span></span> | <span data-ttu-id="2fef2-900">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-901">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-901">Tag</span></span>   | <span data-ttu-id="2fef2-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="2fef2-902">0x0143</span></span>                                      |
| <span data-ttu-id="2fef2-903">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-903">Type</span></span>  | <span data-ttu-id="2fef2-904">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-905">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-905">Count</span></span> | <span data-ttu-id="2fef2-906">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="2fef2-907">PropertyTagTileOffset</span><span class="sxs-lookup"><span data-stu-id="2fef2-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="2fef2-908">Para cada mosaico, el desplazamiento de bytes de ese mosaico.</span><span class="sxs-lookup"><span data-stu-id="2fef2-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="2fef2-909">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-909">Property info</span></span> | <span data-ttu-id="2fef2-910">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-911">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-911">Tag</span></span>   | <span data-ttu-id="2fef2-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="2fef2-912">0x0144</span></span>              |
| <span data-ttu-id="2fef2-913">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-913">Type</span></span>  | <span data-ttu-id="2fef2-914">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-915">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-915">Count</span></span> | <span data-ttu-id="2fef2-916">Número de mosaicos</span><span class="sxs-lookup"><span data-stu-id="2fef2-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="2fef2-917">PropertyTagTileByteCounts</span><span class="sxs-lookup"><span data-stu-id="2fef2-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="2fef2-918">Para cada mosaico, el número de bytes de ese mosaico.</span><span class="sxs-lookup"><span data-stu-id="2fef2-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="2fef2-919">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-919">Property info</span></span> | <span data-ttu-id="2fef2-920">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-921">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-921">Tag</span></span>   | <span data-ttu-id="2fef2-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="2fef2-922">0x0145</span></span>                                      |
| <span data-ttu-id="2fef2-923">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-923">Type</span></span>  | <span data-ttu-id="2fef2-924">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-925">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-925">Count</span></span> | <span data-ttu-id="2fef2-926">Número de mosaicos</span><span class="sxs-lookup"><span data-stu-id="2fef2-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="2fef2-927">PropertyTagInkSet</span><span class="sxs-lookup"><span data-stu-id="2fef2-927">PropertyTagInkSet</span></span>

<span data-ttu-id="2fef2-928">Conjunto de tintas utilizadas en una imagen separada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="2fef2-929">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-929">Property info</span></span> | <span data-ttu-id="2fef2-930">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-931">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-931">Tag</span></span>   | <span data-ttu-id="2fef2-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="2fef2-932">0x014C</span></span>               |
| <span data-ttu-id="2fef2-933">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-933">Type</span></span>  | <span data-ttu-id="2fef2-934">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-935">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-935">Count</span></span> | <span data-ttu-id="2fef2-936">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="2fef2-937">PropertyTagInkNames</span><span class="sxs-lookup"><span data-stu-id="2fef2-937">PropertyTagInkNames</span></span>

<span data-ttu-id="2fef2-938">Secuencia de cadenas de caracteres concatenadas y terminadas en null que especifican los nombres de las tintas utilizadas en una imagen separada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="2fef2-939">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-939">Property info</span></span> | <span data-ttu-id="2fef2-940">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="2fef2-941">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-941">Tag</span></span>   | <span data-ttu-id="2fef2-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="2fef2-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="2fef2-943">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-943">Type</span></span>  | <span data-ttu-id="2fef2-944">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="2fef2-945">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-945">Count</span></span> | <span data-ttu-id="2fef2-946">Longitud total de la secuencia de cadenas, incluidos los terminadores NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="2fef2-947">PropertyTagNumberOfInks</span><span class="sxs-lookup"><span data-stu-id="2fef2-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="2fef2-948">Número de tintas.</span><span class="sxs-lookup"><span data-stu-id="2fef2-948">Number of inks.</span></span>



| <span data-ttu-id="2fef2-949">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-949">Property info</span></span> | <span data-ttu-id="2fef2-950">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-951">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-951">Tag</span></span>   | <span data-ttu-id="2fef2-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="2fef2-952">0x014E</span></span>               |
| <span data-ttu-id="2fef2-953">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-953">Type</span></span>  | <span data-ttu-id="2fef2-954">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-955">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-955">Count</span></span> | <span data-ttu-id="2fef2-956">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="2fef2-957">PropertyTagDotRange</span><span class="sxs-lookup"><span data-stu-id="2fef2-957">PropertyTagDotRange</span></span>

<span data-ttu-id="2fef2-958">Valores de componente de color que corresponden a un punto de 0% y un punto de 100%.</span><span class="sxs-lookup"><span data-stu-id="2fef2-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="2fef2-959">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-959">Property info</span></span> | <span data-ttu-id="2fef2-960">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-961">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-961">Tag</span></span>   | <span data-ttu-id="2fef2-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="2fef2-962">0x0150</span></span>                                      |
| <span data-ttu-id="2fef2-963">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-963">Type</span></span>  | <span data-ttu-id="2fef2-964">PropertyTagTypeByte o PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-965">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-965">Count</span></span> | <span data-ttu-id="2fef2-966">2 o 2 × PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="2fef2-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="2fef2-967">PropertyTagTargetPrinter</span><span class="sxs-lookup"><span data-stu-id="2fef2-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="2fef2-968">Cadena de caracteres terminada en null que describe el entorno de impresión previsto.</span><span class="sxs-lookup"><span data-stu-id="2fef2-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="2fef2-969">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-969">Property info</span></span> | <span data-ttu-id="2fef2-970">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-971">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-971">Tag</span></span>   | <span data-ttu-id="2fef2-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="2fef2-972">0x0151</span></span>                                             |
| <span data-ttu-id="2fef2-973">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-973">Type</span></span>  | <span data-ttu-id="2fef2-974">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-975">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-975">Count</span></span> | <span data-ttu-id="2fef2-976">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="2fef2-977">PropertyTagExtraSamples</span><span class="sxs-lookup"><span data-stu-id="2fef2-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="2fef2-978">Número de componentes de color adicionales.</span><span class="sxs-lookup"><span data-stu-id="2fef2-978">Number of extra color components.</span></span> <span data-ttu-id="2fef2-979">Por ejemplo, un componente adicional podría contener un valor alfa.</span><span class="sxs-lookup"><span data-stu-id="2fef2-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="2fef2-980">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-980">Property info</span></span> | <span data-ttu-id="2fef2-981">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-982">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-982">Tag</span></span>   | <span data-ttu-id="2fef2-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="2fef2-983">0x0152</span></span>               |
| <span data-ttu-id="2fef2-984">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-984">Type</span></span>  | <span data-ttu-id="2fef2-985">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-986">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-986">Count</span></span> | <span data-ttu-id="2fef2-987">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="2fef2-988">PropertyTagSampleFormat</span><span class="sxs-lookup"><span data-stu-id="2fef2-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="2fef2-989">Para cada componente de color, el formato numérico (sin signo, firmado, punto flotante) de ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="2fef2-990">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-991">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-991">Property info</span></span> | <span data-ttu-id="2fef2-992">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-993">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-993">Tag</span></span>   | <span data-ttu-id="2fef2-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="2fef2-994">0x0153</span></span>                                   |
| <span data-ttu-id="2fef2-995">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-995">Type</span></span>  | <span data-ttu-id="2fef2-996">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-997">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-997">Count</span></span> | <span data-ttu-id="2fef2-998">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="2fef2-999">PropertyTagSMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="2fef2-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="2fef2-1000">Para cada componente de color, el valor mínimo de ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="2fef2-1001">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1002">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1002">Property info</span></span> | <span data-ttu-id="2fef2-1003">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="2fef2-1004">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1004">Tag</span></span>   | <span data-ttu-id="2fef2-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="2fef2-1005">0x0154</span></span>                                              |
| <span data-ttu-id="2fef2-1006">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1006">Type</span></span>  | <span data-ttu-id="2fef2-1007">El tipo que mejor coincide con los datos del componente de píxeles</span><span class="sxs-lookup"><span data-stu-id="2fef2-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="2fef2-1008">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1008">Count</span></span> | <span data-ttu-id="2fef2-1009">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="2fef2-1010">PropertyTagSMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="2fef2-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="2fef2-1011">Para cada componente de color, el valor máximo de ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="2fef2-1012">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1013">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1013">Property info</span></span> | <span data-ttu-id="2fef2-1014">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="2fef2-1015">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1015">Tag</span></span>   | <span data-ttu-id="2fef2-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="2fef2-1016">0x0155</span></span>                                              |
| <span data-ttu-id="2fef2-1017">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1017">Type</span></span>  | <span data-ttu-id="2fef2-1018">El tipo que mejor coincide con los datos del componente de píxeles</span><span class="sxs-lookup"><span data-stu-id="2fef2-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="2fef2-1019">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1019">Count</span></span> | <span data-ttu-id="2fef2-1020">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="2fef2-1021">PropertyTagTransferRange</span><span class="sxs-lookup"><span data-stu-id="2fef2-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="2fef2-1022">Tabla de valores que extiende el intervalo de la función de transferencia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="2fef2-1023">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1023">Property info</span></span> | <span data-ttu-id="2fef2-1024">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1025">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1025">Tag</span></span>   | <span data-ttu-id="2fef2-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="2fef2-1026">0x0156</span></span>               |
| <span data-ttu-id="2fef2-1027">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1027">Type</span></span>  | <span data-ttu-id="2fef2-1028">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1029">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1029">Count</span></span> | <span data-ttu-id="2fef2-1030">6</span><span class="sxs-lookup"><span data-stu-id="2fef2-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="2fef2-1031">PropertyTagJPEGProc</span><span class="sxs-lookup"><span data-stu-id="2fef2-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="2fef2-1032">Proceso de compresión JPEG.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1032">JPEG compression process.</span></span>



| <span data-ttu-id="2fef2-1033">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1033">Property info</span></span> | <span data-ttu-id="2fef2-1034">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1035">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1035">Tag</span></span>   | <span data-ttu-id="2fef2-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="2fef2-1036">0x0200</span></span>               |
| <span data-ttu-id="2fef2-1037">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1037">Type</span></span>  | <span data-ttu-id="2fef2-1038">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1039">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1039">Count</span></span> | <span data-ttu-id="2fef2-1040">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="2fef2-1041">PropertyTagJPEGInterFormat</span><span class="sxs-lookup"><span data-stu-id="2fef2-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="2fef2-1042">Desplazamiento al inicio de un fragmentada JPEG.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="2fef2-1043">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1043">Property info</span></span> | <span data-ttu-id="2fef2-1044">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1045">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1045">Tag</span></span>   | <span data-ttu-id="2fef2-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="2fef2-1046">0x0201</span></span>              |
| <span data-ttu-id="2fef2-1047">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1047">Type</span></span>  | <span data-ttu-id="2fef2-1048">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1049">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1049">Count</span></span> | <span data-ttu-id="2fef2-1050">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="2fef2-1051">PropertyTagJPEGInterLength</span><span class="sxs-lookup"><span data-stu-id="2fef2-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="2fef2-1052">Longitud, en bytes, del fragmentada JPEG.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="2fef2-1053">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1053">Property info</span></span> | <span data-ttu-id="2fef2-1054">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1055">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1055">Tag</span></span>   | <span data-ttu-id="2fef2-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="2fef2-1056">0x0202</span></span>              |
| <span data-ttu-id="2fef2-1057">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1057">Type</span></span>  | <span data-ttu-id="2fef2-1058">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1059">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1059">Count</span></span> | <span data-ttu-id="2fef2-1060">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="2fef2-1061">PropertyTagJPEGRestartInterval</span><span class="sxs-lookup"><span data-stu-id="2fef2-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="2fef2-1062">Longitud del intervalo de reinicio.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="2fef2-1063">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1063">Property info</span></span> | <span data-ttu-id="2fef2-1064">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1065">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1065">Tag</span></span>   | <span data-ttu-id="2fef2-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="2fef2-1066">0x0203</span></span>               |
| <span data-ttu-id="2fef2-1067">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1067">Type</span></span>  | <span data-ttu-id="2fef2-1068">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1069">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1069">Count</span></span> | <span data-ttu-id="2fef2-1070">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="2fef2-1071">PropertyTagJPEGLosslessPredictors</span><span class="sxs-lookup"><span data-stu-id="2fef2-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="2fef2-1072">Para cada componente de color, valor de la selección de predictor sin pérdida para ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="2fef2-1073">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1074">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1074">Property info</span></span> | <span data-ttu-id="2fef2-1075">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-1076">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1076">Tag</span></span>   | <span data-ttu-id="2fef2-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="2fef2-1077">0x0205</span></span>                                   |
| <span data-ttu-id="2fef2-1078">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1078">Type</span></span>  | <span data-ttu-id="2fef2-1079">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-1080">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1080">Count</span></span> | <span data-ttu-id="2fef2-1081">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="2fef2-1082">PropertyTagJPEGPointTransforms</span><span class="sxs-lookup"><span data-stu-id="2fef2-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="2fef2-1083">Para cada componente de color, un valor de transformación de punto para ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="2fef2-1084">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1085">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1085">Property info</span></span> | <span data-ttu-id="2fef2-1086">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-1087">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1087">Tag</span></span>   | <span data-ttu-id="2fef2-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="2fef2-1088">0x0206</span></span>                                   |
| <span data-ttu-id="2fef2-1089">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1089">Type</span></span>  | <span data-ttu-id="2fef2-1090">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="2fef2-1091">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1091">Count</span></span> | <span data-ttu-id="2fef2-1092">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="2fef2-1093">PropertyTagJPEGQTables</span><span class="sxs-lookup"><span data-stu-id="2fef2-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="2fef2-1094">Para cada componente de color, el desplazamiento a la tabla de cuantificación de ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="2fef2-1095">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1096">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1096">Property info</span></span> | <span data-ttu-id="2fef2-1097">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-1098">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1098">Tag</span></span>   | <span data-ttu-id="2fef2-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="2fef2-1099">0x0207</span></span>                                   |
| <span data-ttu-id="2fef2-1100">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1100">Type</span></span>  | <span data-ttu-id="2fef2-1101">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="2fef2-1102">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1102">Count</span></span> | <span data-ttu-id="2fef2-1103">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="2fef2-1104">PropertyTagJPEGDCTables</span><span class="sxs-lookup"><span data-stu-id="2fef2-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="2fef2-1105">Para cada componente de color, el desplazamiento a la tabla Huffman del DC (o tabla Huffman sin pérdida) para ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="2fef2-1106">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1107">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1107">Property info</span></span> | <span data-ttu-id="2fef2-1108">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-1109">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1109">Tag</span></span>   | <span data-ttu-id="2fef2-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="2fef2-1110">0x0208</span></span>                                   |
| <span data-ttu-id="2fef2-1111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1111">Type</span></span>  | <span data-ttu-id="2fef2-1112">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="2fef2-1113">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1113">Count</span></span> | <span data-ttu-id="2fef2-1114">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="2fef2-1115">PropertyTagJPEGACTables</span><span class="sxs-lookup"><span data-stu-id="2fef2-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="2fef2-1116">Para cada componente de color, el desplazamiento a la tabla de la tabla de alimentación de CA para ese componente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="2fef2-1117">Vea también [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1118">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1118">Property info</span></span> | <span data-ttu-id="2fef2-1119">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="2fef2-1120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1120">Tag</span></span>   | <span data-ttu-id="2fef2-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="2fef2-1121">0x0209</span></span>                                   |
| <span data-ttu-id="2fef2-1122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1122">Type</span></span>  | <span data-ttu-id="2fef2-1123">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="2fef2-1124">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1124">Count</span></span> | <span data-ttu-id="2fef2-1125">Número de muestras (componentes) por píxel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="2fef2-1126">PropertyTagYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="2fef2-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="2fef2-1127">Coeficientes para la transformación de datos de imagen de RGB a YCbCr.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="2fef2-1128">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1128">Property info</span></span> | <span data-ttu-id="2fef2-1129">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1130">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1130">Tag</span></span>   | <span data-ttu-id="2fef2-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="2fef2-1131">0x0211</span></span>                  |
| <span data-ttu-id="2fef2-1132">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1132">Type</span></span>  | <span data-ttu-id="2fef2-1133">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1134">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1134">Count</span></span> | <span data-ttu-id="2fef2-1135">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="2fef2-1136">PropertyTagYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="2fef2-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="2fef2-1137">Relación de muestreo de los componentes de crominancia en relación con el componente de luminancia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="2fef2-1138">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1138">Property info</span></span> | <span data-ttu-id="2fef2-1139">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1140">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1140">Tag</span></span>   | <span data-ttu-id="2fef2-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="2fef2-1141">0x0212</span></span>               |
| <span data-ttu-id="2fef2-1142">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1142">Type</span></span>  | <span data-ttu-id="2fef2-1143">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1144">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1144">Count</span></span> | <span data-ttu-id="2fef2-1145">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="2fef2-1146">PropertyTagYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="2fef2-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="2fef2-1147">Posición de los componentes de crominancia en relación con el componente de luminancia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="2fef2-1148">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1148">Property info</span></span> | <span data-ttu-id="2fef2-1149">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1150">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1150">Tag</span></span>   | <span data-ttu-id="2fef2-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="2fef2-1151">0x0213</span></span>               |
| <span data-ttu-id="2fef2-1152">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1152">Type</span></span>  | <span data-ttu-id="2fef2-1153">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1154">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1154">Count</span></span> | <span data-ttu-id="2fef2-1155">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="2fef2-1156">PropertyTagREFBlackWhite</span><span class="sxs-lookup"><span data-stu-id="2fef2-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="2fef2-1157">Valor de punto negro de referencia y valor de punto blanco de referencia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="2fef2-1158">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1158">Property info</span></span> | <span data-ttu-id="2fef2-1159">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1160">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1160">Tag</span></span>   | <span data-ttu-id="2fef2-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="2fef2-1161">0x0214</span></span>                  |
| <span data-ttu-id="2fef2-1162">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1162">Type</span></span>  | <span data-ttu-id="2fef2-1163">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1164">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1164">Count</span></span> | <span data-ttu-id="2fef2-1165">6</span><span class="sxs-lookup"><span data-stu-id="2fef2-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="2fef2-1166">PropertyTagGamma</span><span class="sxs-lookup"><span data-stu-id="2fef2-1166">PropertyTagGamma</span></span>

<span data-ttu-id="2fef2-1167">Valor gamma asociado a la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="2fef2-1168">El valor gamma se almacena como un número racional (par de **Long**) con un numerador de 100000.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="2fef2-1169">Por ejemplo, un valor gamma de 2,2 se almacena como el par (100000, 45455).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="2fef2-1170">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1170">Property info</span></span> | <span data-ttu-id="2fef2-1171">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1172">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1172">Tag</span></span>   | <span data-ttu-id="2fef2-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="2fef2-1173">0x0301</span></span>                  |
| <span data-ttu-id="2fef2-1174">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1174">Type</span></span>  | <span data-ttu-id="2fef2-1175">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1176">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1176">Count</span></span> | <span data-ttu-id="2fef2-1177">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="2fef2-1178">PropertyTagICCProfileDescriptor</span><span class="sxs-lookup"><span data-stu-id="2fef2-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="2fef2-1179">Cadena de caracteres terminada en null que identifica un perfil ICC.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="2fef2-1180">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1180">Property info</span></span> | <span data-ttu-id="2fef2-1181">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1182">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1182">Tag</span></span>   | <span data-ttu-id="2fef2-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="2fef2-1183">0x0302</span></span>                                             |
| <span data-ttu-id="2fef2-1184">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1184">Type</span></span>  | <span data-ttu-id="2fef2-1185">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1186">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1186">Count</span></span> | <span data-ttu-id="2fef2-1187">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="2fef2-1188">PropertyTagSRGBRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="2fef2-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="2fef2-1189">Cómo debe mostrarse la imagen tal como la define el International color Consortium (ICC).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="2fef2-1190">Si un objeto de  [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ se construye con el parámetro *UseEmbeddedColorManagement* establecido en **true**, GDI+ representa la imagen según el intento de representación especificado.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="2fef2-1191">La intención se puede establecer en perceptual, relative colorimétrica, saturación o colorimétrico absoluto.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="2fef2-1192">La intención perceptual, que es adecuada para las fotografías, proporciona una buena adaptación a la gama de la pantalla del dispositivo a costa de la precisión colorimétrica.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="2fef2-1193">La intención colorimétrica relativa es adecuada para las imágenes (por ejemplo, logotipos) que requieren una coincidencia de aspecto de color relativa al punto blanco del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="2fef2-1194">La intención de saturación, que es adecuada para gráficos y gráficos, conserva la saturación a costa del matiz y la luminosidad.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="2fef2-1195">La intención de colorimétrico absoluto es adecuada para las pruebas (vistas previas de imágenes destinadas a un dispositivo de pantalla diferente) que requieran la preservación de la colorimétrico absoluta.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="2fef2-1196">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1196">Tag</span></span>

<span data-ttu-id="2fef2-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="2fef2-1197">0x0303</span></span>

<span data-ttu-id="2fef2-1198">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1198">Type</span></span>

<span data-ttu-id="2fef2-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="2fef2-1199">BYTE</span></span>

<span data-ttu-id="2fef2-1200">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1200">Count</span></span>

<span data-ttu-id="2fef2-1201">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1201">1</span></span>

<span data-ttu-id="2fef2-1202">0-percepción 1-colorimétrico relativo 2-saturación 3-colorimétrico absoluto</span><span class="sxs-lookup"><span data-stu-id="2fef2-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="2fef2-1203">PropertyTagImageTitle</span><span class="sxs-lookup"><span data-stu-id="2fef2-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="2fef2-1204">Cadena de caracteres terminada en null que especifica el título de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="2fef2-1205">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1205">Property info</span></span> | <span data-ttu-id="2fef2-1206">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1207">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1207">Tag</span></span>   | <span data-ttu-id="2fef2-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="2fef2-1208">0x0320</span></span>                                             |
| <span data-ttu-id="2fef2-1209">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1209">Type</span></span>  | <span data-ttu-id="2fef2-1210">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1211">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1211">Count</span></span> | <span data-ttu-id="2fef2-1212">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="2fef2-1213">PropertyTagResolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="2fef2-1214">Unidades en las que se va a mostrar la resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="2fef2-1215">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1215">Tag</span></span>

<span data-ttu-id="2fef2-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="2fef2-1216">0x5001</span></span>

<span data-ttu-id="2fef2-1217">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1217">Type</span></span>

<span data-ttu-id="2fef2-1218">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1219">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1219">Count</span></span>

<span data-ttu-id="2fef2-1220">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1220">1</span></span>

<span data-ttu-id="2fef2-1221">1-píxeles por pulgada 2-píxeles por centímetro</span><span class="sxs-lookup"><span data-stu-id="2fef2-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="2fef2-1222">PropertyTagResolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="2fef2-1223">Unidades en las que se va a mostrar la resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="2fef2-1224">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1224">Tag</span></span>

<span data-ttu-id="2fef2-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="2fef2-1225">0x5002</span></span>

<span data-ttu-id="2fef2-1226">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1226">Type</span></span>

<span data-ttu-id="2fef2-1227">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1228">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1228">Count</span></span>

<span data-ttu-id="2fef2-1229">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1229">1</span></span>

<span data-ttu-id="2fef2-1230">1-píxeles por pulgada 2-píxeles por centímetro</span><span class="sxs-lookup"><span data-stu-id="2fef2-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="2fef2-1231">PropertyTagResolutionXLengthUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="2fef2-1232">Unidades en las que se va a mostrar el ancho de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="2fef2-1233">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1233">Tag</span></span>

<span data-ttu-id="2fef2-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="2fef2-1234">0x5003</span></span>

<span data-ttu-id="2fef2-1235">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1235">Type</span></span>

<span data-ttu-id="2fef2-1236">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1237">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1237">Count</span></span>

<span data-ttu-id="2fef2-1238">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1238">1</span></span>

<span data-ttu-id="2fef2-1239">1 PDA 2-centímetros 3 puntos 4-picas 5-columnas</span><span class="sxs-lookup"><span data-stu-id="2fef2-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="2fef2-1240">PropertyTagResolutionYLengthUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="2fef2-1241">Unidades en las que se va a mostrar el alto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="2fef2-1242">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1242">Tag</span></span>

<span data-ttu-id="2fef2-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="2fef2-1243">0x5004</span></span>

<span data-ttu-id="2fef2-1244">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1244">Type</span></span>

<span data-ttu-id="2fef2-1245">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1246">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1246">Count</span></span>

<span data-ttu-id="2fef2-1247">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1247">1</span></span>

<span data-ttu-id="2fef2-1248">1 PDA 2-centímetros 3 puntos 4-picas 5-columnas</span><span class="sxs-lookup"><span data-stu-id="2fef2-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="2fef2-1249">PropertyTagPrintFlags</span><span class="sxs-lookup"><span data-stu-id="2fef2-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="2fef2-1250">Secuencia de valores booleanos de un byte que especifican las opciones de impresión.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="2fef2-1251">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1251">Property info</span></span> | <span data-ttu-id="2fef2-1252">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1253">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1253">Tag</span></span>   | <span data-ttu-id="2fef2-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="2fef2-1254">0x5005</span></span>               |
| <span data-ttu-id="2fef2-1255">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1255">Type</span></span>  | <span data-ttu-id="2fef2-1256">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-1257">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1257">Count</span></span> | <span data-ttu-id="2fef2-1258">Número de marcas</span><span class="sxs-lookup"><span data-stu-id="2fef2-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="2fef2-1259">PropertyTagPrintFlagsVersion</span><span class="sxs-lookup"><span data-stu-id="2fef2-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="2fef2-1260">Versión de marcas de impresión.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1260">Print flags version.</span></span>



| <span data-ttu-id="2fef2-1261">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1261">Property info</span></span> | <span data-ttu-id="2fef2-1262">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1263">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1263">Tag</span></span>   | <span data-ttu-id="2fef2-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="2fef2-1264">0x5006</span></span>               |
| <span data-ttu-id="2fef2-1265">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1265">Type</span></span>  | <span data-ttu-id="2fef2-1266">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1267">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1267">Count</span></span> | <span data-ttu-id="2fef2-1268">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="2fef2-1269">PropertyTagPrintFlagsCrop</span><span class="sxs-lookup"><span data-stu-id="2fef2-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="2fef2-1270">Marcas de recorte del centro de marcas de impresión.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="2fef2-1271">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1271">Property info</span></span> | <span data-ttu-id="2fef2-1272">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1273">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1273">Tag</span></span>   | <span data-ttu-id="2fef2-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="2fef2-1274">0x5007</span></span>              |
| <span data-ttu-id="2fef2-1275">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1275">Type</span></span>  | <span data-ttu-id="2fef2-1276">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-1277">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1277">Count</span></span> | <span data-ttu-id="2fef2-1278">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="2fef2-1279">PropertyTagPrintFlagsBleedWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="2fef2-1280">Ancho de sangría de marcas de impresión</span><span class="sxs-lookup"><span data-stu-id="2fef2-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="2fef2-1281">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1281">Property info</span></span> | <span data-ttu-id="2fef2-1282">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1283">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1283">Tag</span></span>   | <span data-ttu-id="2fef2-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="2fef2-1284">0x5008</span></span>              |
| <span data-ttu-id="2fef2-1285">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1285">Type</span></span>  | <span data-ttu-id="2fef2-1286">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1287">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1287">Count</span></span> | <span data-ttu-id="2fef2-1288">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="2fef2-1289">PropertyTagPrintFlagsBleedWidthScale</span><span class="sxs-lookup"><span data-stu-id="2fef2-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="2fef2-1290">Escala de ancho de sangría de marcas de impresión</span><span class="sxs-lookup"><span data-stu-id="2fef2-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="2fef2-1291">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1291">Property info</span></span> | <span data-ttu-id="2fef2-1292">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1293">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1293">Tag</span></span>   | <span data-ttu-id="2fef2-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="2fef2-1294">0x5009</span></span>               |
| <span data-ttu-id="2fef2-1295">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1295">Type</span></span>  | <span data-ttu-id="2fef2-1296">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1297">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1297">Count</span></span> | <span data-ttu-id="2fef2-1298">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="2fef2-1299">PropertyTagHalftoneLPI</span><span class="sxs-lookup"><span data-stu-id="2fef2-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="2fef2-1300">Frecuencia de la pantalla de la tinta, en líneas por pulgada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="2fef2-1301">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1301">Property info</span></span> | <span data-ttu-id="2fef2-1302">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1303">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1303">Tag</span></span>   | <span data-ttu-id="2fef2-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="2fef2-1304">0x500A</span></span>                  |
| <span data-ttu-id="2fef2-1305">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1305">Type</span></span>  | <span data-ttu-id="2fef2-1306">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1307">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1307">Count</span></span> | <span data-ttu-id="2fef2-1308">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="2fef2-1309">PropertyTagHalftoneLPIUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="2fef2-1310">Unidades para la frecuencia de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="2fef2-1311">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1311">Tag</span></span>

<span data-ttu-id="2fef2-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="2fef2-1312">0x500B</span></span>

<span data-ttu-id="2fef2-1313">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1313">Type</span></span>

<span data-ttu-id="2fef2-1314">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1315">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1315">Count</span></span>

<span data-ttu-id="2fef2-1316">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1316">1</span></span>

<span data-ttu-id="2fef2-1317">1-líneas por pulgada de 2 líneas por centímetro</span><span class="sxs-lookup"><span data-stu-id="2fef2-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="2fef2-1318">PropertyTagHalftoneDegree</span><span class="sxs-lookup"><span data-stu-id="2fef2-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="2fef2-1319">Ángulo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1319">Angle for screen.</span></span>



| <span data-ttu-id="2fef2-1320">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1320">Property info</span></span> | <span data-ttu-id="2fef2-1321">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1322">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1322">Tag</span></span>   | <span data-ttu-id="2fef2-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="2fef2-1323">0x500C</span></span>                  |
| <span data-ttu-id="2fef2-1324">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1324">Type</span></span>  | <span data-ttu-id="2fef2-1325">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1326">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1326">Count</span></span> | <span data-ttu-id="2fef2-1327">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="2fef2-1328">PropertyTagHalftoneShape</span><span class="sxs-lookup"><span data-stu-id="2fef2-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="2fef2-1329">Forma de los puntos de semitono.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="2fef2-1330">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1330">Tag</span></span>

<span data-ttu-id="2fef2-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="2fef2-1331">0x500D</span></span>

<span data-ttu-id="2fef2-1332">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1332">Type</span></span>

<span data-ttu-id="2fef2-1333">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-1334">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1334">Count</span></span>

<span data-ttu-id="2fef2-1335">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1335">1</span></span>

<span data-ttu-id="2fef2-1336">0-redondo 1-elipse 2-línea 3-cuadrado 4-Cruz 6-rombo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="2fef2-1337">PropertyTagHalftoneMisc</span><span class="sxs-lookup"><span data-stu-id="2fef2-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="2fef2-1338">Información de semitono diversa.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="2fef2-1339">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1339">Property info</span></span> | <span data-ttu-id="2fef2-1340">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1341">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1341">Tag</span></span>   | <span data-ttu-id="2fef2-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="2fef2-1342">0x500E</span></span>              |
| <span data-ttu-id="2fef2-1343">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1343">Type</span></span>  | <span data-ttu-id="2fef2-1344">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1345">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1345">Count</span></span> | <span data-ttu-id="2fef2-1346">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="2fef2-1347">PropertyTagHalftoneScreen</span><span class="sxs-lookup"><span data-stu-id="2fef2-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="2fef2-1348">Valor booleano que especifica si se van a utilizar las pantallas predeterminadas de la impresora.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="2fef2-1349">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1349">Tag</span></span>

<span data-ttu-id="2fef2-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="2fef2-1350">0x500F</span></span>

<span data-ttu-id="2fef2-1351">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1351">Type</span></span>

<span data-ttu-id="2fef2-1352">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="2fef2-1353">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1353">Count</span></span>

<span data-ttu-id="2fef2-1354">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1354">1</span></span>

<span data-ttu-id="2fef2-1355">1-usar las pantallas predeterminadas de la impresora 2-otras</span><span class="sxs-lookup"><span data-stu-id="2fef2-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="2fef2-1356">PropertyTagJPEGQuality</span><span class="sxs-lookup"><span data-stu-id="2fef2-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="2fef2-1357">Etiqueta privada utilizada por el formato de Adobe Photoshop.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="2fef2-1358">No disponible para uso público.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1358">Not for public use.</span></span>



| <span data-ttu-id="2fef2-1359">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1359">Property info</span></span> | <span data-ttu-id="2fef2-1360">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1361">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1361">Tag</span></span>   | <span data-ttu-id="2fef2-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="2fef2-1362">0x5010</span></span>               |
| <span data-ttu-id="2fef2-1363">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1363">Type</span></span>  | <span data-ttu-id="2fef2-1364">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1365">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1365">Count</span></span> | <span data-ttu-id="2fef2-1366">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="2fef2-1367">PropertyTagGridSize</span><span class="sxs-lookup"><span data-stu-id="2fef2-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="2fef2-1368">Bloque de información sobre cuadrículas y guías.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="2fef2-1369">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1369">Property info</span></span> | <span data-ttu-id="2fef2-1370">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-1371">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1371">Tag</span></span>   | <span data-ttu-id="2fef2-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="2fef2-1372">0x5011</span></span>                   |
| <span data-ttu-id="2fef2-1373">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1373">Type</span></span>  | <span data-ttu-id="2fef2-1374">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-1375">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1375">Count</span></span> | <span data-ttu-id="2fef2-1376">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="2fef2-1377">PropertyTagThumbnailFormat</span><span class="sxs-lookup"><span data-stu-id="2fef2-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="2fef2-1378">Formato de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="2fef2-1379">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1379">Tag</span></span>

<span data-ttu-id="2fef2-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="2fef2-1380">0x5012</span></span>

<span data-ttu-id="2fef2-1381">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1381">Type</span></span>

<span data-ttu-id="2fef2-1382">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="2fef2-1383">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1383">Count</span></span>

<span data-ttu-id="2fef2-1384">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1384">1</span></span>

<span data-ttu-id="2fef2-1385">0-RGB sin formato 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="2fef2-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="2fef2-1386">PropertyTagThumbnailWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="2fef2-1387">Ancho, en píxeles, de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1388">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1388">Property info</span></span> | <span data-ttu-id="2fef2-1389">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1390">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1390">Tag</span></span>   | <span data-ttu-id="2fef2-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="2fef2-1391">0x5013</span></span>              |
| <span data-ttu-id="2fef2-1392">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1392">Type</span></span>  | <span data-ttu-id="2fef2-1393">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1394">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1394">Count</span></span> | <span data-ttu-id="2fef2-1395">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="2fef2-1396">PropertyTagThumbnailHeight</span><span class="sxs-lookup"><span data-stu-id="2fef2-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="2fef2-1397">Alto, en píxeles, de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1398">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1398">Property info</span></span> | <span data-ttu-id="2fef2-1399">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1400">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1400">Tag</span></span>   | <span data-ttu-id="2fef2-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="2fef2-1401">0x5014</span></span>              |
| <span data-ttu-id="2fef2-1402">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1402">Type</span></span>  | <span data-ttu-id="2fef2-1403">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1404">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1404">Count</span></span> | <span data-ttu-id="2fef2-1405">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="2fef2-1406">PropertyTagThumbnailColorDepth</span><span class="sxs-lookup"><span data-stu-id="2fef2-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="2fef2-1407">bits por píxel (BPP) para la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1408">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1408">Property info</span></span> | <span data-ttu-id="2fef2-1409">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1410">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1410">Tag</span></span>   | <span data-ttu-id="2fef2-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="2fef2-1411">0x5015</span></span>               |
| <span data-ttu-id="2fef2-1412">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1412">Type</span></span>  | <span data-ttu-id="2fef2-1413">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1414">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1414">Count</span></span> | <span data-ttu-id="2fef2-1415">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="2fef2-1416">PropertyTagThumbnailPlanes</span><span class="sxs-lookup"><span data-stu-id="2fef2-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="2fef2-1417">Número de planos de color de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1418">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1418">Property info</span></span> | <span data-ttu-id="2fef2-1419">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1420">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1420">Tag</span></span>   | <span data-ttu-id="2fef2-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="2fef2-1421">0x5016</span></span>               |
| <span data-ttu-id="2fef2-1422">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1422">Type</span></span>  | <span data-ttu-id="2fef2-1423">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1424">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1424">Count</span></span> | <span data-ttu-id="2fef2-1425">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="2fef2-1426">PropertyTagThumbnailRawBytes</span><span class="sxs-lookup"><span data-stu-id="2fef2-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="2fef2-1427">Desplazamiento de bytes entre filas de datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="2fef2-1428">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1428">Property info</span></span> | <span data-ttu-id="2fef2-1429">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1430">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1430">Tag</span></span>   | <span data-ttu-id="2fef2-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="2fef2-1431">0x5017</span></span>              |
| <span data-ttu-id="2fef2-1432">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1432">Type</span></span>  | <span data-ttu-id="2fef2-1433">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1434">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1434">Count</span></span> | <span data-ttu-id="2fef2-1435">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="2fef2-1436">PropertyTagThumbnailSize</span><span class="sxs-lookup"><span data-stu-id="2fef2-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="2fef2-1437">Tamaño total, en bytes, de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1438">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1438">Property info</span></span> | <span data-ttu-id="2fef2-1439">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1440">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1440">Tag</span></span>   | <span data-ttu-id="2fef2-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="2fef2-1441">0x5018</span></span>              |
| <span data-ttu-id="2fef2-1442">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1442">Type</span></span>  | <span data-ttu-id="2fef2-1443">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1444">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1444">Count</span></span> | <span data-ttu-id="2fef2-1445">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="2fef2-1446">PropertyTagThumbnailCompressedSize</span><span class="sxs-lookup"><span data-stu-id="2fef2-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="2fef2-1447">Tamaño comprimido, en bytes, de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1448">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1448">Property info</span></span> | <span data-ttu-id="2fef2-1449">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1450">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1450">Tag</span></span>   | <span data-ttu-id="2fef2-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="2fef2-1451">0x5019</span></span>              |
| <span data-ttu-id="2fef2-1452">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1452">Type</span></span>  | <span data-ttu-id="2fef2-1453">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1454">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1454">Count</span></span> | <span data-ttu-id="2fef2-1455">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="2fef2-1456">PropertyTagColorTransferFunction</span><span class="sxs-lookup"><span data-stu-id="2fef2-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="2fef2-1457">Tabla de valores que especifican las funciones de transferencia de color.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="2fef2-1458">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1458">Property info</span></span> | <span data-ttu-id="2fef2-1459">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-1460">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1460">Tag</span></span>   | <span data-ttu-id="2fef2-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="2fef2-1461">0x501A</span></span>                   |
| <span data-ttu-id="2fef2-1462">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1462">Type</span></span>  | <span data-ttu-id="2fef2-1463">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-1464">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1464">Count</span></span> | <span data-ttu-id="2fef2-1465">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="2fef2-1466">PropertyTagThumbnailData</span><span class="sxs-lookup"><span data-stu-id="2fef2-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="2fef2-1467">Bits de miniaturas sin formato en formato JPEG o RGB.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="2fef2-1468">Depende de PropertyTagThumbnailFormat.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="2fef2-1469">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1469">Property info</span></span> | <span data-ttu-id="2fef2-1470">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1471">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1471">Tag</span></span>   | <span data-ttu-id="2fef2-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="2fef2-1472">0x501B</span></span>              |
| <span data-ttu-id="2fef2-1473">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1473">Type</span></span>  | <span data-ttu-id="2fef2-1474">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-1475">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1475">Count</span></span> | <span data-ttu-id="2fef2-1476">Variable</span><span class="sxs-lookup"><span data-stu-id="2fef2-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="2fef2-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="2fef2-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="2fef2-1478">Número de píxeles por fila de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1479">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1479">Property info</span></span> | <span data-ttu-id="2fef2-1480">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-1481">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1481">Tag</span></span>   | <span data-ttu-id="2fef2-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="2fef2-1482">0x5020</span></span>                                      |
| <span data-ttu-id="2fef2-1483">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1483">Type</span></span>  | <span data-ttu-id="2fef2-1484">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1485">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1485">Count</span></span> | <span data-ttu-id="2fef2-1486">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="2fef2-1487">PropertyTagThumbnailImageHeight</span><span class="sxs-lookup"><span data-stu-id="2fef2-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="2fef2-1488">Número de filas de píxeles de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1489">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1489">Property info</span></span> | <span data-ttu-id="2fef2-1490">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-1491">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1491">Tag</span></span>   | <span data-ttu-id="2fef2-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="2fef2-1492">0x5021</span></span>                                      |
| <span data-ttu-id="2fef2-1493">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1493">Type</span></span>  | <span data-ttu-id="2fef2-1494">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1495">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1495">Count</span></span> | <span data-ttu-id="2fef2-1496">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="2fef2-1497">PropertyTagThumbnailBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="2fef2-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="2fef2-1498">Número de bits por componente de color de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="2fef2-1499">Vea también [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="2fef2-1500">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1500">Property info</span></span> | <span data-ttu-id="2fef2-1501">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="2fef2-1502">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1502">Tag</span></span>   | <span data-ttu-id="2fef2-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="2fef2-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="2fef2-1504">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1504">Type</span></span>  | <span data-ttu-id="2fef2-1505">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="2fef2-1506">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1506">Count</span></span> | <span data-ttu-id="2fef2-1507">Número de muestras (componentes) por píxel en la imagen en miniatura</span><span class="sxs-lookup"><span data-stu-id="2fef2-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="2fef2-1508">PropertyTagThumbnailCompression</span><span class="sxs-lookup"><span data-stu-id="2fef2-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="2fef2-1509">Esquema de compresión utilizado para los datos de imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="2fef2-1510">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1510">Property info</span></span> | <span data-ttu-id="2fef2-1511">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1512">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1512">Tag</span></span>   | <span data-ttu-id="2fef2-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="2fef2-1513">0x5023</span></span>               |
| <span data-ttu-id="2fef2-1514">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1514">Type</span></span>  | <span data-ttu-id="2fef2-1515">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1516">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1516">Count</span></span> | <span data-ttu-id="2fef2-1517">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="2fef2-1518">PropertyTagThumbnailPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="2fef2-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="2fef2-1519">Cómo se interpretarán los datos de píxeles en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="2fef2-1520">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1520">Property info</span></span> | <span data-ttu-id="2fef2-1521">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1522">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1522">Tag</span></span>   | <span data-ttu-id="2fef2-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="2fef2-1523">0x5024</span></span>               |
| <span data-ttu-id="2fef2-1524">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1524">Type</span></span>  | <span data-ttu-id="2fef2-1525">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1526">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1526">Count</span></span> | <span data-ttu-id="2fef2-1527">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="2fef2-1528">PropertyTagThumbnailImageDescription</span><span class="sxs-lookup"><span data-stu-id="2fef2-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="2fef2-1529">Cadena de caracteres terminada en null que especifica el título de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="2fef2-1530">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1530">Property info</span></span> | <span data-ttu-id="2fef2-1531">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1532">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1532">Tag</span></span>   | <span data-ttu-id="2fef2-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="2fef2-1533">0x5025</span></span>                                             |
| <span data-ttu-id="2fef2-1534">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1534">Type</span></span>  | <span data-ttu-id="2fef2-1535">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1536">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1536">Count</span></span> | <span data-ttu-id="2fef2-1537">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="2fef2-1538">PropertyTagThumbnailEquipMake</span><span class="sxs-lookup"><span data-stu-id="2fef2-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="2fef2-1539">Cadena de caracteres terminada en null que especifica el fabricante del equipo usado para grabar la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1540">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1540">Property info</span></span> | <span data-ttu-id="2fef2-1541">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1542">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1542">Tag</span></span>   | <span data-ttu-id="2fef2-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="2fef2-1543">0x5026</span></span>                                             |
| <span data-ttu-id="2fef2-1544">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1544">Type</span></span>  | <span data-ttu-id="2fef2-1545">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1546">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1546">Count</span></span> | <span data-ttu-id="2fef2-1547">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="2fef2-1548">PropertyTagThumbnailEquipModel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="2fef2-1549">Cadena de caracteres terminada en null que especifica el nombre del modelo o el número de modelo del equipo usado para grabar la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1550">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1550">Property info</span></span> | <span data-ttu-id="2fef2-1551">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1552">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1552">Tag</span></span>   | <span data-ttu-id="2fef2-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="2fef2-1553">0x5027</span></span>                                             |
| <span data-ttu-id="2fef2-1554">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1554">Type</span></span>  | <span data-ttu-id="2fef2-1555">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1556">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1556">Count</span></span> | <span data-ttu-id="2fef2-1557">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="2fef2-1558">PropertyTagThumbnailStripOffsets</span><span class="sxs-lookup"><span data-stu-id="2fef2-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="2fef2-1559">Para cada franja de la imagen en miniatura, el desplazamiento de bytes de esa franja.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="2fef2-1560">Vea también [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) y [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="2fef2-1561">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1561">Property info</span></span> | <span data-ttu-id="2fef2-1562">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-1563">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1563">Tag</span></span>   | <span data-ttu-id="2fef2-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="2fef2-1564">0x5028</span></span>                                      |
| <span data-ttu-id="2fef2-1565">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1565">Type</span></span>  | <span data-ttu-id="2fef2-1566">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1567">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1567">Count</span></span> | <span data-ttu-id="2fef2-1568">Número de bandas</span><span class="sxs-lookup"><span data-stu-id="2fef2-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="2fef2-1569">PropertyTagThumbnailOrientation</span><span class="sxs-lookup"><span data-stu-id="2fef2-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="2fef2-1570">Orientación de la imagen en miniatura en términos de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="2fef2-1571">Vea también [PropertyTagOrientation](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="2fef2-1572">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1572">Property info</span></span> | <span data-ttu-id="2fef2-1573">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1574">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1574">Tag</span></span>   | <span data-ttu-id="2fef2-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="2fef2-1575">0x5029</span></span>               |
| <span data-ttu-id="2fef2-1576">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1576">Type</span></span>  | <span data-ttu-id="2fef2-1577">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1578">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1578">Count</span></span> | <span data-ttu-id="2fef2-1579">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="2fef2-1580">PropertyTagThumbnailSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="2fef2-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="2fef2-1581">Número de componentes de color por píxel en la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1582">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1582">Property info</span></span> | <span data-ttu-id="2fef2-1583">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1584">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1584">Tag</span></span>   | <span data-ttu-id="2fef2-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="2fef2-1585">0x502A</span></span>               |
| <span data-ttu-id="2fef2-1586">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1586">Type</span></span>  | <span data-ttu-id="2fef2-1587">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1588">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1588">Count</span></span> | <span data-ttu-id="2fef2-1589">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="2fef2-1590">PropertyTagThumbnailRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="2fef2-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="2fef2-1591">Número de filas por franja en la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="2fef2-1592">Vea también [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) y [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="2fef2-1593">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1593">Property info</span></span> | <span data-ttu-id="2fef2-1594">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-1595">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1595">Tag</span></span>   | <span data-ttu-id="2fef2-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="2fef2-1596">0x502B</span></span>                                      |
| <span data-ttu-id="2fef2-1597">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1597">Type</span></span>  | <span data-ttu-id="2fef2-1598">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1599">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1599">Count</span></span> | <span data-ttu-id="2fef2-1600">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="2fef2-1601">PropertyTagThumbnailStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="2fef2-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="2fef2-1602">Para cada franja de imagen en miniatura, el número total de bytes de esa franja.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="2fef2-1603">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1603">Property info</span></span> | <span data-ttu-id="2fef2-1604">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-1605">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1605">Tag</span></span>   | <span data-ttu-id="2fef2-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="2fef2-1606">0x502C</span></span>                                      |
| <span data-ttu-id="2fef2-1607">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1607">Type</span></span>  | <span data-ttu-id="2fef2-1608">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1609">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1609">Count</span></span> | <span data-ttu-id="2fef2-1610">Número de bandas en la imagen en miniatura</span><span class="sxs-lookup"><span data-stu-id="2fef2-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="2fef2-1611">PropertyTagThumbnailResolutionX</span><span class="sxs-lookup"><span data-stu-id="2fef2-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="2fef2-1612">Resolución de miniaturas en la dirección de ancho.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="2fef2-1613">La unidad de resolución se proporciona en [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="2fef2-1614">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1614">Property info</span></span> | <span data-ttu-id="2fef2-1615">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="2fef2-1616">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1616">Tag</span></span> | <span data-ttu-id="2fef2-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="2fef2-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="2fef2-1618">PropertyTagThumbnailResolutionY</span><span class="sxs-lookup"><span data-stu-id="2fef2-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="2fef2-1619">Resolución de miniaturas en la dirección de alto.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="2fef2-1620">La unidad de resolución se proporciona en [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="2fef2-1621">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1621">Property info</span></span> | <span data-ttu-id="2fef2-1622">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="2fef2-1623">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1623">Tag</span></span> | <span data-ttu-id="2fef2-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="2fef2-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="2fef2-1625">PropertyTagThumbnailPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="2fef2-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="2fef2-1626">Si los componentes de píxeles de la imagen en miniatura se registran en formato plano o fragmentado.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="2fef2-1627">Vea también [PropertyTagPlanarConfig](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="2fef2-1628">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1628">Property info</span></span> | <span data-ttu-id="2fef2-1629">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1630">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1630">Tag</span></span>   | <span data-ttu-id="2fef2-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="2fef2-1631">0x502F</span></span>               |
| <span data-ttu-id="2fef2-1632">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1632">Type</span></span>  | <span data-ttu-id="2fef2-1633">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1634">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1634">Count</span></span> | <span data-ttu-id="2fef2-1635">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="2fef2-1636">PropertyTagThumbnailResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="2fef2-1637">Unidad de medida para la resolución horizontal y la resolución vertical de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="2fef2-1638">Vea también [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="2fef2-1639">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1639">Property info</span></span> | <span data-ttu-id="2fef2-1640">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1641">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1641">Tag</span></span>   | <span data-ttu-id="2fef2-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="2fef2-1642">0x5030</span></span>               |
| <span data-ttu-id="2fef2-1643">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1643">Type</span></span>  | <span data-ttu-id="2fef2-1644">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1645">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1645">Count</span></span> | <span data-ttu-id="2fef2-1646">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="2fef2-1647">PropertyTagThumbnailTransferFunction</span><span class="sxs-lookup"><span data-stu-id="2fef2-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="2fef2-1648">Tablas que especifican funciones de transferencia para la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="2fef2-1649">Vea también [PropertyTagTransferFunction](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="2fef2-1650">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1650">Property info</span></span> | <span data-ttu-id="2fef2-1651">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="2fef2-1652">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1652">Tag</span></span>   | <span data-ttu-id="2fef2-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="2fef2-1653">0x5031</span></span>                                               |
| <span data-ttu-id="2fef2-1654">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1654">Type</span></span>  | <span data-ttu-id="2fef2-1655">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="2fef2-1656">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1656">Count</span></span> | <span data-ttu-id="2fef2-1657">Número total de palabras de 16 bits necesarias para las tablas</span><span class="sxs-lookup"><span data-stu-id="2fef2-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="2fef2-1658">PropertyTagThumbnailSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="2fef2-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="2fef2-1659">Cadena de caracteres terminada en null que especifica el nombre y la versión del software o firmware del dispositivo usado para generar la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1660">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1660">Property info</span></span> | <span data-ttu-id="2fef2-1661">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1662">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1662">Tag</span></span>   | <span data-ttu-id="2fef2-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="2fef2-1663">0x5032</span></span>                                             |
| <span data-ttu-id="2fef2-1664">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1664">Type</span></span>  | <span data-ttu-id="2fef2-1665">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1666">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1666">Count</span></span> | <span data-ttu-id="2fef2-1667">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="2fef2-1668">PropertyTagThumbnailDateTime</span><span class="sxs-lookup"><span data-stu-id="2fef2-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="2fef2-1669">Fecha y hora en que se creó la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="2fef2-1670">Vea también [PropertyTagDateTime](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="2fef2-1671">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1671">Property info</span></span> | <span data-ttu-id="2fef2-1672">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1673">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1673">Tag</span></span>   | <span data-ttu-id="2fef2-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="2fef2-1674">0x5033</span></span>               |
| <span data-ttu-id="2fef2-1675">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1675">Type</span></span>  | <span data-ttu-id="2fef2-1676">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-1677">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1677">Count</span></span> | <span data-ttu-id="2fef2-1678">20</span><span class="sxs-lookup"><span data-stu-id="2fef2-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="2fef2-1679">PropertyTagThumbnailArtist</span><span class="sxs-lookup"><span data-stu-id="2fef2-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="2fef2-1680">Cadena de caracteres terminada en null que especifica el nombre de la persona que creó la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1681">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1681">Property info</span></span> | <span data-ttu-id="2fef2-1682">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1683">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1683">Tag</span></span>   | <span data-ttu-id="2fef2-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="2fef2-1684">0x5034</span></span>                                             |
| <span data-ttu-id="2fef2-1685">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1685">Type</span></span>  | <span data-ttu-id="2fef2-1686">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1687">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1687">Count</span></span> | <span data-ttu-id="2fef2-1688">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="2fef2-1689">PropertyTagThumbnailWhitePoint</span><span class="sxs-lookup"><span data-stu-id="2fef2-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="2fef2-1690">Cromaticidad del punto blanco de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="2fef2-1691">Vea también [PropertyTagWhitePoint](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="2fef2-1692">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1692">Property info</span></span> | <span data-ttu-id="2fef2-1693">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1694">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1694">Tag</span></span>   | <span data-ttu-id="2fef2-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="2fef2-1695">0x5035</span></span>                  |
| <span data-ttu-id="2fef2-1696">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1696">Type</span></span>  | <span data-ttu-id="2fef2-1697">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1698">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1698">Count</span></span> | <span data-ttu-id="2fef2-1699">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="2fef2-1700">PropertyTagThumbnailPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="2fef2-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="2fef2-1701">Para cada uno de los tres colores primarios de la imagen en miniatura, la cromaticidad de ese color.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="2fef2-1702">Vea también [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="2fef2-1703">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1703">Property info</span></span> | <span data-ttu-id="2fef2-1704">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1705">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1705">Tag</span></span>   | <span data-ttu-id="2fef2-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="2fef2-1706">0x5036</span></span>                  |
| <span data-ttu-id="2fef2-1707">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1707">Type</span></span>  | <span data-ttu-id="2fef2-1708">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1709">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1709">Count</span></span> | <span data-ttu-id="2fef2-1710">6</span><span class="sxs-lookup"><span data-stu-id="2fef2-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="2fef2-1711">PropertyTagThumbnailYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="2fef2-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="2fef2-1712">Coeficientes para la transformación de datos de RGB a YCbCr para la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="2fef2-1713">Vea también [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="2fef2-1714">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1714">Property info</span></span> | <span data-ttu-id="2fef2-1715">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1716">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1716">Tag</span></span>   | <span data-ttu-id="2fef2-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="2fef2-1717">0x5037</span></span>                  |
| <span data-ttu-id="2fef2-1718">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1718">Type</span></span>  | <span data-ttu-id="2fef2-1719">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1720">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1720">Count</span></span> | <span data-ttu-id="2fef2-1721">3</span><span class="sxs-lookup"><span data-stu-id="2fef2-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="2fef2-1722">PropertyTagThumbnailYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="2fef2-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="2fef2-1723">Relación de muestreo de los componentes de crominancia en relación con el componente de luminancia de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="2fef2-1724">Vea también [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="2fef2-1725">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1725">Property info</span></span> | <span data-ttu-id="2fef2-1726">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1727">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1727">Tag</span></span>   | <span data-ttu-id="2fef2-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="2fef2-1728">0x5038</span></span>               |
| <span data-ttu-id="2fef2-1729">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1729">Type</span></span>  | <span data-ttu-id="2fef2-1730">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1731">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1731">Count</span></span> | <span data-ttu-id="2fef2-1732">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="2fef2-1733">PropertyTagThumbnailYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="2fef2-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="2fef2-1734">Posición de los componentes de crominancia en relación con el componente de luminancia de la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="2fef2-1735">Vea también [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="2fef2-1736">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1736">Property info</span></span> | <span data-ttu-id="2fef2-1737">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1738">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1738">Tag</span></span>   | <span data-ttu-id="2fef2-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="2fef2-1739">0x5039</span></span>               |
| <span data-ttu-id="2fef2-1740">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1740">Type</span></span>  | <span data-ttu-id="2fef2-1741">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1742">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1742">Count</span></span> | <span data-ttu-id="2fef2-1743">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="2fef2-1744">PropertyTagThumbnailRefBlackWhite</span><span class="sxs-lookup"><span data-stu-id="2fef2-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="2fef2-1745">Valor de punto negro de referencia y valor de punto blanco de referencia para la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="2fef2-1746">Vea también [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="2fef2-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="2fef2-1747">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1747">Property info</span></span> | <span data-ttu-id="2fef2-1748">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1749">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1749">Tag</span></span>   | <span data-ttu-id="2fef2-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="2fef2-1750">0x503A</span></span>                  |
| <span data-ttu-id="2fef2-1751">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1751">Type</span></span>  | <span data-ttu-id="2fef2-1752">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1753">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1753">Count</span></span> | <span data-ttu-id="2fef2-1754">6</span><span class="sxs-lookup"><span data-stu-id="2fef2-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="2fef2-1755">PropertyTagThumbnailCopyRight</span><span class="sxs-lookup"><span data-stu-id="2fef2-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="2fef2-1756">Cadena de caracteres terminada en null que contiene información de copyright para la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="2fef2-1757">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1757">Property info</span></span> | <span data-ttu-id="2fef2-1758">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1759">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1759">Tag</span></span>   | <span data-ttu-id="2fef2-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="2fef2-1760">0x503B</span></span>                                             |
| <span data-ttu-id="2fef2-1761">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1761">Type</span></span>  | <span data-ttu-id="2fef2-1762">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1763">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1763">Count</span></span> | <span data-ttu-id="2fef2-1764">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="2fef2-1765">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="2fef2-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="2fef2-1766">Tabla de luminancia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1766">Luminance table.</span></span> <span data-ttu-id="2fef2-1767">La tabla luminancia y la tabla crominancia se utilizan para controlar la calidad JPEG.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="2fef2-1768">Una tabla de luminancia o crominancia válida tiene 64 entradas de tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="2fef2-1769">Si una imagen tiene una tabla de luminancia o una tabla de crominancia, debe tener ambas tablas.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="2fef2-1770">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1770">Property info</span></span> | <span data-ttu-id="2fef2-1771">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1772">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1772">Tag</span></span>   | <span data-ttu-id="2fef2-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="2fef2-1773">0x5090</span></span>               |
| <span data-ttu-id="2fef2-1774">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1774">Type</span></span>  | <span data-ttu-id="2fef2-1775">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1776">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1776">Count</span></span> | <span data-ttu-id="2fef2-1777">64</span><span class="sxs-lookup"><span data-stu-id="2fef2-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="2fef2-1778">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="2fef2-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="2fef2-1779">Tabla de crominancia.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1779">Chrominance table.</span></span> <span data-ttu-id="2fef2-1780">La tabla luminancia y la tabla crominancia se utilizan para controlar la calidad JPEG.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="2fef2-1781">Una tabla de luminancia o crominancia válida tiene 64 entradas de tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="2fef2-1782">Si una imagen tiene una tabla de luminancia o una tabla de crominancia, debe tener ambas tablas.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="2fef2-1783">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1783">Property info</span></span> | <span data-ttu-id="2fef2-1784">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1785">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1785">Tag</span></span>   | <span data-ttu-id="2fef2-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="2fef2-1786">0x5091</span></span>               |
| <span data-ttu-id="2fef2-1787">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1787">Type</span></span>  | <span data-ttu-id="2fef2-1788">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1789">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1789">Count</span></span> | <span data-ttu-id="2fef2-1790">64</span><span class="sxs-lookup"><span data-stu-id="2fef2-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="2fef2-1791">PropertyTagFrameDelay</span><span class="sxs-lookup"><span data-stu-id="2fef2-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="2fef2-1792">Tiempo de retardo, en centésimas de segundo, entre dos marcos en una imagen GIF animada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="2fef2-1793">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1793">Property info</span></span> | <span data-ttu-id="2fef2-1794">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="2fef2-1795">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1795">Tag</span></span>   | <span data-ttu-id="2fef2-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="2fef2-1796">0x5100</span></span>                        |
| <span data-ttu-id="2fef2-1797">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1797">Type</span></span>  | <span data-ttu-id="2fef2-1798">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="2fef2-1799">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1799">Count</span></span> | <span data-ttu-id="2fef2-1800">Número de fotogramas de la imagen</span><span class="sxs-lookup"><span data-stu-id="2fef2-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="2fef2-1801">PropertyTagLoopCount</span><span class="sxs-lookup"><span data-stu-id="2fef2-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="2fef2-1802">En el caso de una imagen GIF animada, el número de veces que se va a mostrar la animación.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="2fef2-1803">Un valor de 0 especifica que la animación debe mostrarse infinitamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="2fef2-1804">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1804">Property info</span></span> | <span data-ttu-id="2fef2-1805">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1806">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1806">Tag</span></span>   | <span data-ttu-id="2fef2-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="2fef2-1807">0x5101</span></span>               |
| <span data-ttu-id="2fef2-1808">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1808">Type</span></span>  | <span data-ttu-id="2fef2-1809">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1810">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1810">Count</span></span> | <span data-ttu-id="2fef2-1811">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="2fef2-1812">PropertyTagGlobalPalette</span><span class="sxs-lookup"><span data-stu-id="2fef2-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="2fef2-1813">Paleta de colores para un mapa de bits indizado en una imagen GIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="2fef2-1814">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1814">Property info</span></span> | <span data-ttu-id="2fef2-1815">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="2fef2-1816">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1816">Tag</span></span>   | <span data-ttu-id="2fef2-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="2fef2-1817">0x5102</span></span>                        |
| <span data-ttu-id="2fef2-1818">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1818">Type</span></span>  | <span data-ttu-id="2fef2-1819">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="2fef2-1820">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1820">Count</span></span> | <span data-ttu-id="2fef2-1821">3 x número de entradas de la paleta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="2fef2-1822">PropertyTagIndexBackground</span><span class="sxs-lookup"><span data-stu-id="2fef2-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="2fef2-1823">Índice del color de fondo de la paleta de una imagen GIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="2fef2-1824">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1824">Property info</span></span> | <span data-ttu-id="2fef2-1825">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1826">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1826">Tag</span></span>   | <span data-ttu-id="2fef2-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="2fef2-1827">0x5103</span></span>              |
| <span data-ttu-id="2fef2-1828">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1828">Type</span></span>  | <span data-ttu-id="2fef2-1829">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-1830">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1830">Count</span></span> | <span data-ttu-id="2fef2-1831">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="2fef2-1832">PropertyTagIndexTransparent</span><span class="sxs-lookup"><span data-stu-id="2fef2-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="2fef2-1833">Índice del color transparente en la paleta de una imagen GIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="2fef2-1834">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1834">Property info</span></span> | <span data-ttu-id="2fef2-1835">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1836">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1836">Tag</span></span>   | <span data-ttu-id="2fef2-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="2fef2-1837">0x5104</span></span>              |
| <span data-ttu-id="2fef2-1838">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1838">Type</span></span>  | <span data-ttu-id="2fef2-1839">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="2fef2-1840">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1840">Count</span></span> | <span data-ttu-id="2fef2-1841">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="2fef2-1842">PropertyTagPixelUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="2fef2-1843">Unidad para PropertyTagPixelPerUnitX y PropertyTagPixelPerUnitY.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="2fef2-1844">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1844">Tag</span></span>

<span data-ttu-id="2fef2-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="2fef2-1845">0x5110</span></span>

<span data-ttu-id="2fef2-1846">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1846">Type</span></span>

<span data-ttu-id="2fef2-1847">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="2fef2-1848">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1848">Count</span></span>

<span data-ttu-id="2fef2-1849">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1849">1</span></span>

<span data-ttu-id="2fef2-1850">0: desconocido</span><span class="sxs-lookup"><span data-stu-id="2fef2-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="2fef2-1851">PropertyTagPixelPerUnitX</span><span class="sxs-lookup"><span data-stu-id="2fef2-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="2fef2-1852">Píxeles por unidad en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="2fef2-1853">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1853">Property info</span></span> | <span data-ttu-id="2fef2-1854">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1855">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1855">Tag</span></span>   | <span data-ttu-id="2fef2-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="2fef2-1856">0x5111</span></span>              |
| <span data-ttu-id="2fef2-1857">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1857">Type</span></span>  | <span data-ttu-id="2fef2-1858">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1859">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1859">Count</span></span> | <span data-ttu-id="2fef2-1860">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="2fef2-1861">PropertyTagPixelPerUnitY</span><span class="sxs-lookup"><span data-stu-id="2fef2-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="2fef2-1862">Píxeles por unidad en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="2fef2-1863">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1863">Property info</span></span> | <span data-ttu-id="2fef2-1864">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1865">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1865">Tag</span></span>   | <span data-ttu-id="2fef2-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="2fef2-1866">0x5112</span></span>              |
| <span data-ttu-id="2fef2-1867">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1867">Type</span></span>  | <span data-ttu-id="2fef2-1868">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1869">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1869">Count</span></span> | <span data-ttu-id="2fef2-1870">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="2fef2-1871">PropertyTagPaletteHistogram</span><span class="sxs-lookup"><span data-stu-id="2fef2-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="2fef2-1872">Histograma de la paleta.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1872">Palette histogram.</span></span>



| <span data-ttu-id="2fef2-1873">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1873">Property info</span></span> | <span data-ttu-id="2fef2-1874">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1875">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1875">Tag</span></span>   | <span data-ttu-id="2fef2-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="2fef2-1876">0x5113</span></span>                  |
| <span data-ttu-id="2fef2-1877">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1877">Type</span></span>  | <span data-ttu-id="2fef2-1878">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="2fef2-1879">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1879">Count</span></span> | <span data-ttu-id="2fef2-1880">Longitud del histograma</span><span class="sxs-lookup"><span data-stu-id="2fef2-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="2fef2-1881">PropertyTagCopyright</span><span class="sxs-lookup"><span data-stu-id="2fef2-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="2fef2-1882">Cadena de caracteres terminada en null que contiene información de copyright.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="2fef2-1883">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1883">Property info</span></span> | <span data-ttu-id="2fef2-1884">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1885">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1885">Tag</span></span>   | <span data-ttu-id="2fef2-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="2fef2-1886">0x8298</span></span>                                             |
| <span data-ttu-id="2fef2-1887">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1887">Type</span></span>  | <span data-ttu-id="2fef2-1888">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1889">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1889">Count</span></span> | <span data-ttu-id="2fef2-1890">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="2fef2-1891">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="2fef2-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="2fef2-1892">Tiempo de exposición, medido en segundos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="2fef2-1893">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1893">Property info</span></span> | <span data-ttu-id="2fef2-1894">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-1895">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1895">Tag</span></span>   | <span data-ttu-id="2fef2-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="2fef2-1896">0x829A</span></span>                  |
| <span data-ttu-id="2fef2-1897">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1897">Type</span></span>  | <span data-ttu-id="2fef2-1898">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-1899">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1899">Count</span></span> | <span data-ttu-id="2fef2-1900">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="2fef2-1901">PropertyTagExifFNumber</span><span class="sxs-lookup"><span data-stu-id="2fef2-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="2fef2-1902">F número.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1902">F number.</span></span>



| <span data-ttu-id="2fef2-1903">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1903">Property info</span></span> | <span data-ttu-id="2fef2-1904">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="2fef2-1905">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1905">Tag</span></span>   | <span data-ttu-id="2fef2-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="2fef2-1906">0x829D</span></span>   |
| <span data-ttu-id="2fef2-1907">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1907">Type</span></span>  | <span data-ttu-id="2fef2-1908">LÓGICO</span><span class="sxs-lookup"><span data-stu-id="2fef2-1908">RATIONAL</span></span> |
| <span data-ttu-id="2fef2-1909">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1909">Count</span></span> | <span data-ttu-id="2fef2-1910">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="2fef2-1911">PropertyTagExifIFD</span><span class="sxs-lookup"><span data-stu-id="2fef2-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="2fef2-1912">Etiqueta privada utilizada por GDI+.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="2fef2-1913">No disponible para uso público.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1913">Not for public use.</span></span> <span data-ttu-id="2fef2-1914">GDI+ utiliza esta etiqueta para buscar información específica de EXIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="2fef2-1915">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1915">Property info</span></span> | <span data-ttu-id="2fef2-1916">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1917">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1917">Tag</span></span>   | <span data-ttu-id="2fef2-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="2fef2-1918">0x8769</span></span>              |
| <span data-ttu-id="2fef2-1919">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1919">Type</span></span>  | <span data-ttu-id="2fef2-1920">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1921">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1921">Count</span></span> | <span data-ttu-id="2fef2-1922">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="2fef2-1923">PropertyTagICCProfile</span><span class="sxs-lookup"><span data-stu-id="2fef2-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="2fef2-1924">Perfil ICC incrustado en la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="2fef2-1925">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1925">Property info</span></span> | <span data-ttu-id="2fef2-1926">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="2fef2-1927">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1927">Tag</span></span>   | <span data-ttu-id="2fef2-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="2fef2-1928">0x8773</span></span>                |
| <span data-ttu-id="2fef2-1929">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1929">Type</span></span>  | <span data-ttu-id="2fef2-1930">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="2fef2-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="2fef2-1931">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1931">Count</span></span> | <span data-ttu-id="2fef2-1932">Longitud del perfil</span><span class="sxs-lookup"><span data-stu-id="2fef2-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="2fef2-1933">PropertyTagExifExposureProg</span><span class="sxs-lookup"><span data-stu-id="2fef2-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="2fef2-1934">Clase del programa que usa la cámara para establecer la exposición cuando se toma la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="2fef2-1935">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1935">Tag</span></span>

<span data-ttu-id="2fef2-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="2fef2-1936">0x8822</span></span>

<span data-ttu-id="2fef2-1937">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1937">Type</span></span>

<span data-ttu-id="2fef2-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="2fef2-1938">SHORT</span></span>

<span data-ttu-id="2fef2-1939">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1939">Count</span></span>

<span data-ttu-id="2fef2-1940">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1940">1</span></span>

<span data-ttu-id="2fef2-1941">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-1941">Default</span></span>

<span data-ttu-id="2fef2-1942">0</span><span class="sxs-lookup"><span data-stu-id="2fef2-1942">0</span></span>

<span data-ttu-id="2fef2-1943">0-no definido 1-manual 2-programa normal 3-apertura prioridad 4-valor de obturación 5-Programa creativo (sesgado hacia la profundidad de campo) 6-Action Program (sesgado hacia la velocidad rápida). velocidad de obturación) 7: modo vertical (para las fotografías de primer plano con el fondo desenfocado) en modo de 8 horizontal (para las fotos horizontales con el foco de fondo) de 9 a 255: reservado</span><span class="sxs-lookup"><span data-stu-id="2fef2-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="2fef2-1944">PropertyTagExifSpectralSense</span><span class="sxs-lookup"><span data-stu-id="2fef2-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="2fef2-1945">Cadena de caracteres terminada en null que especifica la sensibilidad espectral de cada canal de la cámara utilizada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="2fef2-1946">La cadena es compatible con el estándar desarrollado por el Comité técnico de ASTM.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="2fef2-1947">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1947">Property info</span></span> | <span data-ttu-id="2fef2-1948">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-1949">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1949">Tag</span></span>   | <span data-ttu-id="2fef2-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="2fef2-1950">0x8824</span></span>                                             |
| <span data-ttu-id="2fef2-1951">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1951">Type</span></span>  | <span data-ttu-id="2fef2-1952">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-1953">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1953">Count</span></span> | <span data-ttu-id="2fef2-1954">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="2fef2-1955">PropertyTagGpsIFD</span><span class="sxs-lookup"><span data-stu-id="2fef2-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="2fef2-1956">Desplazamiento a un bloque de elementos de propiedad GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="2fef2-1957">Los elementos de propiedad cuyas etiquetas tienen el prefijo PropertyTagGps se almacenan en el bloque de GPS.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="2fef2-1958">Los elementos de propiedad de GPS se definen en la especificación EXIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="2fef2-1959">GDI+ utiliza esta etiqueta para buscar información GPS, pero GDI+ no expone esta etiqueta para su uso público.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="2fef2-1960">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1960">Property info</span></span> | <span data-ttu-id="2fef2-1961">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-1962">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1962">Tag</span></span>   | <span data-ttu-id="2fef2-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="2fef2-1963">0x8825</span></span>              |
| <span data-ttu-id="2fef2-1964">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1964">Type</span></span>  | <span data-ttu-id="2fef2-1965">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-1966">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1966">Count</span></span> | <span data-ttu-id="2fef2-1967">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="2fef2-1968">PropertyTagExifISOSpeed</span><span class="sxs-lookup"><span data-stu-id="2fef2-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="2fef2-1969">Velocidad ISO e ISO latitud de la cámara o dispositivo de entrada tal y como se especifica en ISO 12232.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="2fef2-1970">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1970">Property info</span></span> | <span data-ttu-id="2fef2-1971">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-1972">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1972">Tag</span></span>   | <span data-ttu-id="2fef2-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="2fef2-1973">0x8827</span></span>               |
| <span data-ttu-id="2fef2-1974">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1974">Type</span></span>  | <span data-ttu-id="2fef2-1975">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-1976">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1976">Count</span></span> | <span data-ttu-id="2fef2-1977">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="2fef2-1978">PropertyTagExifOECF</span><span class="sxs-lookup"><span data-stu-id="2fef2-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="2fef2-1979">Función de conversión Optoelectronic (OECF) especificada en ISO 14524.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="2fef2-1980">OECF es la relación entre los valores de entrada óptica de cámara y de imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="2fef2-1981">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1981">Property info</span></span> | <span data-ttu-id="2fef2-1982">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-1983">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1983">Tag</span></span>   | <span data-ttu-id="2fef2-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="2fef2-1984">0x8828</span></span>                   |
| <span data-ttu-id="2fef2-1985">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1985">Type</span></span>  | <span data-ttu-id="2fef2-1986">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-1987">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-1987">Count</span></span> | <span data-ttu-id="2fef2-1988">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="2fef2-1989">PropertyTagExifVer</span><span class="sxs-lookup"><span data-stu-id="2fef2-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="2fef2-1990">Versión del estándar EXIF compatible.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="2fef2-1991">La no existencia de este campo se toma para hacer referencia a la no conformidad con el estándar.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="2fef2-1992">La conformidad con el estándar se indica grabando 0210 como una cadena ASCII de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="2fef2-1993">Dado que el tipo es PropertyTagTypeUndefined, no hay ningún terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="2fef2-1994">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-1994">Property info</span></span> | <span data-ttu-id="2fef2-1995">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="2fef2-1996">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-1996">Tag</span></span>     | <span data-ttu-id="2fef2-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="2fef2-1997">0x9000</span></span>                   |
| <span data-ttu-id="2fef2-1998">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-1998">Type</span></span>    | <span data-ttu-id="2fef2-1999">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2000">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2000">Count</span></span>   | <span data-ttu-id="2fef2-2001">4</span><span class="sxs-lookup"><span data-stu-id="2fef2-2001">4</span></span>                        |
| <span data-ttu-id="2fef2-2002">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2002">Default</span></span> | <span data-ttu-id="2fef2-2003">0210</span><span class="sxs-lookup"><span data-stu-id="2fef2-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="2fef2-2004">PropertyTagExifDTOrig</span><span class="sxs-lookup"><span data-stu-id="2fef2-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="2fef2-2005">Fecha y hora en que se generaron los datos de imagen originales.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="2fef2-2006">Para un DSC, la fecha y la hora en que se tomó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="2fef2-2007">El formato es AAAA: MM: DD HH: MM: SS con la hora que se muestra en formato de 24 horas y la fecha y hora separadas por un carácter en blanco (0x2000).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="2fef2-2008">La longitud de la cadena de caracteres es de 20 bytes, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="2fef2-2009">Cuando el campo está vacío, se trata como desconocido.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="2fef2-2010">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2010">Property info</span></span> | <span data-ttu-id="2fef2-2011">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-2012">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2012">Tag</span></span>   | <span data-ttu-id="2fef2-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="2fef2-2013">0x9003</span></span>               |
| <span data-ttu-id="2fef2-2014">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2014">Type</span></span>  | <span data-ttu-id="2fef2-2015">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-2016">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2016">Count</span></span> | <span data-ttu-id="2fef2-2017">20</span><span class="sxs-lookup"><span data-stu-id="2fef2-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="2fef2-2018">PropertyTagExifDTDigitized</span><span class="sxs-lookup"><span data-stu-id="2fef2-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="2fef2-2019">Fecha y hora en que se almacenó la imagen como datos digitales.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="2fef2-2020">Por ejemplo, si DSC ha capturado una imagen y, al mismo tiempo, se grabó el archivo, DateTimeOriginal y DateTimeDigitized tendrán el mismo contenido.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="2fef2-2021">El formato es AAAA: MM: DD HH: MM: SS con la hora que se muestra en formato de 24 horas y la fecha y hora separadas por un carácter en blanco (0x2000).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="2fef2-2022">La longitud de la cadena de caracteres es de 20 bytes, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="2fef2-2023">Cuando el campo está vacío, se trata como desconocido.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="2fef2-2024">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2024">Property info</span></span> | <span data-ttu-id="2fef2-2025">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-2026">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2026">Tag</span></span>   | <span data-ttu-id="2fef2-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="2fef2-2027">0x9004</span></span>               |
| <span data-ttu-id="2fef2-2028">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2028">Type</span></span>  | <span data-ttu-id="2fef2-2029">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-2030">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2030">Count</span></span> | <span data-ttu-id="2fef2-2031">20</span><span class="sxs-lookup"><span data-stu-id="2fef2-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="2fef2-2032">PropertyTagExifCompConfig</span><span class="sxs-lookup"><span data-stu-id="2fef2-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="2fef2-2033">Información específica de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2033">Information specific to compressed data.</span></span> <span data-ttu-id="2fef2-2034">Los canales de cada componente se organizan en orden desde el primer componente hasta el cuarto.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="2fef2-2035">En el caso de los datos sin comprimir, la organización de datos se proporciona en la etiqueta PropertyTagPhotometricInterp.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="2fef2-2036">Sin embargo, dado que PropertyTagPhotometricInterp solo puede expresar el orden de Y, CB y CR, esta etiqueta se proporciona para los casos en los que los datos comprimidos usan componentes distintos de Y, CB y CR, y para admitir otras secuencias.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="2fef2-2037">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2037">Tag</span></span>

<span data-ttu-id="2fef2-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="2fef2-2038">0x9101</span></span>

<span data-ttu-id="2fef2-2039">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2039">Type</span></span>

<span data-ttu-id="2fef2-2040">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="2fef2-2041">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2041">Count</span></span>

<span data-ttu-id="2fef2-2042">4</span><span class="sxs-lookup"><span data-stu-id="2fef2-2042">4</span></span>

<span data-ttu-id="2fef2-2043">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2043">Default</span></span>

<span data-ttu-id="2fef2-2044">4 5 6 0 (si RGB no comprimido) 1 2 3 0 (otros casos)</span><span class="sxs-lookup"><span data-stu-id="2fef2-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="2fef2-2045">0: no existe 1-Y 2-CB 3-CR 4-R 5-G 6-B Other-Reserved</span><span class="sxs-lookup"><span data-stu-id="2fef2-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="2fef2-2046">PropertyTagExifCompBPP</span><span class="sxs-lookup"><span data-stu-id="2fef2-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="2fef2-2047">Información específica de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2047">Information specific to compressed data.</span></span> <span data-ttu-id="2fef2-2048">El modo de compresión utilizado para una imagen comprimida se indica en unidad BPP.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="2fef2-2049">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2049">Property info</span></span> | <span data-ttu-id="2fef2-2050">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2051">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2051">Tag</span></span>   | <span data-ttu-id="2fef2-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="2fef2-2052">0x9102</span></span>                  |
| <span data-ttu-id="2fef2-2053">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2053">Type</span></span>  | <span data-ttu-id="2fef2-2054">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2055">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2055">Count</span></span> | <span data-ttu-id="2fef2-2056">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="2fef2-2057">PropertyTagExifShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="2fef2-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="2fef2-2058">Velocidad del obturador.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2058">Shutter speed.</span></span> <span data-ttu-id="2fef2-2059">La unidad es el sistema aditivo de valor de exposición fotográfica (vértice).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="2fef2-2060">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2060">Property info</span></span> | <span data-ttu-id="2fef2-2061">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2062">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2062">Tag</span></span>   | <span data-ttu-id="2fef2-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="2fef2-2063">0x9201</span></span>                   |
| <span data-ttu-id="2fef2-2064">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2064">Type</span></span>  | <span data-ttu-id="2fef2-2065">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="2fef2-2066">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2066">Count</span></span> | <span data-ttu-id="2fef2-2067">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="2fef2-2068">PropertyTagExifAperture</span><span class="sxs-lookup"><span data-stu-id="2fef2-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="2fef2-2069">Abertura de la lente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2069">Lens aperture.</span></span> <span data-ttu-id="2fef2-2070">La unidad es el valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="2fef2-2071">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2071">Property info</span></span> | <span data-ttu-id="2fef2-2072">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2073">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2073">Tag</span></span>   | <span data-ttu-id="2fef2-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="2fef2-2074">0x9202</span></span>                  |
| <span data-ttu-id="2fef2-2075">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2075">Type</span></span>  | <span data-ttu-id="2fef2-2076">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2077">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2077">Count</span></span> | <span data-ttu-id="2fef2-2078">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="2fef2-2079">PropertyTagExifBrightness</span><span class="sxs-lookup"><span data-stu-id="2fef2-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="2fef2-2080">Valor de brillo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2080">Brightness value.</span></span> <span data-ttu-id="2fef2-2081">La unidad es el valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2081">The unit is the APEX value.</span></span> <span data-ttu-id="2fef2-2082">Normalmente, se proporciona en el intervalo de-99,99 a 99,99.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="2fef2-2083">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2083">Property info</span></span> | <span data-ttu-id="2fef2-2084">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2085">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2085">Tag</span></span>   | <span data-ttu-id="2fef2-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="2fef2-2086">0x9203</span></span>                   |
| <span data-ttu-id="2fef2-2087">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2087">Type</span></span>  | <span data-ttu-id="2fef2-2088">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="2fef2-2089">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2089">Count</span></span> | <span data-ttu-id="2fef2-2090">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="2fef2-2091">PropertyTagExifExposureBias</span><span class="sxs-lookup"><span data-stu-id="2fef2-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="2fef2-2092">Tendencia de exposición.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2092">Exposure bias.</span></span> <span data-ttu-id="2fef2-2093">La unidad es el valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2093">The unit is the APEX value.</span></span> <span data-ttu-id="2fef2-2094">Normalmente, se proporciona en el intervalo de-99,99 a 99,99.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="2fef2-2095">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2095">Property info</span></span> | <span data-ttu-id="2fef2-2096">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2097">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2097">Tag</span></span>   | <span data-ttu-id="2fef2-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="2fef2-2098">0x9204</span></span>                   |
| <span data-ttu-id="2fef2-2099">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2099">Type</span></span>  | <span data-ttu-id="2fef2-2100">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="2fef2-2101">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2101">Count</span></span> | <span data-ttu-id="2fef2-2102">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="2fef2-2103">PropertyTagExifMaxAperture</span><span class="sxs-lookup"><span data-stu-id="2fef2-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="2fef2-2104">Número F más pequeño de la lente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="2fef2-2105">La unidad es el valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2105">The unit is the APEX value.</span></span> <span data-ttu-id="2fef2-2106">Normalmente, se proporciona en el intervalo de 00,00 a 99,99, pero no se limita a este intervalo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="2fef2-2107">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2107">Property info</span></span> | <span data-ttu-id="2fef2-2108">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2109">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2109">Tag</span></span>   | <span data-ttu-id="2fef2-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="2fef2-2110">0x9205</span></span>                  |
| <span data-ttu-id="2fef2-2111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2111">Type</span></span>  | <span data-ttu-id="2fef2-2112">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2113">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2113">Count</span></span> | <span data-ttu-id="2fef2-2114">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="2fef2-2115">PropertyTagExifSubjectDist</span><span class="sxs-lookup"><span data-stu-id="2fef2-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="2fef2-2116">Distancia al asunto, medida en metros.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="2fef2-2117">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2117">Property info</span></span> | <span data-ttu-id="2fef2-2118">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2119">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2119">Tag</span></span>   | <span data-ttu-id="2fef2-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="2fef2-2120">0x9206</span></span>                  |
| <span data-ttu-id="2fef2-2121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2121">Type</span></span>  | <span data-ttu-id="2fef2-2122">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2123">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2123">Count</span></span> | <span data-ttu-id="2fef2-2124">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="2fef2-2125">PropertyTagExifMeteringMode</span><span class="sxs-lookup"><span data-stu-id="2fef2-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="2fef2-2126">Modo de medición.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2126">Metering mode.</span></span>



<span data-ttu-id="2fef2-2127">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2127">Tag</span></span>

<span data-ttu-id="2fef2-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="2fef2-2128">0x9207</span></span>

<span data-ttu-id="2fef2-2129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2129">Type</span></span>

<span data-ttu-id="2fef2-2130">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2131">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2131">Count</span></span>

<span data-ttu-id="2fef2-2132">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2132">1</span></span>

<span data-ttu-id="2fef2-2133">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2133">Default</span></span>

<span data-ttu-id="2fef2-2134">0</span><span class="sxs-lookup"><span data-stu-id="2fef2-2134">0</span></span>

<span data-ttu-id="2fef2-2135">0-desconocido 1-promedio 2-CenterWeightedAverage 3-punto 4-multiposición 5-patrón 6-parcial 7 a 254-reservado 255-otro</span><span class="sxs-lookup"><span data-stu-id="2fef2-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="2fef2-2136">PropertyTagExifLightSource</span><span class="sxs-lookup"><span data-stu-id="2fef2-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="2fef2-2137">Tipo de fuente de luz.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2137">Type of light source.</span></span>



<span data-ttu-id="2fef2-2138">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2138">Tag</span></span>

<span data-ttu-id="2fef2-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="2fef2-2139">0x9208</span></span>

<span data-ttu-id="2fef2-2140">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2140">Type</span></span>

<span data-ttu-id="2fef2-2141">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2142">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2142">Count</span></span>

<span data-ttu-id="2fef2-2143">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2143">1</span></span>

<span data-ttu-id="2fef2-2144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2144">Default</span></span>

<span data-ttu-id="2fef2-2145">0</span><span class="sxs-lookup"><span data-stu-id="2fef2-2145">0</span></span>

<span data-ttu-id="2fef2-2146">0-desconocido 1-horario de verano 2-Flourescent 3-Tungsten 17-luz estándar A 18-estándar Light B 19-estándar claro C 20-D55 21-D65 22-D75 23 a 254-reservado 255-otro</span><span class="sxs-lookup"><span data-stu-id="2fef2-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="2fef2-2147">PropertyTagExifFlash</span><span class="sxs-lookup"><span data-stu-id="2fef2-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="2fef2-2148">Estado de Flash.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2148">Flash status.</span></span> <span data-ttu-id="2fef2-2149">Esta etiqueta se registra cuando se toma una imagen mediante una luz estroboscópica (Flash).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="2fef2-2150">Bit 0 indica el estado de activación de Flash y los bits 1 y 2 indican el estado de retorno de Flash.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="2fef2-2151">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2151">Tag</span></span>

<span data-ttu-id="2fef2-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="2fef2-2152">0x9209</span></span>

<span data-ttu-id="2fef2-2153">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2153">Type</span></span>

<span data-ttu-id="2fef2-2154">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2155">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2155">Count</span></span>

<span data-ttu-id="2fef2-2156">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2156">1</span></span>

<span data-ttu-id="2fef2-2157">Valores de bit 0 que indican si el flash activado: 0B-Flash no se ha desencadenado 1B-flash activado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="2fef2-2158">Valores de los bits 1 y 2 que indican el estado de devuelto Light: 00B-no se detectó la función de detección de devoluciones estroboscópica 01B-Reserved 10B-luz de retorno de luz estroboscópica no detectada 11b-luz de retorno de luz estroboscópica detectada</span><span class="sxs-lookup"><span data-stu-id="2fef2-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="2fef2-2159">Valores de etiqueta Flash resultantes: 0x0000-Flash no activó 0x0001-Flash 0x0005-luz de retorno de luz estroboscópica no detectada</span><span class="sxs-lookup"><span data-stu-id="2fef2-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="2fef2-2160">PropertyTagExifFocalLength</span><span class="sxs-lookup"><span data-stu-id="2fef2-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="2fef2-2161">La longitud focal real, en milímetros, de la lente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="2fef2-2162">La conversión no se realiza en la longitud focal de una cámara de película 35 milímetros.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="2fef2-2163">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2163">Property info</span></span> | <span data-ttu-id="2fef2-2164">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2165">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2165">Tag</span></span>   | <span data-ttu-id="2fef2-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="2fef2-2166">0x920A</span></span>                  |
| <span data-ttu-id="2fef2-2167">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2167">Type</span></span>  | <span data-ttu-id="2fef2-2168">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2169">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2169">Count</span></span> | <span data-ttu-id="2fef2-2170">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="2fef2-2171">PropertyTagExifMakerNote</span><span class="sxs-lookup"><span data-stu-id="2fef2-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="2fef2-2172">Etiqueta de nota.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2172">Note tag.</span></span> <span data-ttu-id="2fef2-2173">Etiqueta utilizada por los fabricantes de escritores EXIF para registrar información.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="2fef2-2174">El contenido depende del fabricante.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="2fef2-2175">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2175">Property info</span></span> | <span data-ttu-id="2fef2-2176">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2177">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2177">Tag</span></span>   | <span data-ttu-id="2fef2-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="2fef2-2178">0x927C</span></span>                   |
| <span data-ttu-id="2fef2-2179">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2179">Type</span></span>  | <span data-ttu-id="2fef2-2180">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2181">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2181">Count</span></span> | <span data-ttu-id="2fef2-2182">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="2fef2-2183">PropertyTagExifUserComment</span><span class="sxs-lookup"><span data-stu-id="2fef2-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="2fef2-2184">Etiqueta de comentario.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2184">Comment tag.</span></span> <span data-ttu-id="2fef2-2185">Una etiqueta utilizada por los usuarios EXIF para escribir palabras clave o comentarios sobre la imagen, además de los de PropertyTagImageDescription y sin las limitaciones de código de carácter de la etiqueta PropertyTagImageDescription.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="2fef2-2186">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2186">Property info</span></span> | <span data-ttu-id="2fef2-2187">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2188">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2188">Tag</span></span>   | <span data-ttu-id="2fef2-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="2fef2-2189">0x9286</span></span>                   |
| <span data-ttu-id="2fef2-2190">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2190">Type</span></span>  | <span data-ttu-id="2fef2-2191">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2192">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2192">Count</span></span> | <span data-ttu-id="2fef2-2193">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-2193">Any</span></span>                      |



 

<span data-ttu-id="2fef2-2194">El código de carácter que se usa en la etiqueta PropertyTagExifUserComment se identifica en función de un código de identificador en un área fija de 8 bytes al principio del área de datos de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="2fef2-2195">La parte no utilizada del área se rellena con caracteres nulos (0).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="2fef2-2196">Los códigos de identificador se asignan por medio del registro.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="2fef2-2197">Dado que el tipo no es ASCII, no es necesario utilizar un terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="2fef2-2198">PropertyTagExifDTSubsec</span><span class="sxs-lookup"><span data-stu-id="2fef2-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="2fef2-2199">Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagDateTime.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="2fef2-2200">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2200">Property info</span></span> | <span data-ttu-id="2fef2-2201">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="2fef2-2202">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2202">Tag</span></span>   | <span data-ttu-id="2fef2-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="2fef2-2203">0x9290</span></span>                                             |
| <span data-ttu-id="2fef2-2204">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2204">Type</span></span>  | <span data-ttu-id="2fef2-2205">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-2206">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2206">Count</span></span> | <span data-ttu-id="2fef2-2207">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="2fef2-2208">PropertyTagExifDTOrigSS</span><span class="sxs-lookup"><span data-stu-id="2fef2-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="2fef2-2209">Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagExifDTOrig.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="2fef2-2210">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2210">Property info</span></span> | <span data-ttu-id="2fef2-2211">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="2fef2-2212">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2212">Tag</span></span>  | <span data-ttu-id="2fef2-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="2fef2-2213">0x9291</span></span>                                             |
| <span data-ttu-id="2fef2-2214">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2214">Type</span></span> | <span data-ttu-id="2fef2-2215">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="2fef2-2216">N</span><span class="sxs-lookup"><span data-stu-id="2fef2-2216">N</span></span>    | <span data-ttu-id="2fef2-2217">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="2fef2-2218">PropertyTagExifDTDigSS</span><span class="sxs-lookup"><span data-stu-id="2fef2-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="2fef2-2219">Cadena de caracteres terminada en null que especifica una fracción de segundo para la etiqueta PropertyTagExifDTDigitized.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="2fef2-2220">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2220">Property info</span></span> | <span data-ttu-id="2fef2-2221">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="2fef2-2222">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2222">Tag</span></span>  | <span data-ttu-id="2fef2-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="2fef2-2223">0x9292</span></span>                                             |
| <span data-ttu-id="2fef2-2224">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2224">Type</span></span> | <span data-ttu-id="2fef2-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2225">ASCII</span></span>                                              |
| <span data-ttu-id="2fef2-2226">N</span><span class="sxs-lookup"><span data-stu-id="2fef2-2226">N</span></span>    | <span data-ttu-id="2fef2-2227">Longitud de la cadena, incluido el terminador NULL</span><span class="sxs-lookup"><span data-stu-id="2fef2-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="2fef2-2228">PropertyTagExifFPXVer</span><span class="sxs-lookup"><span data-stu-id="2fef2-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="2fef2-2229">Versión de formato de FlashPix compatible con un archivo FPXR.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="2fef2-2230">Si la función FPXR admite el formato de FlashPix versión 1,0, esto se indica de forma similar a PropertyTagExifVer grabando 0100 como una cadena ASCII de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="2fef2-2231">Dado que el tipo es PropertyTagTypeUndefined, no hay ningún terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="2fef2-2232">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2232">Tag</span></span>

<span data-ttu-id="2fef2-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="2fef2-2233">0xA000</span></span>

<span data-ttu-id="2fef2-2234">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2234">Type</span></span>

<span data-ttu-id="2fef2-2235">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="2fef2-2236">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2236">Count</span></span>

<span data-ttu-id="2fef2-2237">4</span><span class="sxs-lookup"><span data-stu-id="2fef2-2237">4</span></span>

<span data-ttu-id="2fef2-2238">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2238">Default</span></span>

<span data-ttu-id="2fef2-2239">0100</span><span class="sxs-lookup"><span data-stu-id="2fef2-2239">0100</span></span>

<span data-ttu-id="2fef2-2240">0100: formato FlashPix versión 1,0 otros: reservados</span><span class="sxs-lookup"><span data-stu-id="2fef2-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="2fef2-2241">PropertyTagExifColorSpace</span><span class="sxs-lookup"><span data-stu-id="2fef2-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="2fef2-2242">Especificador de espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2242">Color space specifier.</span></span> <span data-ttu-id="2fef2-2243">Normalmente, sRGB (= 1) se usa para definir el espacio de colores en función del entorno y las condiciones del monitor de PC.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="2fef2-2244">Si se utiliza un espacio de colores distinto de sRGB, se establece sin calibración (= 0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="2fef2-2245">Los datos de imagen grabados como no calibrados se pueden tratar como sRGB cuando se convierten en FlashPix.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="2fef2-2246">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2246">Tag</span></span>

<span data-ttu-id="2fef2-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="2fef2-2247">0xA001</span></span>

<span data-ttu-id="2fef2-2248">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2248">Type</span></span>

<span data-ttu-id="2fef2-2249">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2250">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2250">Count</span></span>

<span data-ttu-id="2fef2-2251">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2251">1</span></span>

<span data-ttu-id="2fef2-2252">0x1-sRGB 0xFFFF-otro no calibrado: reservado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="2fef2-2253">PropertyTagExifPixXDim</span><span class="sxs-lookup"><span data-stu-id="2fef2-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="2fef2-2254">Información específica de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2254">Information specific to compressed data.</span></span> <span data-ttu-id="2fef2-2255">Cuando se graba un archivo comprimido, se debe grabar el ancho válido de la imagen significativa en esta etiqueta, independientemente de si hay datos de relleno o un marcador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="2fef2-2256">Esta etiqueta no debe existir en un archivo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="2fef2-2257">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2257">Property info</span></span> | <span data-ttu-id="2fef2-2258">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-2259">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2259">Tag</span></span>   | <span data-ttu-id="2fef2-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="2fef2-2260">0xA002</span></span>                                      |
| <span data-ttu-id="2fef2-2261">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2261">Type</span></span>  | <span data-ttu-id="2fef2-2262">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-2263">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2263">Count</span></span> | <span data-ttu-id="2fef2-2264">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="2fef2-2265">PropertyTagExifPixYDim</span><span class="sxs-lookup"><span data-stu-id="2fef2-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="2fef2-2266">Información específica de los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2266">Information specific to compressed data.</span></span> <span data-ttu-id="2fef2-2267">Cuando se graba un archivo comprimido, se debe grabar el alto válido de la imagen significativa en esta etiqueta independientemente de si hay datos de relleno o un marcador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="2fef2-2268">Esta etiqueta no debe existir en un archivo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="2fef2-2269">Dado que el relleno de datos no es necesario en la dirección vertical, el número de líneas registradas en esta etiqueta de alto de imagen válida será el mismo que se registró en Soft.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="2fef2-2270">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2270">Property info</span></span> | <span data-ttu-id="2fef2-2271">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="2fef2-2272">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2272">Tag</span></span>   | <span data-ttu-id="2fef2-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="2fef2-2273">0xA003</span></span>                                      |
| <span data-ttu-id="2fef2-2274">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2274">Type</span></span>  | <span data-ttu-id="2fef2-2275">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-2276">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2276">Count</span></span> | <span data-ttu-id="2fef2-2277">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="2fef2-2278">PropertyTagExifRelatedWav</span><span class="sxs-lookup"><span data-stu-id="2fef2-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="2fef2-2279">Nombre de un archivo de audio relacionado con los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="2fef2-2280">La única información relacional registrada es el nombre y la extensión de archivo de audio EXIF (una cadena ASCII que consta de 8 caracteres más un punto (.), más 3 caracteres).</span><span class="sxs-lookup"><span data-stu-id="2fef2-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="2fef2-2281">La ruta de acceso no se registra.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2281">The path is not recorded.</span></span> <span data-ttu-id="2fef2-2282">Cuando se usa esta etiqueta, los archivos de audio deben registrarse de acuerdo con el formato de audio EXIF.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="2fef2-2283">Los escritores también pueden almacenar datos de audio dentro de APP2 como datos de flujo de extensión de FlashPix.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="2fef2-2284">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2284">Property info</span></span> | <span data-ttu-id="2fef2-2285">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-2286">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2286">Tag</span></span>   | <span data-ttu-id="2fef2-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="2fef2-2287">0xA004</span></span>               |
| <span data-ttu-id="2fef2-2288">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2288">Type</span></span>  | <span data-ttu-id="2fef2-2289">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="2fef2-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="2fef2-2290">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2290">Count</span></span> | <span data-ttu-id="2fef2-2291">13</span><span class="sxs-lookup"><span data-stu-id="2fef2-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="2fef2-2292">PropertyTagExifInterop</span><span class="sxs-lookup"><span data-stu-id="2fef2-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="2fef2-2293">Desplazamiento a un bloque de elementos de propiedad que contienen información de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="2fef2-2294">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2294">Property info</span></span> | <span data-ttu-id="2fef2-2295">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="2fef2-2296">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2296">Tag</span></span>   | <span data-ttu-id="2fef2-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="2fef2-2297">0xA005</span></span>              |
| <span data-ttu-id="2fef2-2298">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2298">Type</span></span>  | <span data-ttu-id="2fef2-2299">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="2fef2-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="2fef2-2300">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2300">Count</span></span> | <span data-ttu-id="2fef2-2301">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="2fef2-2302">PropertyTagExifFlashEnergy</span><span class="sxs-lookup"><span data-stu-id="2fef2-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="2fef2-2303">Energía de luz estroboscópica, en la vela de luz de los segundos (BCPS), en el momento en que se capturó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="2fef2-2304">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2304">Property info</span></span> | <span data-ttu-id="2fef2-2305">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2306">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2306">Tag</span></span>   | <span data-ttu-id="2fef2-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="2fef2-2307">0xA20B</span></span>                  |
| <span data-ttu-id="2fef2-2308">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2308">Type</span></span>  | <span data-ttu-id="2fef2-2309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2310">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2310">Count</span></span> | <span data-ttu-id="2fef2-2311">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="2fef2-2312">PropertyTagExifSpatialFR</span><span class="sxs-lookup"><span data-stu-id="2fef2-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="2fef2-2313">Valores de tabla y SFR de frecuencia espacial del dispositivo de entrada y de cámara en el ancho de la imagen, el alto de la imagen y la dirección diagonal, tal como se especifica en ISO 12233.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="2fef2-2314">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2314">Property info</span></span> | <span data-ttu-id="2fef2-2315">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2316">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2316">Tag</span></span>   | <span data-ttu-id="2fef2-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="2fef2-2317">0xA20C</span></span>                   |
| <span data-ttu-id="2fef2-2318">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2318">Type</span></span>  | <span data-ttu-id="2fef2-2319">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2320">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2320">Count</span></span> | <span data-ttu-id="2fef2-2321">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="2fef2-2322">PropertyTagExifFocalXRes</span><span class="sxs-lookup"><span data-stu-id="2fef2-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="2fef2-2323">Número de píxeles en la dirección de ancho de la imagen (x) por unidad en el plano focal de la cámara.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="2fef2-2324">La unidad se especifica en PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="2fef2-2325">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2325">Property info</span></span> | <span data-ttu-id="2fef2-2326">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2327">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2327">Tag</span></span>   | <span data-ttu-id="2fef2-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="2fef2-2328">0xA20E</span></span>                  |
| <span data-ttu-id="2fef2-2329">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2329">Type</span></span>  | <span data-ttu-id="2fef2-2330">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2331">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2331">Count</span></span> | <span data-ttu-id="2fef2-2332">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="2fef2-2333">PropertyTagExifFocalYRes</span><span class="sxs-lookup"><span data-stu-id="2fef2-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="2fef2-2334">Número de píxeles en la dirección de alto (y) de la imagen por unidad en el plano focal de la cámara.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="2fef2-2335">La unidad se especifica en PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="2fef2-2336">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2336">Property info</span></span> | <span data-ttu-id="2fef2-2337">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2338">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2338">Tag</span></span>   | <span data-ttu-id="2fef2-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="2fef2-2339">0xA20F</span></span>                  |
| <span data-ttu-id="2fef2-2340">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2340">Type</span></span>  | <span data-ttu-id="2fef2-2341">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2342">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2342">Count</span></span> | <span data-ttu-id="2fef2-2343">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="2fef2-2344">PropertyTagExifFocalResUnit</span><span class="sxs-lookup"><span data-stu-id="2fef2-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="2fef2-2345">Unidad de medida para PropertyTagExifFocalXRes y PropertyTagExifFocalYRes.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="2fef2-2346">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2346">Tag</span></span>

<span data-ttu-id="2fef2-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="2fef2-2347">0xA210</span></span>

<span data-ttu-id="2fef2-2348">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2348">Type</span></span>

<span data-ttu-id="2fef2-2349">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2350">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2350">Count</span></span>

<span data-ttu-id="2fef2-2351">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2351">1</span></span>

<span data-ttu-id="2fef2-2352">2 pulgadas 3-centímetro</span><span class="sxs-lookup"><span data-stu-id="2fef2-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="2fef2-2353">PropertyTagExifSubjectLoc</span><span class="sxs-lookup"><span data-stu-id="2fef2-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="2fef2-2354">Ubicación del asunto principal de la escena.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="2fef2-2355">El valor de esta etiqueta representa el píxel del centro del asunto principal relativo al borde izquierdo.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="2fef2-2356">El primer valor indica el número de columna y el segundo valor indica el número de fila.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="2fef2-2357">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2357">Property info</span></span> | <span data-ttu-id="2fef2-2358">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="2fef2-2359">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2359">Tag</span></span>   | <span data-ttu-id="2fef2-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="2fef2-2360">0xA214</span></span>               |
| <span data-ttu-id="2fef2-2361">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2361">Type</span></span>  | <span data-ttu-id="2fef2-2362">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="2fef2-2363">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2363">Count</span></span> | <span data-ttu-id="2fef2-2364">2</span><span class="sxs-lookup"><span data-stu-id="2fef2-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="2fef2-2365">PropertyTagExifExposureIndex</span><span class="sxs-lookup"><span data-stu-id="2fef2-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="2fef2-2366">Índice de exposición seleccionado en la cámara o dispositivo de entrada en el momento en que se capturó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="2fef2-2367">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2367">Property info</span></span> | <span data-ttu-id="2fef2-2368">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="2fef2-2369">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2369">Tag</span></span>   | <span data-ttu-id="2fef2-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="2fef2-2370">0xA215</span></span>                  |
| <span data-ttu-id="2fef2-2371">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2371">Type</span></span>  | <span data-ttu-id="2fef2-2372">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="2fef2-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="2fef2-2373">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2373">Count</span></span> | <span data-ttu-id="2fef2-2374">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="2fef2-2375">PropertyTagExifSensingMethod</span><span class="sxs-lookup"><span data-stu-id="2fef2-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="2fef2-2376">Tipo de sensor de imagen en la cámara o dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="2fef2-2377">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2377">Tag</span></span>

<span data-ttu-id="2fef2-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="2fef2-2378">0xA217</span></span>

<span data-ttu-id="2fef2-2379">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2379">Type</span></span>

<span data-ttu-id="2fef2-2380">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="2fef2-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="2fef2-2381">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2381">Count</span></span>

<span data-ttu-id="2fef2-2382">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2382">1</span></span>

<span data-ttu-id="2fef2-2383">1: sensor de área de color de dos chips de 3 a 2: sensor de área de color de dos chips 4-tres-chip sensor de área de color 5-sensor de área 3D de sensor trilineal de 8 colores sensor lineal de color 2-reservado</span><span class="sxs-lookup"><span data-stu-id="2fef2-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="2fef2-2384">PropertyTagExifFileSource</span><span class="sxs-lookup"><span data-stu-id="2fef2-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="2fef2-2385">Origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2385">The image source.</span></span> <span data-ttu-id="2fef2-2386">Si un DSC grabó la imagen, el valor de esta etiqueta es 3.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="2fef2-2387">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2387">Property info</span></span> | <span data-ttu-id="2fef2-2388">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2389">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2389">Tag</span></span>   | <span data-ttu-id="2fef2-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="2fef2-2390">0xA300</span></span>                   |
| <span data-ttu-id="2fef2-2391">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2391">Type</span></span>  | <span data-ttu-id="2fef2-2392">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2393">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2393">Count</span></span> | <span data-ttu-id="2fef2-2394">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="2fef2-2395">PropertyTagExifSceneType</span><span class="sxs-lookup"><span data-stu-id="2fef2-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="2fef2-2396">Tipo de escena.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2396">The type of scene.</span></span> <span data-ttu-id="2fef2-2397">Si un DSC grabó la imagen, el valor de esta etiqueta debe establecerse en 1, lo que indica que la imagen se ha fotografiado directamente.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="2fef2-2398">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2398">Property info</span></span> | <span data-ttu-id="2fef2-2399">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2400">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2400">Tag</span></span>   | <span data-ttu-id="2fef2-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="2fef2-2401">0xA301</span></span>                   |
| <span data-ttu-id="2fef2-2402">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2402">Type</span></span>  | <span data-ttu-id="2fef2-2403">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2404">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2404">Count</span></span> | <span data-ttu-id="2fef2-2405">1</span><span class="sxs-lookup"><span data-stu-id="2fef2-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="2fef2-2406">PropertyTagExifCfaPattern</span><span class="sxs-lookup"><span data-stu-id="2fef2-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="2fef2-2407">El patrón geométrico de matriz de filtro de colores (CFA) del sensor de imagen cuando se usa un sensor de área de color de un solo chip.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="2fef2-2408">No se aplica a todos los métodos de detección.</span><span class="sxs-lookup"><span data-stu-id="2fef2-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="2fef2-2409">Información de propiedad</span><span class="sxs-lookup"><span data-stu-id="2fef2-2409">Property info</span></span> | <span data-ttu-id="2fef2-2410">Value</span><span class="sxs-lookup"><span data-stu-id="2fef2-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="2fef2-2411">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2fef2-2411">Tag</span></span>   | <span data-ttu-id="2fef2-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="2fef2-2412">0xA302</span></span>                   |
| <span data-ttu-id="2fef2-2413">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fef2-2413">Type</span></span>  | <span data-ttu-id="2fef2-2414">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="2fef2-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="2fef2-2415">Count</span><span class="sxs-lookup"><span data-stu-id="2fef2-2415">Count</span></span> | <span data-ttu-id="2fef2-2416">Any</span><span class="sxs-lookup"><span data-stu-id="2fef2-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="2fef2-2417">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fef2-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fef2-2418">Especificaciones de formato de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="2fef2-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="2fef2-2419">Constantes de etiqueta de propiedad de imagen</span><span class="sxs-lookup"><span data-stu-id="2fef2-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="2fef2-2420">**Constantes de tipo de etiqueta de propiedad de imagen**</span><span class="sxs-lookup"><span data-stu-id="2fef2-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="2fef2-2421">Etiquetas de propiedad en orden alfabético</span><span class="sxs-lookup"><span data-stu-id="2fef2-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="2fef2-2422">Etiquetas de propiedad en orden numérico</span><span class="sxs-lookup"><span data-stu-id="2fef2-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="2fef2-2423">Leer y escribir metadatos</span><span class="sxs-lookup"><span data-stu-id="2fef2-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



