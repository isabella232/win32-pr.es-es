---
description: Especifica el perfil de codificación de vídeo en el tipo de medio de salida. Se trata de un alias del \_ atributo de perfil MF MT \_ MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716957"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="b52f7-104">\_Atributo de \_ Perfil de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b52f7-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="b52f7-105">Especifica el perfil de codificación de vídeo en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="b52f7-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="b52f7-106">Se trata de un alias del atributo de [ \_ \_ \_ perfil MF MT MPEG2](mf-mt-mpeg2-profile-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b52f7-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="b52f7-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b52f7-107">Data type</span></span>

<span data-ttu-id="b52f7-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b52f7-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b52f7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b52f7-109">Remarks</span></span>

<span data-ttu-id="b52f7-110">**Codificadores H. 264:**</span><span class="sxs-lookup"><span data-stu-id="b52f7-110">**H.264 encoders:**</span></span>

<span data-ttu-id="b52f7-111">Los perfiles admitidos se superan para incluir [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) y **eAVEncH264VProfile \_ ConstrainedHigh**.</span><span class="sxs-lookup"><span data-stu-id="b52f7-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="b52f7-112">Los codificadores deben admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) y [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para este atributo.</span><span class="sxs-lookup"><span data-stu-id="b52f7-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="b52f7-113">Esto es estático, por lo que los codificadores de vídeo deben configurarse antes de que se inicie la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="b52f7-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="b52f7-114">Si la aplicación establece un perfil que el codificador no admite, el codificador rechazará el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b52f7-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="b52f7-115">Valor predeterminado recomendado: perfil [**\_ principal de eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="b52f7-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52f7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b52f7-116">Requirements</span></span>



| <span data-ttu-id="b52f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52f7-117">Requirement</span></span> | <span data-ttu-id="b52f7-118">Value</span><span class="sxs-lookup"><span data-stu-id="b52f7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b52f7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b52f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b52f7-120">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b52f7-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b52f7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b52f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b52f7-122">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b52f7-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b52f7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b52f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b52f7-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52f7-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52f7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b52f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52f7-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b52f7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
