---
title: Métodos de ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Métodos de PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681204"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="87cb7-104">ID2D1RenderTarget::P ushAxisAlignedClip métodos)</span><span class="sxs-lookup"><span data-stu-id="87cb7-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="87cb7-105">Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="87cb7-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="87cb7-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="87cb7-106">Overload list</span></span>



| <span data-ttu-id="87cb7-107">Método</span><span class="sxs-lookup"><span data-stu-id="87cb7-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="87cb7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="87cb7-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cb7-109">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, D2D1 \_ antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="87cb7-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="87cb7-110">Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="87cb7-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="87cb7-111">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , D2D1 \_ antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="87cb7-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="87cb7-112">Especifica un rectángulo en el que se recortan todas las operaciones de dibujo subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="87cb7-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="87cb7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87cb7-113">Remarks</span></span>

<span data-ttu-id="87cb7-114">Un par [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) puede aparecer alrededor o dentro de [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), pero no puede superponerse.</span><span class="sxs-lookup"><span data-stu-id="87cb7-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="87cb7-115">Por ejemplo, la secuencia de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** es válida, pero la secuencia de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** no es válida.</span><span class="sxs-lookup"><span data-stu-id="87cb7-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="87cb7-116">Este método no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="87cb7-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="87cb7-117">Para determinar si una operación de dibujo (como **PushAxisAlignedClip**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="87cb7-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="87cb7-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="87cb7-118">Examples</span></span>

<span data-ttu-id="87cb7-119">Para obtener un ejemplo, consulte [Cómo recortar con un Axis-Aligned rectángulo de recorte](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="87cb7-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87cb7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87cb7-120">Requirements</span></span>



| <span data-ttu-id="87cb7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cb7-121">Requirement</span></span> | <span data-ttu-id="87cb7-122">Value</span><span class="sxs-lookup"><span data-stu-id="87cb7-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cb7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87cb7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87cb7-124"><dt>D2d1 \_ 1. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87cb7-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="87cb7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87cb7-125">Library</span></span><br/> | <dl> <span data-ttu-id="87cb7-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87cb7-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="87cb7-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87cb7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="87cb7-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87cb7-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="87cb7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="87cb7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cb7-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="87cb7-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="87cb7-131">�</span><span class="sxs-lookup"><span data-stu-id="87cb7-131">�</span></span>

<span data-ttu-id="87cb7-132">�</span><span class="sxs-lookup"><span data-stu-id="87cb7-132">�</span></span>
