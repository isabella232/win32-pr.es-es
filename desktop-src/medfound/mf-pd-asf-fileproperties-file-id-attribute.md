---
description: Especifica el identificador de archivo de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: MF_PD_ASF_FILEPROPERTIES_FILE_ID atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659843"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="f752e-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ atributo de ID. de archivo</span><span class="sxs-lookup"><span data-stu-id="f752e-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="f752e-104">Especifica el identificador de archivo de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f752e-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f752e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f752e-105">Data type</span></span>

<span data-ttu-id="f752e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f752e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="f752e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f752e-107">Remarks</span></span>

<span data-ttu-id="f752e-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="f752e-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f752e-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="f752e-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="f752e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f752e-110">Requirements</span></span>



| <span data-ttu-id="f752e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f752e-111">Requirement</span></span> | <span data-ttu-id="f752e-112">Value</span><span class="sxs-lookup"><span data-stu-id="f752e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f752e-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f752e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f752e-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f752e-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f752e-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f752e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f752e-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f752e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f752e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f752e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f752e-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f752e-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f752e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f752e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f752e-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f752e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f752e-121">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="f752e-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="f752e-122">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="f752e-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="f752e-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f752e-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f752e-124">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f752e-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f752e-125">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="f752e-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f752e-126">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="f752e-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




