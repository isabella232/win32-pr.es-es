---
description: Contiene los datos de cifrado de un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de cifrado de contenido extendido del encabezado ASF, definido en la especificación ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360511"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="b89b3-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ atributo de datos de cifrado \_</span><span class="sxs-lookup"><span data-stu-id="b89b3-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="b89b3-105">Contiene los datos de cifrado de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="b89b3-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b89b3-106">Este atributo corresponde al objeto de cifrado de contenido extendido del encabezado ASF, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="b89b3-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="b89b3-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b89b3-107">Data type</span></span>

<span data-ttu-id="b89b3-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="b89b3-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="b89b3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b89b3-109">Remarks</span></span>

<span data-ttu-id="b89b3-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="b89b3-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b89b3-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del encabezado de objeto de cifrado de contenido extendido.</span><span class="sxs-lookup"><span data-stu-id="b89b3-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="b89b3-112">El tamaño del BLOB es igual al campo tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="b89b3-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="b89b3-113">La matriz de bytes contenida en el BLOB es igual al campo de datos del objeto de cifrado de contenido extendido del encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="b89b3-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89b3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89b3-114">Requirements</span></span>



| <span data-ttu-id="b89b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b89b3-115">Requirement</span></span> | <span data-ttu-id="b89b3-116">Value</span><span class="sxs-lookup"><span data-stu-id="b89b3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89b3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b89b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b89b3-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b89b3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b89b3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b89b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b89b3-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b89b3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b89b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b89b3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b89b3-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89b3-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b89b3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b89b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89b3-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b89b3-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b89b3-125">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="b89b3-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="b89b3-126">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="b89b3-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="b89b3-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b89b3-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b89b3-128">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="b89b3-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b89b3-129">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="b89b3-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b89b3-130">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="b89b3-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




