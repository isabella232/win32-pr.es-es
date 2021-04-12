---
title: Constantes de GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes especifican la posición de carácter que se va a devolver en función de las coordenadas de pantalla del punto en relación con un rectángulo de selección de caracteres.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489706"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="7adbe-103">Constantes de GXFPF \_ \*</span><span class="sxs-lookup"><span data-stu-id="7adbe-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="7adbe-104">\_ \* Las constantes GXFPF especifican la posición de carácter que se va a devolver en función de las coordenadas de pantalla del punto en relación con un rectángulo de selección de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adbe-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="7adbe-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7adbe-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="7adbe-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7adbe-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="7adbe-107"><dt>**GXFPF \_ REDONDEO \_ más próximo**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7adbe-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="7adbe-108">Si las coordenadas de pantalla del punto están contenidas en un cuadro de límite de caracteres, la posición de carácter devuelta es el borde de límite más próximo a las coordenadas de pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="7adbe-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="7adbe-109"><dt>**GXFPF \_ MÁS próximo**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="7adbe-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="7adbe-110">Si las coordenadas de pantalla del punto no están contenidas en un cuadro de límite de caracteres, se devuelve la posición del carácter más cercano.</span><span class="sxs-lookup"><span data-stu-id="7adbe-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="7adbe-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7adbe-111">Remarks</span></span>

<span data-ttu-id="7adbe-112">Los parámetros *dwFlags* de los métodos [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) y [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usan estas constantes.</span><span class="sxs-lookup"><span data-stu-id="7adbe-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adbe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7adbe-113">Requirements</span></span>



| <span data-ttu-id="7adbe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adbe-114">Requirement</span></span> | <span data-ttu-id="7adbe-115">Value</span><span class="sxs-lookup"><span data-stu-id="7adbe-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adbe-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adbe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7adbe-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7adbe-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7adbe-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adbe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7adbe-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7adbe-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7adbe-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7adbe-120">Redistributable</span></span><br/>          | <span data-ttu-id="7adbe-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7adbe-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="7adbe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7adbe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adbe-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="7adbe-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="7adbe-124">IDL</span><span class="sxs-lookup"><span data-stu-id="7adbe-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7adbe-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7adbe-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adbe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7adbe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adbe-127">ITextStoreACP:: GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="7adbe-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="7adbe-128">ITfContextOwner::GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="7adbe-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





