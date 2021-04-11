---
description: Nivel de volumen promedio de referencia de un archivo de Windows Media Audio.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: MF_MT_AUDIO_WMADRC_AVGREF atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdde0bfb4c2993580d73981e9e121d1f7f18612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275950"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a><span data-ttu-id="c56eb-103">\_ \_ Atributo AVGREF de audio MF MT \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="c56eb-103">MF\_MT\_AUDIO\_WMADRC\_AVGREF attribute</span></span>

<span data-ttu-id="c56eb-104">Nivel de volumen promedio de referencia de un archivo de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="c56eb-104">Reference average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c56eb-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c56eb-105">Data type</span></span>

<span data-ttu-id="c56eb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c56eb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c56eb-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c56eb-107">Remarks</span></span>

<span data-ttu-id="c56eb-108">Este atributo se aplica a los tipos de medios de audio para códecs de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="c56eb-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="c56eb-109">Especifica el nivel de volumen medio original del contenido.</span><span class="sxs-lookup"><span data-stu-id="c56eb-109">It specifies the original average volume level of the content.</span></span> <span data-ttu-id="c56eb-110">El descodificador puede utilizar este valor para realizar un control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c56eb-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="c56eb-111">El método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) .</span><span class="sxs-lookup"><span data-stu-id="c56eb-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) attribute.</span></span> <span data-ttu-id="c56eb-112">Este atributo se documenta en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="c56eb-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="c56eb-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c56eb-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56eb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56eb-114">Requirements</span></span>



| <span data-ttu-id="c56eb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56eb-115">Requirement</span></span> | <span data-ttu-id="c56eb-116">Value</span><span class="sxs-lookup"><span data-stu-id="c56eb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c56eb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c56eb-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c56eb-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c56eb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c56eb-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c56eb-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c56eb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c56eb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c56eb-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c56eb-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56eb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56eb-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c56eb-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c56eb-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c56eb-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c56eb-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c56eb-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c56eb-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c56eb-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c56eb-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="c56eb-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
