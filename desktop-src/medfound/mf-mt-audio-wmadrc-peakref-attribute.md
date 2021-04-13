---
description: Nivel de volumen máximo de referencia de un archivo de Windows Media Audio.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: MF_MT_AUDIO_WMADRC_PEAKREF atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544347"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="40a62-103">\_ \_ Atributo PEAKREF de audio MF MT \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="40a62-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="40a62-104">Nivel de volumen máximo de referencia de un archivo de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="40a62-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="40a62-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="40a62-105">Data type</span></span>

<span data-ttu-id="40a62-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="40a62-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="40a62-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40a62-107">Remarks</span></span>

<span data-ttu-id="40a62-108">Este atributo se aplica a los tipos de medios de audio para códecs de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="40a62-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="40a62-109">Especifica el nivel de volumen máximo original del contenido.</span><span class="sxs-lookup"><span data-stu-id="40a62-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="40a62-110">El descodificador puede utilizar este valor para realizar un control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="40a62-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="40a62-111">El método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) .</span><span class="sxs-lookup"><span data-stu-id="40a62-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="40a62-112">Este atributo se documenta en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="40a62-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="40a62-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="40a62-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a62-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a62-114">Requirements</span></span>



| <span data-ttu-id="40a62-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a62-115">Requirement</span></span> | <span data-ttu-id="40a62-116">Value</span><span class="sxs-lookup"><span data-stu-id="40a62-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40a62-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40a62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40a62-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="40a62-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="40a62-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40a62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40a62-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="40a62-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="40a62-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40a62-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a62-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a62-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a62-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="40a62-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a62-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40a62-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="40a62-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="40a62-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="40a62-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="40a62-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="40a62-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="40a62-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="40a62-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="40a62-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
