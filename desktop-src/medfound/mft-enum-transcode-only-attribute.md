---
description: Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423851"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="457e7-103">Atributo \_ de \_ atributo de solo Metacode de enumeración de MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="457e7-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="457e7-104">Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="457e7-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="457e7-105">Actualmente, este atributo solo se aplica a los descodificadores basados en hardware que usan el controlador de AVStream.</span><span class="sxs-lookup"><span data-stu-id="457e7-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="457e7-106">El atributo se almacena en el registro en la información de capacidades del descodificador.</span><span class="sxs-lookup"><span data-stu-id="457e7-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="457e7-107">Para obtener más información, consulte la documentación de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="457e7-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="457e7-108">Normalmente, las aplicaciones no usan este atributo.</span><span class="sxs-lookup"><span data-stu-id="457e7-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="457e7-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="457e7-109">Data type</span></span>

<span data-ttu-id="457e7-110">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="457e7-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="457e7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="457e7-111">Remarks</span></span>

<span data-ttu-id="457e7-112">Si esta entrada del registro está presente y es igual a 1, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) omite el descodificador, a menos que el autor de la llamada haya especificado la marca de **enumeración de MFT \_ \_ \_ \_ solo Transcode** Flag en **MFTEnumEx**.</span><span class="sxs-lookup"><span data-stu-id="457e7-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="457e7-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="457e7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="457e7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="457e7-114">Requirements</span></span>



| <span data-ttu-id="457e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="457e7-115">Requirement</span></span> | <span data-ttu-id="457e7-116">Value</span><span class="sxs-lookup"><span data-stu-id="457e7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="457e7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="457e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="457e7-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="457e7-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="457e7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="457e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="457e7-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="457e7-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="457e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="457e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="457e7-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="457e7-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="457e7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="457e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457e7-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="457e7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="457e7-125">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="457e7-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
