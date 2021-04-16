---
description: Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716150"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="d7a92-103">MF \_ SD \_ ASF \_ \_ atributo de \_ plantilla de cumplimiento de dispositivos de metadatos \_</span><span class="sxs-lookup"><span data-stu-id="d7a92-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="d7a92-104">Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="d7a92-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7a92-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d7a92-105">Data type</span></span>

<span data-ttu-id="d7a92-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="d7a92-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a92-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a92-107">Remarks</span></span>

<span data-ttu-id="d7a92-108">Este atributo se aplica a los descriptores de flujo para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="d7a92-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="d7a92-109">Para obtener más información acerca de las plantillas de conformidad de dispositivos, consulte el tema "parámetros de plantilla de conformidad de dispositivos" en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d7a92-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="d7a92-110">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="d7a92-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a92-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a92-111">Requirements</span></span>



| <span data-ttu-id="d7a92-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a92-112">Requirement</span></span> | <span data-ttu-id="d7a92-113">Value</span><span class="sxs-lookup"><span data-stu-id="d7a92-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a92-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a92-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a92-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a92-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7a92-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a92-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a92-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a92-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d7a92-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7a92-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a92-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a92-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a92-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7a92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a92-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7a92-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7a92-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="d7a92-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="d7a92-123">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="d7a92-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="d7a92-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d7a92-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="d7a92-125">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="d7a92-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7a92-126">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="d7a92-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




