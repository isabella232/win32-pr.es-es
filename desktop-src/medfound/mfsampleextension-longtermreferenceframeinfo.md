---
description: Especifica la información de marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689678"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="9f293-103">\_Atributo LongTermReferenceFrameInfo de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="9f293-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="9f293-104">Especifica la información de marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="9f293-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="9f293-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9f293-105">Data type</span></span>

<span data-ttu-id="9f293-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9f293-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9f293-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f293-107">Remarks</span></span>

<span data-ttu-id="9f293-108">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="9f293-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="9f293-109">Los codificadores devolverán este atributo en el ejemplo de salida cuando la aplicación controle Marcos LTR, que se especifica mediante [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="9f293-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="9f293-110">MFSampleExtension \_ LongTermReferenceFrameInfo devuelve hasta dos campos.</span><span class="sxs-lookup"><span data-stu-id="9f293-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="9f293-111">El primer campo, bits \[ 0.. 15 \] , se *LongTermFrameIdx* asociado con el fotograma de salida si está marcado como marco LTR.</span><span class="sxs-lookup"><span data-stu-id="9f293-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="9f293-112">El primer valor es 0xFFFF, si este fotograma de salida es un marco de referencia a corto plazo o un fotograma sin referencia.</span><span class="sxs-lookup"><span data-stu-id="9f293-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="9f293-113">El segundo campo, bits \[ 16... 31 \] , es un mapa de bits que se compone de *MaxNumLTRFrames* muchos bits que indican qué Marcos LTR se usaron para codificar este fotograma de salida, empezando por el bit 16.</span><span class="sxs-lookup"><span data-stu-id="9f293-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="9f293-114">El resto de bits se establecerá en 0.</span><span class="sxs-lookup"><span data-stu-id="9f293-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="9f293-115">El segundo valor es 0 si este fotograma de salida no se codifica con ningún marco LTR.</span><span class="sxs-lookup"><span data-stu-id="9f293-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="9f293-116">*MaxNumLTRFrames* es el número máximo de Marcos LTR establecidos a través de [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="9f293-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f293-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f293-117">Requirements</span></span>



| <span data-ttu-id="9f293-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f293-118">Requirement</span></span> | <span data-ttu-id="9f293-119">Value</span><span class="sxs-lookup"><span data-stu-id="9f293-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f293-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f293-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f293-121">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9f293-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="9f293-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f293-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f293-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9f293-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9f293-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f293-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f293-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f293-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f293-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f293-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f293-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f293-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




