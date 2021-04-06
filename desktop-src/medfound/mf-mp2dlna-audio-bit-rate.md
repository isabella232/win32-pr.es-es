---
description: Especifica la velocidad de bits máxima de audio para el receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001504"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="5e081-103">\_Atributo de \_ velocidad de bits de audio MF MP2DLNA \_ \_</span><span class="sxs-lookup"><span data-stu-id="5e081-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="5e081-104">Especifica la velocidad de bits máxima de audio para el receptor de medios de la Alianza de redes digitales (DLNA).</span><span class="sxs-lookup"><span data-stu-id="5e081-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e081-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5e081-105">Data type</span></span>

<span data-ttu-id="5e081-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5e081-106">**UINT32**</span></span>

<span data-ttu-id="5e081-107">El valor es la velocidad de bits máxima de destino para la secuencia de audio codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="5e081-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="5e081-108">El valor debe ser una de las velocidades de bits permitidas para el audio MPEG-2 de nivel 2 para DLNA.</span><span class="sxs-lookup"><span data-stu-id="5e081-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="5e081-109">El valor predeterminado es 192000 (192 kbps).</span><span class="sxs-lookup"><span data-stu-id="5e081-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="5e081-110">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="5e081-110">Get/set</span></span>

<span data-ttu-id="5e081-111">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5e081-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5e081-112">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5e081-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e081-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e081-113">Remarks</span></span>

<span data-ttu-id="5e081-114">Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="5e081-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="5e081-115">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="5e081-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e081-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e081-116">Requirements</span></span>



| <span data-ttu-id="5e081-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e081-117">Requirement</span></span> | <span data-ttu-id="5e081-118">Value</span><span class="sxs-lookup"><span data-stu-id="5e081-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e081-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e081-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e081-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e081-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5e081-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e081-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e081-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e081-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5e081-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e081-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e081-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e081-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e081-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e081-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e081-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e081-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




