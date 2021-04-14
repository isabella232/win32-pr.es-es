---
description: Contiene datos secretos para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo de datos Secret del encabezado de cifrado de contenido, definido en la especificación ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541358"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="0fcab-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_ atributo de datos secretos</span><span class="sxs-lookup"><span data-stu-id="0fcab-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="0fcab-105">Contiene datos secretos para un archivo de formato de sistema avanzado (ASF) cifrado.</span><span class="sxs-lookup"><span data-stu-id="0fcab-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="0fcab-106">Este atributo corresponde al campo de datos Secret del encabezado de cifrado de contenido, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="0fcab-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="0fcab-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0fcab-107">Data type</span></span>

<span data-ttu-id="0fcab-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="0fcab-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="0fcab-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fcab-109">Remarks</span></span>

<span data-ttu-id="0fcab-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="0fcab-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="0fcab-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) rellena una matriz de bytes con el campo de datos Secret.</span><span class="sxs-lookup"><span data-stu-id="0fcab-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="0fcab-112">El tamaño de la matriz es igual al campo de longitud de datos de secreto del encabezado de cifrado de contenido.</span><span class="sxs-lookup"><span data-stu-id="0fcab-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcab-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fcab-113">Requirements</span></span>



| <span data-ttu-id="0fcab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fcab-114">Requirement</span></span> | <span data-ttu-id="0fcab-115">Value</span><span class="sxs-lookup"><span data-stu-id="0fcab-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcab-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fcab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0fcab-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fcab-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0fcab-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fcab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0fcab-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fcab-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0fcab-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fcab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fcab-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fcab-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcab-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fcab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcab-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0fcab-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0fcab-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="0fcab-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="0fcab-125">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="0fcab-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="0fcab-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0fcab-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0fcab-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="0fcab-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0fcab-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="0fcab-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="0fcab-129">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="0fcab-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




