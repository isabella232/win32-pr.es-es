---
description: Especifica el tamaño promedio de búfer, en bytes, necesario para una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910802"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="56dfa-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ promedio de \_ BUFFERSIZE (atributo)</span><span class="sxs-lookup"><span data-stu-id="56dfa-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="56dfa-104">Especifica el tamaño promedio de búfer, en bytes, necesario para una secuencia en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="56dfa-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="56dfa-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="56dfa-105">Data type</span></span>

<span data-ttu-id="56dfa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="56dfa-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="56dfa-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56dfa-107">Remarks</span></span>

<span data-ttu-id="56dfa-108">Este atributo se aplica a los descriptores de flujo para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="56dfa-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="56dfa-109">Se corresponde con el campo tamaño del búfer del objeto Extended Stream Properties y define el tamaño del cubo que se usa en el modelo de "depósito de fugas".</span><span class="sxs-lookup"><span data-stu-id="56dfa-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="56dfa-110">Para obtener más información, consulte la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="56dfa-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="56dfa-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="56dfa-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="56dfa-112">La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="56dfa-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="56dfa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56dfa-113">Requirements</span></span>



| <span data-ttu-id="56dfa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dfa-114">Requirement</span></span> | <span data-ttu-id="56dfa-115">Value</span><span class="sxs-lookup"><span data-stu-id="56dfa-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56dfa-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56dfa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56dfa-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56dfa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56dfa-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56dfa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56dfa-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56dfa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56dfa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56dfa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56dfa-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="56dfa-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dfa-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="56dfa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dfa-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56dfa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="56dfa-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="56dfa-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="56dfa-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="56dfa-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="56dfa-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="56dfa-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="56dfa-127">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="56dfa-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="56dfa-128">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="56dfa-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




