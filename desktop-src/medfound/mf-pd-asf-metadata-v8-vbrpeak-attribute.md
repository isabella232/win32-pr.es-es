---
description: Especifica la velocidad de bits más alta en un archivo de formato ASF (velocidad de bits variable) (VBR).
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: MF_PD_ASF_METADATA_V8_VBRPEAK atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546091"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="f5b20-103">MF \_ PD \_ ASF \_ Metadata \_ V8 \_ VBRPEAK atributo</span><span class="sxs-lookup"><span data-stu-id="f5b20-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="f5b20-104">Especifica la velocidad de bits más alta en un archivo de formato ASF (velocidad de bits variable) (VBR).</span><span class="sxs-lookup"><span data-stu-id="f5b20-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5b20-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f5b20-105">Data type</span></span>

<span data-ttu-id="f5b20-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f5b20-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b20-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5b20-107">Remarks</span></span>

<span data-ttu-id="f5b20-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="f5b20-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f5b20-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo.</span><span class="sxs-lookup"><span data-stu-id="f5b20-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="f5b20-110">Este atributo solo se aplica a los archivos creados por la versión 8 del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="f5b20-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="f5b20-111">Se corresponde con el atributo **VBRPeak** en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="f5b20-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5b20-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b20-112">Requirements</span></span>



| <span data-ttu-id="f5b20-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b20-113">Requirement</span></span> | <span data-ttu-id="f5b20-114">Value</span><span class="sxs-lookup"><span data-stu-id="f5b20-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b20-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b20-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b20-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b20-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f5b20-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b20-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b20-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b20-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5b20-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5b20-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b20-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b20-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b20-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5b20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b20-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5b20-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5b20-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f5b20-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f5b20-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f5b20-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f5b20-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f5b20-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f5b20-126">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f5b20-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5b20-127">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="f5b20-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f5b20-128">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="f5b20-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




