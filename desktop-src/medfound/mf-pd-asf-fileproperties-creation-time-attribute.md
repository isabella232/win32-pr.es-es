---
description: Especifica la fecha y hora en que se creó un archivo de formato de sistema avanzado (ASF).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: MF_PD_ASF_FILEPROPERTIES_CREATION_TIME atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001116"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="172fb-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ atributo de hora de creación \_</span><span class="sxs-lookup"><span data-stu-id="172fb-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="172fb-104">Especifica la fecha y hora en que se creó un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="172fb-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="172fb-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="172fb-105">Data type</span></span>

<span data-ttu-id="172fb-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="172fb-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="172fb-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="172fb-107">Remarks</span></span>

<span data-ttu-id="172fb-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="172fb-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="172fb-109">El valor del atributo es una estructura **FILETIME** , que se documenta en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="172fb-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="172fb-110">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="172fb-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="172fb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="172fb-111">Requirements</span></span>



| <span data-ttu-id="172fb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="172fb-112">Requirement</span></span> | <span data-ttu-id="172fb-113">Value</span><span class="sxs-lookup"><span data-stu-id="172fb-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="172fb-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="172fb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="172fb-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="172fb-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="172fb-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="172fb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="172fb-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="172fb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="172fb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="172fb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="172fb-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="172fb-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172fb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="172fb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172fb-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="172fb-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="172fb-122">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="172fb-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="172fb-123">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="172fb-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="172fb-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="172fb-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="172fb-125">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="172fb-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="172fb-126">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="172fb-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="172fb-127">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="172fb-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




