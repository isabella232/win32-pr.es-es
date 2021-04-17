---
description: Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo. Este proceso también se denomina doblei.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: MF_MT_AUDIO_FOLDDOWN_MATRIX atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687214"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="0cbed-104">MF \_ MT \_ audio \_ FOLDDOWN \_ Matrix (atributo)</span><span class="sxs-lookup"><span data-stu-id="0cbed-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="0cbed-105">Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo.</span><span class="sxs-lookup"><span data-stu-id="0cbed-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="0cbed-106">Este proceso también se denomina *doblei*.</span><span class="sxs-lookup"><span data-stu-id="0cbed-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cbed-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0cbed-107">Data type</span></span>

<span data-ttu-id="0cbed-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="0cbed-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbed-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cbed-109">Remarks</span></span>

<span data-ttu-id="0cbed-110">Este atributo se aplica a los tipos de medios de audio.</span><span class="sxs-lookup"><span data-stu-id="0cbed-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="0cbed-111">El valor de este atributo es una estructura de [**\_ matriz MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .</span><span class="sxs-lookup"><span data-stu-id="0cbed-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="0cbed-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0cbed-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cbed-113">Requirements</span></span>



| <span data-ttu-id="0cbed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cbed-114">Requirement</span></span> | <span data-ttu-id="0cbed-115">Value</span><span class="sxs-lookup"><span data-stu-id="0cbed-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbed-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cbed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0cbed-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="0cbed-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0cbed-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cbed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0cbed-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0cbed-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0cbed-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cbed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cbed-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cbed-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbed-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cbed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbed-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0cbed-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0cbed-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="0cbed-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="0cbed-125">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="0cbed-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="0cbed-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0cbed-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0cbed-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="0cbed-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




