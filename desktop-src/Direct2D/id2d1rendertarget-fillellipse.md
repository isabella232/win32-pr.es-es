---
title: Métodos ID2D1RenderTarget FillEllipse (D2d1. h)
description: Pinta el interior de la elipse especificada.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- FillEllipse (métodos) Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690053"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="d8920-104">ID2D1RenderTarget:: FillEllipse (métodos)</span><span class="sxs-lookup"><span data-stu-id="d8920-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="d8920-105">Pinta el interior de la elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="d8920-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d8920-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="d8920-106">Overload list</span></span>



| <span data-ttu-id="d8920-107">Método</span><span class="sxs-lookup"><span data-stu-id="d8920-107">Method</span></span>                                                                                                             | <span data-ttu-id="d8920-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8920-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="d8920-109">[**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d8920-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="d8920-110">Pinta el interior de la elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="d8920-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="d8920-111">[**FillEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="d8920-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="d8920-112">Pinta el interior de la elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="d8920-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d8920-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8920-113">Remarks</span></span>

<span data-ttu-id="d8920-114">Este método no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d8920-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="d8920-115">Para determinar si una operación de dibujo (como **FillEllipse**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="d8920-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="d8920-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d8920-116">Examples</span></span>

<span data-ttu-id="d8920-117">Para obtener un ejemplo, vea [Cómo dibujar y rellenar una forma básica](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="d8920-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8920-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8920-118">Requirements</span></span>



| <span data-ttu-id="d8920-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8920-119">Requirement</span></span> | <span data-ttu-id="d8920-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8920-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d8920-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8920-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8920-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8920-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8920-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8920-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8920-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8920-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8920-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8920-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8920-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8920-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8920-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8920-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8920-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="d8920-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="d8920-129">Cómo dibujar y rellenar una forma básica</span><span class="sxs-lookup"><span data-stu-id="d8920-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="d8920-130">�</span><span class="sxs-lookup"><span data-stu-id="d8920-130">�</span></span>

<span data-ttu-id="d8920-131">�</span><span class="sxs-lookup"><span data-stu-id="d8920-131">�</span></span>
