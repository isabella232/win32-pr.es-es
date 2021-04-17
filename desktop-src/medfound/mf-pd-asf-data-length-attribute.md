---
description: Especifica el tamaño, en bytes, de la sección de datos de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: MF_PD_ASF_DATA_LENGTH atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659821"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="fa3f6-103">MF \_ PD \_ ASF \_ atributo de longitud de datos \_</span><span class="sxs-lookup"><span data-stu-id="fa3f6-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="fa3f6-104">Especifica el tamaño, en bytes, de la sección de datos de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="fa3f6-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="fa3f6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fa3f6-105">Data type</span></span>

<span data-ttu-id="fa3f6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fa3f6-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3f6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa3f6-107">Remarks</span></span>

<span data-ttu-id="fa3f6-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="fa3f6-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fa3f6-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="fa3f6-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3f6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa3f6-110">Requirements</span></span>



| <span data-ttu-id="fa3f6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa3f6-111">Requirement</span></span> | <span data-ttu-id="fa3f6-112">Value</span><span class="sxs-lookup"><span data-stu-id="fa3f6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3f6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa3f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3f6-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fa3f6-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa3f6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa3f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3f6-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa3f6-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fa3f6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa3f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa3f6-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f6-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa3f6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa3f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3f6-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fa3f6-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fa3f6-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fa3f6-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="fa3f6-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fa3f6-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="fa3f6-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fa3f6-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fa3f6-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="fa3f6-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fa3f6-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="fa3f6-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




