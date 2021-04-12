---
description: Nivel de volumen medio de destino de un archivo de Windows Media Audio.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: MF_MT_AUDIO_WMADRC_AVGTARGET atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361425"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a><span data-ttu-id="28add-103">\_ \_ Atributo AVGTARGET de audio MF MT \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="28add-103">MF\_MT\_AUDIO\_WMADRC\_AVGTARGET attribute</span></span>

<span data-ttu-id="28add-104">Nivel de volumen medio de destino de un archivo de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="28add-104">Target average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="28add-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="28add-105">Data type</span></span>

<span data-ttu-id="28add-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="28add-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="28add-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28add-107">Remarks</span></span>

<span data-ttu-id="28add-108">Este atributo se aplica a los tipos de medios de audio para códecs de Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="28add-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="28add-109">Especifica el nivel de volumen medio de destino del contenido.</span><span class="sxs-lookup"><span data-stu-id="28add-109">It specifies the target average volume level of the content.</span></span> <span data-ttu-id="28add-110">El descodificador puede utilizar este valor para realizar un control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="28add-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="28add-111">El método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) agrega este atributo al tipo de medio si el encabezado ASF contiene el atributo [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) .</span><span class="sxs-lookup"><span data-stu-id="28add-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) attribute.</span></span> <span data-ttu-id="28add-112">Este atributo se documenta en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="28add-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="28add-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="28add-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="28add-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28add-114">Requirements</span></span>



| <span data-ttu-id="28add-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28add-115">Requirement</span></span> | <span data-ttu-id="28add-116">Value</span><span class="sxs-lookup"><span data-stu-id="28add-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28add-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28add-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28add-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="28add-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="28add-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28add-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28add-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="28add-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="28add-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28add-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28add-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28add-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28add-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="28add-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28add-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28add-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28add-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="28add-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="28add-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="28add-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="28add-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="28add-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="28add-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="28add-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
