---
description: Especifica los marcadores en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de marcador en el encabezado ASF, definido en la especificación ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688518"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="71672-104">MF \_ PD \_ ASF \_ atributo de marcador</span><span class="sxs-lookup"><span data-stu-id="71672-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="71672-105">Especifica los marcadores en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="71672-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="71672-106">Este atributo corresponde al objeto de marcador en el encabezado ASF, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="71672-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="71672-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71672-107">Data type</span></span>

<span data-ttu-id="71672-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="71672-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="71672-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71672-109">Remarks</span></span>

<span data-ttu-id="71672-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="71672-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="71672-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto de marcador.</span><span class="sxs-lookup"><span data-stu-id="71672-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="71672-112">En la tabla siguiente se muestra el formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="71672-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="71672-113">Campo de objeto de marcador</span><span class="sxs-lookup"><span data-stu-id="71672-113">Marker Object field</span></span> | <span data-ttu-id="71672-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71672-114">Data type</span></span>    | <span data-ttu-id="71672-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="71672-115">Size</span></span>    | <span data-ttu-id="71672-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="71672-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="71672-117">Recuento de marcadores</span><span class="sxs-lookup"><span data-stu-id="71672-117">Markers Count</span></span>       | <span data-ttu-id="71672-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="71672-118">**DWORD**</span></span>    | <span data-ttu-id="71672-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="71672-119">4 bytes</span></span> | <span data-ttu-id="71672-120">Número de marcadores</span><span class="sxs-lookup"><span data-stu-id="71672-120">Number of markers</span></span> |
| <span data-ttu-id="71672-121">Marcadores</span><span class="sxs-lookup"><span data-stu-id="71672-121">Markers</span></span>             | <span data-ttu-id="71672-122">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="71672-122">**BYTE**\[\]</span></span> | <span data-ttu-id="71672-123">Varía</span><span class="sxs-lookup"><span data-stu-id="71672-123">Varies</span></span>  | <span data-ttu-id="71672-124">Matriz de marcadores</span><span class="sxs-lookup"><span data-stu-id="71672-124">Array of markers</span></span>  |



 

<span data-ttu-id="71672-125">El primer **valor DWORD** es el número de marcadores seguido de una matriz de marcadores.</span><span class="sxs-lookup"><span data-stu-id="71672-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="71672-126">Cada marcador tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="71672-126">Each marker has the following format:</span></span>



| <span data-ttu-id="71672-127">Campo de objeto de marcador</span><span class="sxs-lookup"><span data-stu-id="71672-127">Marker Object field</span></span>       | <span data-ttu-id="71672-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71672-128">Data type</span></span>     | <span data-ttu-id="71672-129">Tamaño</span><span class="sxs-lookup"><span data-stu-id="71672-129">Size</span></span>    | <span data-ttu-id="71672-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="71672-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71672-131">Longitud de la descripción del marcador</span><span class="sxs-lookup"><span data-stu-id="71672-131">Marker Description Length</span></span> | <span data-ttu-id="71672-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="71672-132">**DWORD**</span></span>     | <span data-ttu-id="71672-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="71672-133">4 bytes</span></span> | <span data-ttu-id="71672-134">Tamaño de la cadena de descripción, en bytes, incluido el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="71672-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="71672-135">Descripción del marcador</span><span class="sxs-lookup"><span data-stu-id="71672-135">Marker Description</span></span>        | <span data-ttu-id="71672-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="71672-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="71672-137">Varía</span><span class="sxs-lookup"><span data-stu-id="71672-137">Varies</span></span>  | <span data-ttu-id="71672-138">Cadena terminada en null que describe el marcador.</span><span class="sxs-lookup"><span data-stu-id="71672-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="71672-139">Tiempo de presentación</span><span class="sxs-lookup"><span data-stu-id="71672-139">Presentation Time</span></span>         | <span data-ttu-id="71672-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="71672-140">**LONGLONG**</span></span>  | <span data-ttu-id="71672-141">8 bytes</span><span class="sxs-lookup"><span data-stu-id="71672-141">8 bytes</span></span> | <span data-ttu-id="71672-142">Tiempo de presentación del marcador, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="71672-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="71672-143">Hora de envío</span><span class="sxs-lookup"><span data-stu-id="71672-143">Send Time</span></span>                 | <span data-ttu-id="71672-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="71672-144">**LONGLONG**</span></span>  | <span data-ttu-id="71672-145">8 bytes</span><span class="sxs-lookup"><span data-stu-id="71672-145">8 bytes</span></span> | <span data-ttu-id="71672-146">Hora de envío de la entrada de marcador, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="71672-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="71672-147">Offset</span><span class="sxs-lookup"><span data-stu-id="71672-147">Offset</span></span>                    | <span data-ttu-id="71672-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="71672-148">**UINT64**</span></span>    | <span data-ttu-id="71672-149">8 bytes</span><span class="sxs-lookup"><span data-stu-id="71672-149">8 bytes</span></span> | <span data-ttu-id="71672-150">Desplazamiento, en bytes, en el objeto de datos que especifica la posición del mercado.</span><span class="sxs-lookup"><span data-stu-id="71672-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="71672-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71672-151">Requirements</span></span>



| <span data-ttu-id="71672-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="71672-152">Requirement</span></span> | <span data-ttu-id="71672-153">Value</span><span class="sxs-lookup"><span data-stu-id="71672-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71672-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71672-154">Minimum supported client</span></span><br/> | <span data-ttu-id="71672-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71672-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="71672-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71672-156">Minimum supported server</span></span><br/> | <span data-ttu-id="71672-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71672-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71672-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71672-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="71672-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="71672-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71672-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="71672-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71672-161">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71672-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="71672-162">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="71672-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="71672-163">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="71672-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="71672-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="71672-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="71672-165">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="71672-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="71672-166">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="71672-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="71672-167">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="71672-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




