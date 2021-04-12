---
description: Especifica la cantidad de tiempo, en milisegundos, para almacenar en búfer los datos antes de reproducir un archivo de formato de sistema avanzado (ASF).
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: MF_PD_ASF_FILEPROPERTIES_PREROLL atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277835"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="4f5a7-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ atributo de preroll</span><span class="sxs-lookup"><span data-stu-id="4f5a7-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="4f5a7-104">Especifica la cantidad de tiempo, en milisegundos, para almacenar en búfer los datos antes de reproducir un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="4f5a7-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f5a7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4f5a7-105">Data type</span></span>

<span data-ttu-id="4f5a7-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5a7-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f5a7-107">Remarks</span></span>

<span data-ttu-id="4f5a7-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="4f5a7-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="4f5a7-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="4f5a7-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5a7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f5a7-110">Requirements</span></span>



| <span data-ttu-id="4f5a7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5a7-111">Requirement</span></span> | <span data-ttu-id="4f5a7-112">Value</span><span class="sxs-lookup"><span data-stu-id="4f5a7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5a7-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f5a7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5a7-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4f5a7-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4f5a7-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f5a7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5a7-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f5a7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f5a7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f5a7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f5a7-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f5a7-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f5a7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f5a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5a7-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f5a7-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f5a7-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4f5a7-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="4f5a7-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4f5a7-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="4f5a7-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f5a7-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="4f5a7-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="4f5a7-126">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="4f5a7-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




