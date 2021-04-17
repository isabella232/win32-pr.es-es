---
description: Especifica si un archivo de formato de sistema avanzado (ASF) contiene al menos un flujo de vídeo.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: MF_PD_ASF_INFO_HAS_VIDEO atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716494"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="0185d-103">MF \_ PD \_ ASF \_ info \_ tiene el \_ atributo vídeo</span><span class="sxs-lookup"><span data-stu-id="0185d-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="0185d-104">Especifica si un archivo de formato de sistema avanzado (ASF) contiene al menos un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0185d-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="0185d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0185d-105">Data type</span></span>

<span data-ttu-id="0185d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0185d-106">**UINT32**</span></span>

<span data-ttu-id="0185d-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="0185d-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0185d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0185d-108">Remarks</span></span>

<span data-ttu-id="0185d-109">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="0185d-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="0185d-110">Si el valor es **true**, el archivo tiene al menos un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0185d-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="0185d-111">De lo contrario, el archivo no contiene ninguna secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0185d-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="0185d-112">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="0185d-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="0185d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0185d-113">Requirements</span></span>



| <span data-ttu-id="0185d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0185d-114">Requirement</span></span> | <span data-ttu-id="0185d-115">Value</span><span class="sxs-lookup"><span data-stu-id="0185d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0185d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0185d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0185d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0185d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0185d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0185d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0185d-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0185d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0185d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0185d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0185d-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0185d-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0185d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0185d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0185d-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0185d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0185d-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0185d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0185d-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0185d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0185d-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0185d-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0185d-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="0185d-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0185d-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="0185d-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




