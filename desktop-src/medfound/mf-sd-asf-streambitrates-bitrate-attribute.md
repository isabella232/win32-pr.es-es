---
description: Especifica la velocidad de bits promedio, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de propiedades de velocidad de bits de flujo definido en la especificación ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716149"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="51f7f-104">MF \_ SD \_ ASF \_ STREAMBITRATES \_ atributo de velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="51f7f-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="51f7f-105">Especifica la velocidad de bits promedio, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="51f7f-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="51f7f-106">Este atributo corresponde al objeto de propiedades de velocidad de bits de flujo definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="51f7f-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="51f7f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="51f7f-107">Data type</span></span>

<span data-ttu-id="51f7f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="51f7f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="51f7f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51f7f-109">Remarks</span></span>

<span data-ttu-id="51f7f-110">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo y lo establece en el descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="51f7f-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="51f7f-111">La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="51f7f-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="51f7f-112">El valor de atributo es igual al campo de velocidad de bits promedio del objeto de propiedades de velocidad de bits de flujo.</span><span class="sxs-lookup"><span data-stu-id="51f7f-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f7f-113">Requirements</span></span>



| <span data-ttu-id="51f7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f7f-114">Requirement</span></span> | <span data-ttu-id="51f7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="51f7f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f7f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51f7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="51f7f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="51f7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="51f7f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51f7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="51f7f-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="51f7f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51f7f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51f7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f7f-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f7f-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f7f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="51f7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f7f-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51f7f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51f7f-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="51f7f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="51f7f-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="51f7f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="51f7f-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="51f7f-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="51f7f-127">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="51f7f-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="51f7f-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="51f7f-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




