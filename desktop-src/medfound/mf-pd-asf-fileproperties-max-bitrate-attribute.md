---
description: Especifica la velocidad de bits instantánea máxima, en bits por segundo, para un archivo de formato de sistema avanzado (ASF).
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909593"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="55381-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ atributo de velocidad de bits máx.</span><span class="sxs-lookup"><span data-stu-id="55381-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="55381-104">Especifica la velocidad de bits instantánea máxima, en bits por segundo, para un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="55381-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="55381-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="55381-105">Data type</span></span>

<span data-ttu-id="55381-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="55381-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="55381-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55381-107">Remarks</span></span>

<span data-ttu-id="55381-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="55381-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="55381-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="55381-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="55381-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55381-110">Requirements</span></span>



| <span data-ttu-id="55381-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="55381-111">Requirement</span></span> | <span data-ttu-id="55381-112">Value</span><span class="sxs-lookup"><span data-stu-id="55381-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55381-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55381-113">Minimum supported client</span></span><br/> | <span data-ttu-id="55381-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55381-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="55381-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55381-115">Minimum supported server</span></span><br/> | <span data-ttu-id="55381-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="55381-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="55381-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55381-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="55381-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="55381-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55381-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="55381-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55381-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55381-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55381-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55381-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="55381-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55381-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="55381-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="55381-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="55381-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="55381-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="55381-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="55381-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="55381-126">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="55381-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




