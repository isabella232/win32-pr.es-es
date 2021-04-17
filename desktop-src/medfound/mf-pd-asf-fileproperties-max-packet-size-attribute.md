---
description: Especifica el tamaño de paquete máximo, en bytes, de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 8dcae150-2363-47ba-b0d3-0bc182574d81
title: MF_PD_ASF_FILEPROPERTIES_MAX_PACKET_SIZE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9c95b7511525570a9e04a33db8128f374f9472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659921"
---
# <a name="mf_pd_asf_fileproperties_max_packet_size-attribute"></a><span data-ttu-id="f0fcd-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ tamaño máximo de \_ paquete \_ atributo</span><span class="sxs-lookup"><span data-stu-id="f0fcd-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="f0fcd-104">Especifica el tamaño de paquete máximo, en bytes, de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f0fcd-104">Specifies the maximum packet size, in bytes, of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0fcd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f0fcd-105">Data type</span></span>

<span data-ttu-id="f0fcd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f0fcd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0fcd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0fcd-107">Remarks</span></span>

<span data-ttu-id="f0fcd-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="f0fcd-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f0fcd-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="f0fcd-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0fcd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0fcd-110">Requirements</span></span>



| <span data-ttu-id="f0fcd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0fcd-111">Requirement</span></span> | <span data-ttu-id="f0fcd-112">Value</span><span class="sxs-lookup"><span data-stu-id="f0fcd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fcd-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0fcd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f0fcd-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0fcd-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f0fcd-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0fcd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f0fcd-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0fcd-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0fcd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0fcd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0fcd-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0fcd-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0fcd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0fcd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0fcd-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0fcd-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0fcd-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f0fcd-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f0fcd-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f0fcd-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f0fcd-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f0fcd-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f0fcd-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f0fcd-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0fcd-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="f0fcd-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f0fcd-126">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="f0fcd-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




