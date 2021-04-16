---
description: Especifica el tamaño máximo de QP compatible con el codificador.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Propiedad CODECAPI_AVEncVideoMaxQP (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696172"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="803f4-103">\_Propiedad AVEncVideoMaxQP de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="803f4-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="803f4-104">Especifica el tamaño máximo de QP compatible con el codificador.</span><span class="sxs-lookup"><span data-stu-id="803f4-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="803f4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="803f4-105">Data type</span></span>

<span data-ttu-id="803f4-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="803f4-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="803f4-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="803f4-107">Property GUID</span></span>

<span data-ttu-id="803f4-108">**CODECAPI \_ AVEncVideoMaxQP**</span><span class="sxs-lookup"><span data-stu-id="803f4-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="803f4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="803f4-109">Remarks</span></span>

<span data-ttu-id="803f4-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="803f4-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="803f4-111">El codificador debe admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="803f4-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="803f4-112">Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="803f4-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="803f4-113">El valor predeterminado será el máximo de QP permitido por el estándar de codificación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="803f4-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="803f4-114">Por ejemplo, los codificadores H. 264 deben tener un valor predeterminado de 51.</span><span class="sxs-lookup"><span data-stu-id="803f4-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="803f4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="803f4-115">Requirements</span></span>



| <span data-ttu-id="803f4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="803f4-116">Requirement</span></span> | <span data-ttu-id="803f4-117">Value</span><span class="sxs-lookup"><span data-stu-id="803f4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="803f4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="803f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="803f4-119">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="803f4-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="803f4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="803f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="803f4-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="803f4-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="803f4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="803f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="803f4-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="803f4-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803f4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="803f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803f4-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="803f4-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="803f4-126">CODECAPI \_ AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="803f4-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

