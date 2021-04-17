---
description: Contiene una lista de los lenguajes RFC 1766 usados en la presentación actual.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687969"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="32bfd-103">MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER atributo</span><span class="sxs-lookup"><span data-stu-id="32bfd-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="32bfd-104">Contiene una lista de los lenguajes RFC 1766 usados en la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="32bfd-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="32bfd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="32bfd-105">Data type</span></span>

<span data-ttu-id="32bfd-106">**BYTES \[\]**</span><span class="sxs-lookup"><span data-stu-id="32bfd-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="32bfd-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="32bfd-107">Get/set</span></span>

<span data-ttu-id="32bfd-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="32bfd-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="32bfd-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="32bfd-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="32bfd-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="32bfd-110">Applies to</span></span>

[<span data-ttu-id="32bfd-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="32bfd-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="32bfd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32bfd-112">Remarks</span></span>

<span data-ttu-id="32bfd-113">Este atributo se aplica a los descriptores de presentación que se generaron a partir del [objeto ContentInfo ASF](asf-contentinfo-object.md) mediante una llamada a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="32bfd-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="32bfd-114">El formato de la matriz de bytes es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="32bfd-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="32bfd-115">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="32bfd-115">Language List Object field</span></span> | <span data-ttu-id="32bfd-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="32bfd-116">Data type</span></span>    | <span data-ttu-id="32bfd-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="32bfd-117">Size</span></span>    | <span data-ttu-id="32bfd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="32bfd-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="32bfd-119">Recuento de registros de ID. de idioma</span><span class="sxs-lookup"><span data-stu-id="32bfd-119">Language ID Records Count</span></span>  | <span data-ttu-id="32bfd-120">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32bfd-120">**DWORD**</span></span>    | <span data-ttu-id="32bfd-121">4 bytes</span><span class="sxs-lookup"><span data-stu-id="32bfd-121">4 bytes</span></span> | <span data-ttu-id="32bfd-122">Número de idiomas</span><span class="sxs-lookup"><span data-stu-id="32bfd-122">Number of languages</span></span>                    |
| <span data-ttu-id="32bfd-123">Registros de ID. de idioma</span><span class="sxs-lookup"><span data-stu-id="32bfd-123">Language ID Records</span></span>        | <span data-ttu-id="32bfd-124">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="32bfd-124">**BYTE**\[\]</span></span> | <span data-ttu-id="32bfd-125">Varía</span><span class="sxs-lookup"><span data-stu-id="32bfd-125">Varies</span></span>  | <span data-ttu-id="32bfd-126">Matriz de cadenas de lenguaje (vea más abajo).</span><span class="sxs-lookup"><span data-stu-id="32bfd-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="32bfd-127">El primer **valor DWORD** es el número de idiomas seguido de una matriz de cadenas de identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="32bfd-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="32bfd-128">Cada cadena tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="32bfd-128">Each string has the following format:</span></span>



| <span data-ttu-id="32bfd-129">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="32bfd-129">Language List Object field</span></span> | <span data-ttu-id="32bfd-130">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="32bfd-130">Data type</span></span>     | <span data-ttu-id="32bfd-131">Tamaño</span><span class="sxs-lookup"><span data-stu-id="32bfd-131">Size</span></span>    | <span data-ttu-id="32bfd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="32bfd-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bfd-133">Longitud del identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="32bfd-133">Language ID Length</span></span>         | <span data-ttu-id="32bfd-134">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="32bfd-134">**DWORD**</span></span>     | <span data-ttu-id="32bfd-135">4 bytes</span><span class="sxs-lookup"><span data-stu-id="32bfd-135">4 bytes</span></span> | <span data-ttu-id="32bfd-136">Longitud de la cadena en bytes, incluido el tamaño del carácter **nulo** final.</span><span class="sxs-lookup"><span data-stu-id="32bfd-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="32bfd-137">Id. de idioma</span><span class="sxs-lookup"><span data-stu-id="32bfd-137">Language ID</span></span>                | <span data-ttu-id="32bfd-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="32bfd-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="32bfd-139">Varía</span><span class="sxs-lookup"><span data-stu-id="32bfd-139">Varies</span></span>  | <span data-ttu-id="32bfd-140">Una cadena terminada en null que contiene el nombre del idioma RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="32bfd-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="32bfd-141">Cada cadena es una etiqueta de lenguaje compatible con RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="32bfd-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="32bfd-142">Utilice este atributo solo para la compatibilidad con versiones anteriores con el orden de enumeración de la interfaz [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="32bfd-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="32bfd-143">Las cadenas de idioma se almacenan en un orden diferente en el atributo [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="32bfd-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="32bfd-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32bfd-144">Requirements</span></span>



| <span data-ttu-id="32bfd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="32bfd-145">Requirement</span></span> | <span data-ttu-id="32bfd-146">Value</span><span class="sxs-lookup"><span data-stu-id="32bfd-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bfd-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32bfd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="32bfd-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="32bfd-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32bfd-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32bfd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="32bfd-150">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="32bfd-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32bfd-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32bfd-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="32bfd-152"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="32bfd-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32bfd-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="32bfd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32bfd-154">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32bfd-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="32bfd-155">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="32bfd-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
