---
description: Especifica el número de paquetes en la sección de datos de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: MF_PD_ASF_FILEPROPERTIES_PACKETS atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001115"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="76c28-103">MF \_ PD \_ ASF \_ \_ atributo de paquetes FILEPROPERTIES</span><span class="sxs-lookup"><span data-stu-id="76c28-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="76c28-104">Especifica el número de paquetes en la sección de datos de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="76c28-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="76c28-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="76c28-105">Data type</span></span>

<span data-ttu-id="76c28-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="76c28-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="76c28-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76c28-107">Remarks</span></span>

<span data-ttu-id="76c28-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="76c28-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="76c28-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="76c28-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c28-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76c28-110">Requirements</span></span>



| <span data-ttu-id="76c28-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c28-111">Requirement</span></span> | <span data-ttu-id="76c28-112">Value</span><span class="sxs-lookup"><span data-stu-id="76c28-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c28-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76c28-113">Minimum supported client</span></span><br/> | <span data-ttu-id="76c28-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76c28-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="76c28-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76c28-115">Minimum supported server</span></span><br/> | <span data-ttu-id="76c28-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="76c28-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76c28-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76c28-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="76c28-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="76c28-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76c28-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="76c28-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c28-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76c28-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76c28-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="76c28-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="76c28-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="76c28-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="76c28-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="76c28-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="76c28-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="76c28-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="76c28-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="76c28-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="76c28-126">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="76c28-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




