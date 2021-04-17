---
description: Especifica el tiempo, en unidades de 100-nanosegundos, necesario para enviar un archivo de formato de sistema avanzado (ASF). La hora de envío de los paquetes es la hora a la que se debe entregar el paquete a través de la red. No es el tiempo de presentación del paquete.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716499"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="a88b8-105">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ enviar \_ atributo Duration</span><span class="sxs-lookup"><span data-stu-id="a88b8-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="a88b8-106">Especifica el tiempo, en unidades de 100-nanosegundos, necesario para enviar un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="a88b8-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a88b8-107">La hora de *envío* de un paquete es la hora a la que se debe entregar el paquete a través de la red.</span><span class="sxs-lookup"><span data-stu-id="a88b8-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="a88b8-108">No es el tiempo de presentación del paquete.</span><span class="sxs-lookup"><span data-stu-id="a88b8-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="a88b8-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a88b8-109">Data type</span></span>

<span data-ttu-id="a88b8-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a88b8-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a88b8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a88b8-111">Remarks</span></span>

<span data-ttu-id="a88b8-112">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="a88b8-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a88b8-113">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="a88b8-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88b8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a88b8-114">Requirements</span></span>



| <span data-ttu-id="a88b8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88b8-115">Requirement</span></span> | <span data-ttu-id="a88b8-116">Value</span><span class="sxs-lookup"><span data-stu-id="a88b8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88b8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a88b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a88b8-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a88b8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a88b8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a88b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a88b8-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a88b8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a88b8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a88b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88b8-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88b8-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88b8-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a88b8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88b8-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a88b8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a88b8-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a88b8-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a88b8-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a88b8-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a88b8-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a88b8-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a88b8-128">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="a88b8-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a88b8-129">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="a88b8-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a88b8-130">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="a88b8-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




