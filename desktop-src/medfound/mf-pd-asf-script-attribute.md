---
description: Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de comando de script del encabezado ASF, definido en la especificación ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716421"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="54f8a-104">MF \_ PD \_ ASF \_ atributo de script</span><span class="sxs-lookup"><span data-stu-id="54f8a-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="54f8a-105">Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="54f8a-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="54f8a-106">Este atributo corresponde al objeto de comando de script del encabezado ASF, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="54f8a-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="54f8a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="54f8a-107">Data type</span></span>

<span data-ttu-id="54f8a-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="54f8a-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="54f8a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54f8a-109">Remarks</span></span>

<span data-ttu-id="54f8a-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="54f8a-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="54f8a-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo desde el encabezado del objeto de comando de script.</span><span class="sxs-lookup"><span data-stu-id="54f8a-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="54f8a-112">En la tabla siguiente se muestra el formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="54f8a-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="54f8a-113">Campo de objeto de comando de script</span><span class="sxs-lookup"><span data-stu-id="54f8a-113">Script Command Object field</span></span> | <span data-ttu-id="54f8a-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="54f8a-114">Data type</span></span>    | <span data-ttu-id="54f8a-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="54f8a-115">Size</span></span>    | <span data-ttu-id="54f8a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f8a-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="54f8a-117">Recuento de comandos</span><span class="sxs-lookup"><span data-stu-id="54f8a-117">Commands Count</span></span>              | <span data-ttu-id="54f8a-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="54f8a-118">**DWORD**</span></span>    | <span data-ttu-id="54f8a-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="54f8a-119">4 bytes</span></span> | <span data-ttu-id="54f8a-120">Número de comandos de script</span><span class="sxs-lookup"><span data-stu-id="54f8a-120">Number of script commands</span></span> |
| <span data-ttu-id="54f8a-121">Tipo de comando, comandos</span><span class="sxs-lookup"><span data-stu-id="54f8a-121">Command Type, Commands</span></span>      | <span data-ttu-id="54f8a-122">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="54f8a-122">**BYTE**\[\]</span></span> | <span data-ttu-id="54f8a-123">Varía</span><span class="sxs-lookup"><span data-stu-id="54f8a-123">Varies</span></span>  | <span data-ttu-id="54f8a-124">Matriz de comandos de script</span><span class="sxs-lookup"><span data-stu-id="54f8a-124">Array of script commands</span></span>  |



 

<span data-ttu-id="54f8a-125">El primer **valor DWORD** es el número de comandos de script, seguidos de una matriz de comandos.</span><span class="sxs-lookup"><span data-stu-id="54f8a-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="54f8a-126">Cada comando de script tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="54f8a-126">Each script command has the following format:</span></span>



| <span data-ttu-id="54f8a-127">Campo de objeto de comando de script</span><span class="sxs-lookup"><span data-stu-id="54f8a-127">Script Command Object field</span></span> | <span data-ttu-id="54f8a-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="54f8a-128">Data type</span></span>     | <span data-ttu-id="54f8a-129">Tamaño</span><span class="sxs-lookup"><span data-stu-id="54f8a-129">Size</span></span>    | <span data-ttu-id="54f8a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f8a-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="54f8a-131">Longitud del nombre de comando</span><span class="sxs-lookup"><span data-stu-id="54f8a-131">Command Name Length</span></span>         | <span data-ttu-id="54f8a-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="54f8a-132">**DWORD**</span></span>     | <span data-ttu-id="54f8a-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="54f8a-133">4 bytes</span></span> | <span data-ttu-id="54f8a-134">Tamaño de la cadena de comandos, en bytes, incluido el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="54f8a-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="54f8a-135">Nombre de comando</span><span class="sxs-lookup"><span data-stu-id="54f8a-135">Command Name</span></span>                | <span data-ttu-id="54f8a-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="54f8a-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="54f8a-137">Varía</span><span class="sxs-lookup"><span data-stu-id="54f8a-137">Varies</span></span>  | <span data-ttu-id="54f8a-138">Cadena terminada en null que contiene el comando de script.</span><span class="sxs-lookup"><span data-stu-id="54f8a-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="54f8a-139">Longitud del nombre del tipo de comando</span><span class="sxs-lookup"><span data-stu-id="54f8a-139">Command Type Name Length</span></span>    | <span data-ttu-id="54f8a-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="54f8a-140">**DWORD**</span></span>     | <span data-ttu-id="54f8a-141">4 bytes</span><span class="sxs-lookup"><span data-stu-id="54f8a-141">4 bytes</span></span> | <span data-ttu-id="54f8a-142">Tamaño de la cadena de tipo de comando, en bytes, incluido el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="54f8a-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="54f8a-143">Nombre del tipo de comando</span><span class="sxs-lookup"><span data-stu-id="54f8a-143">Command Type Name</span></span>           | <span data-ttu-id="54f8a-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="54f8a-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="54f8a-145">Varía</span><span class="sxs-lookup"><span data-stu-id="54f8a-145">Varies</span></span>  | <span data-ttu-id="54f8a-146">Cadena terminada en null que contiene el tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="54f8a-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="54f8a-147">Tiempo de presentación</span><span class="sxs-lookup"><span data-stu-id="54f8a-147">Presentation Time</span></span>           | <span data-ttu-id="54f8a-148">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="54f8a-148">**DWORD**</span></span>     | <span data-ttu-id="54f8a-149">4 bytes</span><span class="sxs-lookup"><span data-stu-id="54f8a-149">4 bytes</span></span> | <span data-ttu-id="54f8a-150">Tiempo de presentación del comando en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="54f8a-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="54f8a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54f8a-151">Requirements</span></span>



| <span data-ttu-id="54f8a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="54f8a-152">Requirement</span></span> | <span data-ttu-id="54f8a-153">Value</span><span class="sxs-lookup"><span data-stu-id="54f8a-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f8a-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54f8a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="54f8a-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="54f8a-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54f8a-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54f8a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="54f8a-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="54f8a-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54f8a-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54f8a-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f8a-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f8a-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f8a-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="54f8a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f8a-161">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54f8a-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="54f8a-162">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="54f8a-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="54f8a-163">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="54f8a-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="54f8a-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="54f8a-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="54f8a-165">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="54f8a-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="54f8a-166">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="54f8a-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="54f8a-167">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="54f8a-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




