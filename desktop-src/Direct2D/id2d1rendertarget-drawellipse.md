---
title: Métodos DrawEllipse ID2D1RenderTarget (D2d1. h)
description: Dibuja el contorno de una elipse con las dimensiones y el trazo especificados.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Métodos DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690160"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="332b7-104">ID2D1RenderTarget::D rawEllipse métodos)</span><span class="sxs-lookup"><span data-stu-id="332b7-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="332b7-105">Dibuja el contorno de una elipse con las dimensiones y el trazo especificados.</span><span class="sxs-lookup"><span data-stu-id="332b7-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="332b7-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="332b7-106">Overload list</span></span>



| <span data-ttu-id="332b7-107">Método</span><span class="sxs-lookup"><span data-stu-id="332b7-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="332b7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="332b7-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="332b7-109">[**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , Float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="332b7-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="332b7-110">Dibuja el contorno de la elipse especificada utilizando el estilo de trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="332b7-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="332b7-111">[**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , Float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="332b7-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="332b7-112">Dibuja el contorno de la elipse especificada utilizando el estilo de trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="332b7-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="332b7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="332b7-113">Remarks</span></span>

<span data-ttu-id="332b7-114">El método **DrawEllipse** no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="332b7-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="332b7-115">Para determinar si una operación de dibujo (como **DrawEllipse**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="332b7-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="332b7-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="332b7-116">Examples</span></span>

<span data-ttu-id="332b7-117">Para obtener un ejemplo, vea [Cómo dibujar y rellenar una forma básica](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="332b7-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="332b7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="332b7-118">Requirements</span></span>



| <span data-ttu-id="332b7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="332b7-119">Requirement</span></span> | <span data-ttu-id="332b7-120">Value</span><span class="sxs-lookup"><span data-stu-id="332b7-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="332b7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="332b7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="332b7-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="332b7-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="332b7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="332b7-123">Library</span></span><br/> | <dl> <span data-ttu-id="332b7-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="332b7-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="332b7-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="332b7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="332b7-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="332b7-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332b7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="332b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332b7-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="332b7-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="332b7-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="332b7-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="332b7-130">�</span><span class="sxs-lookup"><span data-stu-id="332b7-130">�</span></span>

<span data-ttu-id="332b7-131">�</span><span class="sxs-lookup"><span data-stu-id="332b7-131">�</span></span>
