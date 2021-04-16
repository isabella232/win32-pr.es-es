---
description: Especifica el idioma que usa una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648475"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="f7b8c-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ atributo de índice de ID. de idioma \_</span><span class="sxs-lookup"><span data-stu-id="f7b8c-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="f7b8c-104">Especifica el idioma que usa una secuencia en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f7b8c-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f7b8c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f7b8c-105">Data type</span></span>

<span data-ttu-id="f7b8c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f7b8c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b8c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7b8c-107">Remarks</span></span>

<span data-ttu-id="f7b8c-108">Este atributo se aplica a los descriptores de flujo para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="f7b8c-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="f7b8c-109">El valor es un índice de la lista de idiomas que se encuentra en el atributo [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f7b8c-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="f7b8c-110">Este atributo corresponde al campo de índice de ID. de lenguaje de secuencia del objeto Extended Stream Properties.</span><span class="sxs-lookup"><span data-stu-id="f7b8c-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="f7b8c-111">Para obtener más información, consulte la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="f7b8c-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="f7b8c-112">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.</span><span class="sxs-lookup"><span data-stu-id="f7b8c-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="f7b8c-113">La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="f7b8c-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="f7b8c-114">También puede obtener la etiqueta de idioma consultando el descriptor de flujo para el atributo de [**\_ \_ idioma MF SD**](mf-sd-language-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b8c-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b8c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7b8c-115">Requirements</span></span>



| <span data-ttu-id="f7b8c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b8c-116">Requirement</span></span> | <span data-ttu-id="f7b8c-117">Value</span><span class="sxs-lookup"><span data-stu-id="f7b8c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b8c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b8c-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b8c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f7b8c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7b8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b8c-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b8c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f7b8c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7b8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b8c-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b8c-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b8c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7b8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b8c-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7b8c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f7b8c-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f7b8c-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f7b8c-127">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f7b8c-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f7b8c-128">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f7b8c-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="f7b8c-129">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="f7b8c-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f7b8c-130">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="f7b8c-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




