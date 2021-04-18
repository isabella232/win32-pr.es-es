---
description: Especifica si se va a difundir o buscar un archivo de formato de sistema avanzado (ASF). Este valor corresponde al campo Flags del objeto de propiedades de archivo, definido en la especificación ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: MF_PD_ASF_FILEPROPERTIES_FLAGS atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659922"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="74f3f-104">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ atributo Flags</span><span class="sxs-lookup"><span data-stu-id="74f3f-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="74f3f-105">Especifica si se va a difundir o buscar un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="74f3f-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="74f3f-106">Este valor corresponde al campo Flags del objeto de propiedades de archivo, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="74f3f-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="74f3f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74f3f-107">Data type</span></span>

<span data-ttu-id="74f3f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="74f3f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="74f3f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74f3f-109">Remarks</span></span>

<span data-ttu-id="74f3f-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="74f3f-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="74f3f-111">El valor del atributo es una operación OR bit a bit de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="74f3f-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="74f3f-112">Marca</span><span class="sxs-lookup"><span data-stu-id="74f3f-112">Flag</span></span> | <span data-ttu-id="74f3f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="74f3f-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f3f-114">0x01</span><span class="sxs-lookup"><span data-stu-id="74f3f-114">0x01</span></span> | <span data-ttu-id="74f3f-115">Marca de difusión.</span><span class="sxs-lookup"><span data-stu-id="74f3f-115">Broadcast flag.</span></span> <span data-ttu-id="74f3f-116">El archivo está en proceso de creación.</span><span class="sxs-lookup"><span data-stu-id="74f3f-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="74f3f-117">0x02</span><span class="sxs-lookup"><span data-stu-id="74f3f-117">0x02</span></span> | <span data-ttu-id="74f3f-118">Marca de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="74f3f-118">Seekable flag.</span></span> <span data-ttu-id="74f3f-119">Se busca en el archivo.</span><span class="sxs-lookup"><span data-stu-id="74f3f-119">The file is seekable.</span></span><br/> <span data-ttu-id="74f3f-120">Se hace búsquedas en un archivo si hay una secuencia de audio y el tamaño máximo del paquete de datos es igual al tamaño mínimo de los paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="74f3f-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="74f3f-121">También se puede buscar en si el archivo tiene una secuencia de audio y una secuencia de vídeo con un objeto de índice simple coincidente.</span><span class="sxs-lookup"><span data-stu-id="74f3f-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="74f3f-122">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="74f3f-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="74f3f-123">Si se establece la marca de difusión, los siguientes atributos del descriptor de presentación no son válidos:</span><span class="sxs-lookup"><span data-stu-id="74f3f-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="74f3f-124">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ ID. de archivo**</span><span class="sxs-lookup"><span data-stu-id="74f3f-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="74f3f-125">**MF \_ PD \_ ASF \_ \_ hora de creación FILEPROPERTIES \_**</span><span class="sxs-lookup"><span data-stu-id="74f3f-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="74f3f-126">**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="74f3f-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="74f3f-127">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ duración de la reproducción**</span><span class="sxs-lookup"><span data-stu-id="74f3f-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="74f3f-128">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ duración del envío \_**</span><span class="sxs-lookup"><span data-stu-id="74f3f-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="74f3f-129">Además, el atributo de tamaño de [**paquete de MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ \_ Max**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) y los valores de atributo de [**tamaño de \_ paquete de MF PD \_ ASF \_ FILEPROPERTIES \_ \_ \_**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) se establecen en el tamaño de paquete real.</span><span class="sxs-lookup"><span data-stu-id="74f3f-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f3f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74f3f-130">Requirements</span></span>



| <span data-ttu-id="74f3f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="74f3f-131">Requirement</span></span> | <span data-ttu-id="74f3f-132">Value</span><span class="sxs-lookup"><span data-stu-id="74f3f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f3f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74f3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74f3f-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74f3f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="74f3f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74f3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74f3f-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="74f3f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="74f3f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74f3f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f3f-138"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f3f-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f3f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="74f3f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f3f-140">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74f3f-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="74f3f-141">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="74f3f-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="74f3f-142">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="74f3f-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="74f3f-143">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="74f3f-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="74f3f-144">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="74f3f-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="74f3f-145">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="74f3f-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="74f3f-146">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="74f3f-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




