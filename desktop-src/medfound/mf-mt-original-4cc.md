---
description: Contiene el objeto FOURCC del códec original para una secuencia de vídeo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: MF_MT_ORIGINAL_4CC atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002626"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="65905-103">MF \_ MT \_ original \_ 4cc atributo</span><span class="sxs-lookup"><span data-stu-id="65905-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="65905-104">Contiene el objeto FOURCC del códec original para una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="65905-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="65905-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="65905-105">Data type</span></span>

<span data-ttu-id="65905-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="65905-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="65905-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="65905-107">Get/set</span></span>

<span data-ttu-id="65905-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="65905-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="65905-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="65905-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="65905-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="65905-110">Applies to</span></span>

[<span data-ttu-id="65905-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="65905-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="65905-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65905-112">Remarks</span></span>

<span data-ttu-id="65905-113">Dependiendo del archivo de origen, el origen de medios AVI podría establecer este atributo en los tipos de medios que ofrece.</span><span class="sxs-lookup"><span data-stu-id="65905-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="65905-114">Un archivo AVI contiene un encabezado de secuencia para cada flujo del archivo.</span><span class="sxs-lookup"><span data-stu-id="65905-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="65905-115">El origen de medios AVI traduce el encabezado de secuencia en un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="65905-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="65905-116">En el caso de las secuencias de vídeo comprimidas, el encabezado de flujo contiene un FOURCC que identifica el códec de vídeo.</span><span class="sxs-lookup"><span data-stu-id="65905-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="65905-117">En la mayoría de los casos, el origen de medios AVI convierte este FOURCC directamente en un GUID de subtipo, tal y como se describe en el tema [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="65905-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="65905-118">En algunos casos, sin embargo, asigna el FOURCC original a otro FOURCC equivalente.</span><span class="sxs-lookup"><span data-stu-id="65905-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="65905-119">Si es así, el origen de medios almacena el FOURCC original en el tipo de medio, mediante el \_ \_ atributo 4cc original MF MT \_ .</span><span class="sxs-lookup"><span data-stu-id="65905-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="65905-120">Las asignaciones de FOURCC se almacenan en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="65905-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="65905-121">**HKEY \_ MediaFoundation \_ raíz de clases** \\  \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="65905-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="65905-122">Cada entrada es un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="65905-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="65905-123">El nombre de la entrada es la representación hexadecimal del FOURCC, sin un prefijo "0x", y con el primer carácter que aparece primero en la cadena.</span><span class="sxs-lookup"><span data-stu-id="65905-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="65905-124">Por ejemplo, el código FOURCC ' abcd ' aparecería como "61626364".</span><span class="sxs-lookup"><span data-stu-id="65905-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="65905-125">El valor de la entrada es el código FOURCC equivalente.</span><span class="sxs-lookup"><span data-stu-id="65905-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="65905-126">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="65905-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="65905-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65905-127">Requirements</span></span>



| <span data-ttu-id="65905-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="65905-128">Requirement</span></span> | <span data-ttu-id="65905-129">Value</span><span class="sxs-lookup"><span data-stu-id="65905-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65905-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65905-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65905-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="65905-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="65905-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65905-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65905-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="65905-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="65905-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65905-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="65905-135"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="65905-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65905-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="65905-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65905-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="65905-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="65905-138">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="65905-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




