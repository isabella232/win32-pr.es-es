---
description: Especifica la velocidad de bits de vídeo máxima del receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275954"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="03e69-103">\_Atributo de \_ velocidad de bits de vídeo MF MP2DLNA \_ \_</span><span class="sxs-lookup"><span data-stu-id="03e69-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="03e69-104">Especifica la velocidad de bits de vídeo máxima del receptor de medios de la Alianza de redes digitales (DLNA).</span><span class="sxs-lookup"><span data-stu-id="03e69-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="03e69-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="03e69-105">Data type</span></span>

<span data-ttu-id="03e69-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03e69-106">**UINT32**</span></span>

<span data-ttu-id="03e69-107">El valor es la velocidad de bits máxima de destino para la secuencia de vídeo codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="03e69-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="03e69-108">El valor máximo es 9,8 millones (9,8 Mbps), que también es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03e69-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="03e69-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="03e69-109">Get/set</span></span>

<span data-ttu-id="03e69-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="03e69-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="03e69-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="03e69-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="03e69-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03e69-112">Remarks</span></span>

<span data-ttu-id="03e69-113">Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="03e69-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="03e69-114">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="03e69-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e69-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03e69-115">Requirements</span></span>



| <span data-ttu-id="03e69-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e69-116">Requirement</span></span> | <span data-ttu-id="03e69-117">Value</span><span class="sxs-lookup"><span data-stu-id="03e69-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03e69-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03e69-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="03e69-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03e69-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03e69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03e69-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="03e69-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03e69-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03e69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03e69-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e69-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e69-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e69-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e69-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03e69-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




