---
description: Especifica el número máximo de fotogramas de referencia que admite el codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Propiedad CODECAPI_AVEncVideoMaxNumRefFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157008"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="3e77b-103">\_Propiedad AVEncVideoMaxNumRefFrame de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="3e77b-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="3e77b-104">Especifica el número máximo de fotogramas de referencia que admite el codificador.</span><span class="sxs-lookup"><span data-stu-id="3e77b-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e77b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3e77b-105">Data type</span></span>

<span data-ttu-id="3e77b-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="3e77b-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3e77b-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="3e77b-107">Property GUID</span></span>

<span data-ttu-id="3e77b-108">**CODECAPI \_ AVEncVideoMaxNumRefFrame**</span><span class="sxs-lookup"><span data-stu-id="3e77b-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="3e77b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e77b-109">Remarks</span></span>

<span data-ttu-id="3e77b-110">Para H. 264, se asigna a la variable de conjunto de parámetros de secuencia set **Max \_ NUM \_ \_ frames** , tal y como se define en la especificación H. 264.</span><span class="sxs-lookup"><span data-stu-id="3e77b-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="3e77b-111">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="3e77b-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="3e77b-112">Los codificadores pueden usar menos fotogramas de referencia para obedecer el nivel especificado en el fragmentada.</span><span class="sxs-lookup"><span data-stu-id="3e77b-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="3e77b-113">Los codificadores deben admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)y [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="3e77b-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="3e77b-114">Se trata de una propiedad estática que significa que solo se puede establecer antes de que se inicie la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="3e77b-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="3e77b-115">El valor predeterminado recomendado es 2.</span><span class="sxs-lookup"><span data-stu-id="3e77b-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e77b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e77b-116">Requirements</span></span>



| <span data-ttu-id="3e77b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e77b-117">Requirement</span></span> | <span data-ttu-id="3e77b-118">Value</span><span class="sxs-lookup"><span data-stu-id="3e77b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e77b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e77b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e77b-120">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="3e77b-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="3e77b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e77b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e77b-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3e77b-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3e77b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e77b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e77b-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e77b-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e77b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e77b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e77b-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e77b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

