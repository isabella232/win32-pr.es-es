---
description: Especifica si un archivo de formato de sistema avanzado (ASF) utiliza la codificación de velocidad de bits variable (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: MF_PD_ASF_METADATA_IS_VBR atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687968"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="08f38-103">Los \_ \_ metadatos ASF de MF PD \_ \_ son \_ atributos VBR</span><span class="sxs-lookup"><span data-stu-id="08f38-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="08f38-104">Especifica si un archivo de formato de sistema avanzado (ASF) utiliza la codificación de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="08f38-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="08f38-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="08f38-105">Data type</span></span>

<span data-ttu-id="08f38-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="08f38-106">**UINT32**</span></span>

<span data-ttu-id="08f38-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="08f38-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f38-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08f38-108">Remarks</span></span>

<span data-ttu-id="08f38-109">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="08f38-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="08f38-110">Si el valor es **true**, el archivo se ha codificado mediante VBR.</span><span class="sxs-lookup"><span data-stu-id="08f38-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="08f38-111">Si el valor es **false** o el atributo no está presente, el archivo no utiliza la codificación VBR.</span><span class="sxs-lookup"><span data-stu-id="08f38-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="08f38-112">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo y lo establece en el descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="08f38-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="08f38-113">Este atributo corresponde al atributo **IsVBR** en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="08f38-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08f38-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f38-114">Requirements</span></span>



| <span data-ttu-id="08f38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f38-115">Requirement</span></span> | <span data-ttu-id="08f38-116">Value</span><span class="sxs-lookup"><span data-stu-id="08f38-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f38-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08f38-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08f38-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08f38-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08f38-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08f38-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08f38-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="08f38-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="08f38-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08f38-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="08f38-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f38-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f38-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="08f38-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f38-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08f38-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08f38-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="08f38-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="08f38-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="08f38-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="08f38-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="08f38-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="08f38-128">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="08f38-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="08f38-129">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="08f38-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="08f38-130">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="08f38-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




