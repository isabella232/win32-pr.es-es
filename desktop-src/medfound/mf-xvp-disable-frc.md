---
description: Deshabilita la conversión de velocidad de fotogramas en la MFT del procesador de vídeo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001356"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="bcb5f-103">MF \_ XVP \_ deshabilitar el \_ atributo FRC</span><span class="sxs-lookup"><span data-stu-id="bcb5f-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="bcb5f-104">Deshabilita la conversión de velocidad de fotogramas en la [**MFT del procesador de vídeo**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="bcb5f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bcb5f-105">Data type</span></span>

<span data-ttu-id="bcb5f-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bcb5f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb5f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcb5f-107">Remarks</span></span>

<span data-ttu-id="bcb5f-108">Si este atributo es **true**, el procesador de vídeo no realizará la conversión de velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="bcb5f-109">De forma predeterminada, el procesador de vídeo convertirá la velocidad de fotogramas para que coincida con el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="bcb5f-110">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="bcb5f-110">To set this attribute:</span></span>

1.  <span data-ttu-id="bcb5f-111">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="bcb5f-112">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="bcb5f-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="bcb5f-113">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="bcb5f-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb5f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb5f-114">Requirements</span></span>



| <span data-ttu-id="bcb5f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb5f-115">Requirement</span></span> | <span data-ttu-id="bcb5f-116">Value</span><span class="sxs-lookup"><span data-stu-id="bcb5f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb5f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb5f-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcb5f-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bcb5f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb5f-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcb5f-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bcb5f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcb5f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb5f-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb5f-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb5f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcb5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb5f-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcb5f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




