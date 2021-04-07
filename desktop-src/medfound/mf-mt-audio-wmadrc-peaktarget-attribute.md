---
description: Nivel de volumen máximo de destino de un archivo de Windows Media Audio.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: MF_MT_AUDIO_WMADRC_PEAKTARGET atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002627"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a><span data-ttu-id="68d17-103">\_ \_ Atributo PEAKTARGET de audio MF MT \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="68d17-103">MF\_MT\_AUDIO\_WMADRC\_PEAKTARGET attribute</span></span>

<span data-ttu-id="68d17-104">Nivel de volumen máximo de destino de un archivo de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="68d17-104">Target peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="68d17-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="68d17-105">Data type</span></span>

<span data-ttu-id="68d17-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68d17-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="68d17-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68d17-107">Remarks</span></span>

<span data-ttu-id="68d17-108">Este atributo se aplica a los tipos de medios de audio para códecs de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="68d17-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="68d17-109">Especifica el nivel de volumen máximo de destino del contenido.</span><span class="sxs-lookup"><span data-stu-id="68d17-109">It specifies the target peak volume level of the content.</span></span> <span data-ttu-id="68d17-110">El descodificador puede utilizar este valor para realizar un control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="68d17-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="68d17-111">El método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) .</span><span class="sxs-lookup"><span data-stu-id="68d17-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) attribute.</span></span> <span data-ttu-id="68d17-112">Este atributo se documenta en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="68d17-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="68d17-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68d17-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d17-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68d17-114">Requirements</span></span>



| <span data-ttu-id="68d17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68d17-115">Requirement</span></span> | <span data-ttu-id="68d17-116">Value</span><span class="sxs-lookup"><span data-stu-id="68d17-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68d17-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68d17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68d17-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="68d17-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="68d17-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68d17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68d17-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="68d17-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="68d17-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68d17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d17-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68d17-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68d17-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="68d17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d17-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68d17-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68d17-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68d17-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68d17-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68d17-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68d17-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="68d17-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="68d17-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="68d17-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
