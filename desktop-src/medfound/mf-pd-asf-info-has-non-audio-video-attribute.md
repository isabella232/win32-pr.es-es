---
description: Especifica si un archivo de formato de sistema avanzado (ASF) contiene secuencias que no son de audio o de vídeo.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002405"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="a51a8-103">MF \_ PD \_ ASF \_ info \_ tiene \_ un \_ atributo de vídeo que no es audio \_</span><span class="sxs-lookup"><span data-stu-id="a51a8-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="a51a8-104">Especifica si un archivo de formato de sistema avanzado (ASF) contiene secuencias que no son de audio o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a51a8-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="a51a8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a51a8-105">Data type</span></span>

<span data-ttu-id="a51a8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a51a8-106">**UINT32**</span></span>

<span data-ttu-id="a51a8-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="a51a8-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a51a8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a51a8-108">Remarks</span></span>

<span data-ttu-id="a51a8-109">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="a51a8-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="a51a8-110">Si el valor es **true**, el archivo tiene al menos un flujo que no es de audio o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a51a8-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="a51a8-111">Entre los ejemplos se incluyen secuencias de imágenes, comandos de script y datos arbitrarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="a51a8-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="a51a8-112">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="a51a8-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="a51a8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a51a8-113">Requirements</span></span>



| <span data-ttu-id="a51a8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a51a8-114">Requirement</span></span> | <span data-ttu-id="a51a8-115">Value</span><span class="sxs-lookup"><span data-stu-id="a51a8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51a8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a51a8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a51a8-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a51a8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a51a8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a51a8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a51a8-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a51a8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a51a8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a51a8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a51a8-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a51a8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a51a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51a8-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a51a8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a51a8-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a51a8-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a51a8-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a51a8-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a51a8-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a51a8-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a51a8-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="a51a8-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a51a8-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="a51a8-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




