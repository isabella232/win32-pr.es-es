---
description: Especifica la velocidad de bits de datos máxima, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85626be11afe2e9413852e8aec3533f987538473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716803"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a><span data-ttu-id="4351e-103">\_Atributo MF SD \_ ASF \_ EXTSTRMPROP \_ Max \_ Data \_ bitrate</span><span class="sxs-lookup"><span data-stu-id="4351e-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE attribute</span></span>

<span data-ttu-id="4351e-104">Especifica la velocidad de bits de datos máxima, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="4351e-104">Specifies the maximum data bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="4351e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4351e-105">Data type</span></span>

<span data-ttu-id="4351e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4351e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4351e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4351e-107">Remarks</span></span>

<span data-ttu-id="4351e-108">Este atributo se aplica a los descriptores de flujo para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="4351e-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="4351e-109">Corresponde al campo de velocidad de bits de datos alternativo del objeto de propiedades de flujo extendido.</span><span class="sxs-lookup"><span data-stu-id="4351e-109">It corresponds to the Alternate Data Bit Rate field in the Extended Stream Properties object.</span></span> <span data-ttu-id="4351e-110">Para obtener más información, consulte la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="4351e-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="4351e-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="4351e-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="4351e-112">La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="4351e-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="4351e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4351e-113">Requirements</span></span>



| <span data-ttu-id="4351e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4351e-114">Requirement</span></span> | <span data-ttu-id="4351e-115">Value</span><span class="sxs-lookup"><span data-stu-id="4351e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4351e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4351e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4351e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4351e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4351e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4351e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4351e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4351e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4351e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4351e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4351e-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4351e-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4351e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4351e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4351e-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4351e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4351e-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4351e-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4351e-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4351e-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4351e-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4351e-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="4351e-127">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="4351e-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4351e-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="4351e-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




