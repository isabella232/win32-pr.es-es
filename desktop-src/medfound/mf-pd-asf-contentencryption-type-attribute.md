---
description: Especifica el tipo de mecanismo de protección usado en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: MF_PD_ASF_CONTENTENCRYPTION_TYPE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907916"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="222ae-103">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ atributo de tipo</span><span class="sxs-lookup"><span data-stu-id="222ae-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="222ae-104">Especifica el tipo de mecanismo de protección usado en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="222ae-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="222ae-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="222ae-105">Data type</span></span>

<span data-ttu-id="222ae-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="222ae-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="222ae-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="222ae-107">Remarks</span></span>

<span data-ttu-id="222ae-108">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="222ae-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="222ae-109">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo de tipo de protección, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="222ae-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="222ae-110">Si está presente, el valor debe ser "DRM".</span><span class="sxs-lookup"><span data-stu-id="222ae-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="222ae-111">El tamaño de la matriz es igual al campo de longitud de campo de tipo de protección del encabezado de cifrado de contenido.</span><span class="sxs-lookup"><span data-stu-id="222ae-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="222ae-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222ae-112">Requirements</span></span>



| <span data-ttu-id="222ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="222ae-113">Requirement</span></span> | <span data-ttu-id="222ae-114">Value</span><span class="sxs-lookup"><span data-stu-id="222ae-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="222ae-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="222ae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="222ae-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="222ae-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="222ae-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="222ae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="222ae-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="222ae-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="222ae-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="222ae-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="222ae-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="222ae-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="222ae-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="222ae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222ae-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="222ae-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="222ae-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="222ae-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="222ae-124">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="222ae-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="222ae-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="222ae-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="222ae-126">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="222ae-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="222ae-127">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="222ae-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="222ae-128">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="222ae-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




