---
description: Especifica el tamaño de búfer promedio necesario para un archivo de formato de sistema avanzado (VBR) de velocidad de bits variable (VBR).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: MF_PD_ASF_METADATA_V8_BUFFERAVERAGE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715395"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="ee0be-103">MF \_ PD \_ ASF \_ Metadata \_ V8 \_ BUFFERAVERAGE atributo</span><span class="sxs-lookup"><span data-stu-id="ee0be-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="ee0be-104">Especifica el tamaño de búfer promedio necesario para un archivo de formato de sistema avanzado (VBR) de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="ee0be-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee0be-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ee0be-105">Data type</span></span>

<span data-ttu-id="ee0be-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ee0be-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee0be-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee0be-107">Remarks</span></span>

<span data-ttu-id="ee0be-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="ee0be-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ee0be-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo que se aplica al descriptor de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="ee0be-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="ee0be-110">Este atributo solo se aplica a los archivos creados por la versión 8 del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ee0be-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="ee0be-111">Se corresponde con el atributo **BufferAverage** en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ee0be-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee0be-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee0be-112">Requirements</span></span>



| <span data-ttu-id="ee0be-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee0be-113">Requirement</span></span> | <span data-ttu-id="ee0be-114">Value</span><span class="sxs-lookup"><span data-stu-id="ee0be-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0be-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0be-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee0be-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee0be-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee0be-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee0be-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee0be-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee0be-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ee0be-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee0be-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee0be-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee0be-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0be-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee0be-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0be-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee0be-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee0be-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee0be-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ee0be-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee0be-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ee0be-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ee0be-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ee0be-126">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="ee0be-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee0be-127">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="ee0be-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="ee0be-128">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="ee0be-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




