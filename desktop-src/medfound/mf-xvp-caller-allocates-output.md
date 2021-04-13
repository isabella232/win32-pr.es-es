---
description: Especifica si el llamador asignará las texturas utilizadas para la salida.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543219"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="cfa16-103">El \_ autor de la llamada MF XVP \_ asigna el atributo de \_ \_ salida</span><span class="sxs-lookup"><span data-stu-id="cfa16-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="cfa16-104">Especifica si el llamador asignará las texturas utilizadas para la salida.</span><span class="sxs-lookup"><span data-stu-id="cfa16-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfa16-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cfa16-105">Data type</span></span>

<span data-ttu-id="cfa16-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="cfa16-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa16-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfa16-107">Remarks</span></span>

<span data-ttu-id="cfa16-108">Si este atributo es **true**, el procesador de vídeo espera que el autor de la llamada asigne las texturas de salida, incluso cuando se trabaja en modo de aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="cfa16-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="cfa16-109">Si este atributo es **false**, el procesador de vídeo asignará las texturas de salida al operar en modo DXVA y se producirá un error si se proporcionan las texturas de salida proporcionadas por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cfa16-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="cfa16-110">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="cfa16-110">To set this attribute:</span></span>

1.  <span data-ttu-id="cfa16-111">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cfa16-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="cfa16-112">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="cfa16-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="cfa16-113">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="cfa16-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa16-114">Requirements</span></span>



| <span data-ttu-id="cfa16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa16-115">Requirement</span></span> | <span data-ttu-id="cfa16-116">Value</span><span class="sxs-lookup"><span data-stu-id="cfa16-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa16-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfa16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa16-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfa16-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cfa16-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfa16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa16-120">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfa16-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cfa16-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfa16-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa16-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa16-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfa16-123">IDL</span><span class="sxs-lookup"><span data-stu-id="cfa16-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cfa16-124"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cfa16-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa16-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfa16-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa16-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfa16-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




