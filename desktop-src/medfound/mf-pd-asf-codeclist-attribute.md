---
description: Contiene información acerca de los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de lista de códecs del encabezado ASF, definido en la especificación ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697524"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="fbc76-104">MF \_ PD \_ ASF \_ atributo CODECLIST</span><span class="sxs-lookup"><span data-stu-id="fbc76-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="fbc76-105">Contiene información acerca de los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="fbc76-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="fbc76-106">Este atributo corresponde al objeto de lista de códecs del encabezado ASF, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="fbc76-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbc76-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fbc76-107">Data type</span></span>

<span data-ttu-id="fbc76-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="fbc76-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc76-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbc76-109">Remarks</span></span>

<span data-ttu-id="fbc76-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="fbc76-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fbc76-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto de lista de códecs del encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="fbc76-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="fbc76-112">Una aplicación que usa el [origen de medios ASF](asf-media-source.md) puede obtener este atributo llamando a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) y, a continuación, obteniendo el atributo del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="fbc76-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="fbc76-113">En la tabla siguiente se muestra el diseño del BLOB de atributo.</span><span class="sxs-lookup"><span data-stu-id="fbc76-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="fbc76-114">Campo de objeto de lista de códecs</span><span class="sxs-lookup"><span data-stu-id="fbc76-114">Codec List Object field</span></span> | <span data-ttu-id="fbc76-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fbc76-115">Data type</span></span>    | <span data-ttu-id="fbc76-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fbc76-116">Size</span></span>    | <span data-ttu-id="fbc76-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbc76-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="fbc76-118">Recuento de entradas de códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-118">Codec Entries Count</span></span>     | <span data-ttu-id="fbc76-119">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fbc76-119">**DWORD**</span></span>    | <span data-ttu-id="fbc76-120">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fbc76-120">4 bytes</span></span> | <span data-ttu-id="fbc76-121">Número de códecs</span><span class="sxs-lookup"><span data-stu-id="fbc76-121">Number of codecs</span></span>                      |
| <span data-ttu-id="fbc76-122">Entradas de códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-122">Codec Entries</span></span>           | <span data-ttu-id="fbc76-123">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="fbc76-123">**BYTE**\[\]</span></span> | <span data-ttu-id="fbc76-124">Varía</span><span class="sxs-lookup"><span data-stu-id="fbc76-124">Varies</span></span>  | <span data-ttu-id="fbc76-125">Matriz de estructuras de información de códecs</span><span class="sxs-lookup"><span data-stu-id="fbc76-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="fbc76-126">El campo entradas de código es una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="fbc76-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="fbc76-127">En la tabla siguiente se muestra el formato de cada entrada:</span><span class="sxs-lookup"><span data-stu-id="fbc76-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbc76-128">Campo de objeto de lista de códecs</span><span class="sxs-lookup"><span data-stu-id="fbc76-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="fbc76-129">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fbc76-129">Data type</span></span></th>
<th><span data-ttu-id="fbc76-130">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fbc76-130">Size</span></span></th>
<th><span data-ttu-id="fbc76-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbc76-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbc76-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbc76-132">Type</span></span></td>
<td><span data-ttu-id="fbc76-133"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fbc76-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="fbc76-134">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fbc76-134">4 bytes</span></span></td>
<td><span data-ttu-id="fbc76-135">Tipo de códec.</span><span class="sxs-lookup"><span data-stu-id="fbc76-135">Codec type.</span></span> <span data-ttu-id="fbc76-136">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="fbc76-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="fbc76-137">0x0001: códec de audio</span><span class="sxs-lookup"><span data-stu-id="fbc76-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="fbc76-138">0x0002: códec de vídeo</span><span class="sxs-lookup"><span data-stu-id="fbc76-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="fbc76-139">0xFFFF: desconocido</span><span class="sxs-lookup"><span data-stu-id="fbc76-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbc76-140">Longitud del nombre del códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="fbc76-141"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fbc76-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="fbc76-142">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fbc76-142">4 bytes</span></span></td>
<td><span data-ttu-id="fbc76-143">Tamaño de la cadena del nombre del códec, en bytes, incluido el carácter <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="fbc76-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbc76-144">Nombre del códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-144">Codec Name</span></span></td>
<td><span data-ttu-id="fbc76-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="fbc76-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="fbc76-146">Varía</span><span class="sxs-lookup"><span data-stu-id="fbc76-146">Varies</span></span></td>
<td><span data-ttu-id="fbc76-147">Cadena Unicode terminada en null que contiene el nombre del códec, como &quot; Windows Media Video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="fbc76-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbc76-148">Longitud de la descripción del códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="fbc76-149"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fbc76-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="fbc76-150">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fbc76-150">4 bytes</span></span></td>
<td><span data-ttu-id="fbc76-151">Tamaño de la cadena de Descripción del códec, en bytes, incluido el carácter <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="fbc76-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbc76-152">Descripción del códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-152">Codec Description</span></span></td>
<td><span data-ttu-id="fbc76-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="fbc76-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="fbc76-154">Varía</span><span class="sxs-lookup"><span data-stu-id="fbc76-154">Varies</span></span></td>
<td><span data-ttu-id="fbc76-155">Una cadena Unicode terminada en null que contiene una descripción del códec.</span><span class="sxs-lookup"><span data-stu-id="fbc76-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbc76-156">Longitud de información de códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="fbc76-157"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fbc76-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="fbc76-158">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fbc76-158">4 bytes</span></span></td>
<td><span data-ttu-id="fbc76-159">Tamaño del campo de información del códec, en bytes.</span><span class="sxs-lookup"><span data-stu-id="fbc76-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbc76-160">Información del códec</span><span class="sxs-lookup"><span data-stu-id="fbc76-160">Codec Information</span></span></td>
<td><span data-ttu-id="fbc76-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="fbc76-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="fbc76-162">Varía</span><span class="sxs-lookup"><span data-stu-id="fbc76-162">Varies</span></span></td>
<td><span data-ttu-id="fbc76-163">Datos de códec.</span><span class="sxs-lookup"><span data-stu-id="fbc76-163">Codec data.</span></span> <span data-ttu-id="fbc76-164">El significado de estos datos depende del códec.</span><span class="sxs-lookup"><span data-stu-id="fbc76-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="fbc76-165">Normalmente, estos datos indican el formato.</span><span class="sxs-lookup"><span data-stu-id="fbc76-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="fbc76-166">El diseño del BLOB de atributo no coincide exactamente con el diseño del objeto de lista de códecs del encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="fbc76-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="fbc76-167">En concreto, las longitudes de cadena se proporcionan en bytes e incluyen el tamaño del terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="fbc76-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fbc76-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc76-168">Requirements</span></span>



| <span data-ttu-id="fbc76-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc76-169">Requirement</span></span> | <span data-ttu-id="fbc76-170">Value</span><span class="sxs-lookup"><span data-stu-id="fbc76-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc76-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc76-171">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc76-172">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fbc76-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fbc76-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc76-173">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc76-174">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbc76-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbc76-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbc76-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc76-176"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc76-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc76-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbc76-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc76-178">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbc76-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbc76-179">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="fbc76-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fbc76-180">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="fbc76-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fbc76-181">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fbc76-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fbc76-182">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="fbc76-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbc76-183">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="fbc76-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fbc76-184">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="fbc76-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




