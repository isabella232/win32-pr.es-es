---
description: Especifica el modo downmix estéreo para un descodificador de audio Dolby digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: Propiedad CODECAPI_AVDecDDStereoDownMixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423571"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a><span data-ttu-id="827a1-103">\_Propiedad AVDecDDStereoDownMixMode de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="827a1-103">CODECAPI\_AVDecDDStereoDownMixMode property</span></span>

<span data-ttu-id="827a1-104">Especifica el modo downmix estéreo para un descodificador de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="827a1-104">Specifies the stereo downmix mode for a Dolby Digital audio decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="827a1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="827a1-105">Data type</span></span>

<span data-ttu-id="827a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="827a1-106">**UINT32**</span></span>

## <a name="property-guid"></a><span data-ttu-id="827a1-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="827a1-107">Property GUID</span></span>

<span data-ttu-id="827a1-108">**CODECAPI \_ AVDecDDStereoDownMixMode**</span><span class="sxs-lookup"><span data-stu-id="827a1-108">**CODECAPI\_AVDecDDStereoDownMixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="827a1-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="827a1-109">Property value</span></span>

<span data-ttu-id="827a1-110">El valor de esta propiedad es un miembro de la enumeración [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="827a1-110">The value of this property is a member of the [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="827a1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="827a1-111">Remarks</span></span>

<span data-ttu-id="827a1-112">Este atributo se aplica cuando la entrada para el descodificador es audio PCM multicanal y el resultado es audio estéreo.</span><span class="sxs-lookup"><span data-stu-id="827a1-112">This attribute applies when the input to the decoder is multichannel PCM audio, and the output is stereo audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="827a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="827a1-113">Requirements</span></span>



| <span data-ttu-id="827a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="827a1-114">Requirement</span></span> | <span data-ttu-id="827a1-115">Value</span><span class="sxs-lookup"><span data-stu-id="827a1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="827a1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="827a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="827a1-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="827a1-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="827a1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="827a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="827a1-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="827a1-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="827a1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="827a1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="827a1-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="827a1-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="827a1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="827a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827a1-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="827a1-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="827a1-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="827a1-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

