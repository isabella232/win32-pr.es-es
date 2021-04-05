---
description: Especifica el desplazamiento, en bytes, desde el inicio de un archivo de formato de sistema avanzado (ASF) hasta el inicio del primer paquete de datos.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: MF_PD_ASF_DATA_START_OFFSET atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912158"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="fbeff-103">MF \_ PD \_ - \_ atributo de desplazamiento de inicio de datos ASF \_ \_</span><span class="sxs-lookup"><span data-stu-id="fbeff-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="fbeff-104">Especifica el desplazamiento, en bytes, desde el inicio de un archivo de formato de sistema avanzado (ASF) hasta el inicio del primer paquete de datos.</span><span class="sxs-lookup"><span data-stu-id="fbeff-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbeff-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fbeff-105">Data type</span></span>

<span data-ttu-id="fbeff-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fbeff-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="fbeff-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbeff-107">Remarks</span></span>

<span data-ttu-id="fbeff-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="fbeff-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fbeff-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="fbeff-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbeff-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbeff-110">Requirements</span></span>



| <span data-ttu-id="fbeff-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbeff-111">Requirement</span></span> | <span data-ttu-id="fbeff-112">Value</span><span class="sxs-lookup"><span data-stu-id="fbeff-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeff-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbeff-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fbeff-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fbeff-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fbeff-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbeff-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fbeff-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbeff-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbeff-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbeff-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbeff-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeff-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbeff-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbeff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbeff-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbeff-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbeff-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fbeff-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="fbeff-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fbeff-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="fbeff-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fbeff-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fbeff-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="fbeff-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbeff-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="fbeff-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




