---
title: Métodos ID2D1RenderTarget FillOpacityMask
description: Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Métodos de FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660207"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="142fe-104">ID2D1RenderTarget:: FillOpacityMask (métodos)</span><span class="sxs-lookup"><span data-stu-id="142fe-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="142fe-105">Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="142fe-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="142fe-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="142fe-106">Overload list</span></span>



| <span data-ttu-id="142fe-107">Método</span><span class="sxs-lookup"><span data-stu-id="142fe-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="142fe-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="142fe-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="142fe-109">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 de la \_ máscara de opacidad \_ \_ , D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="142fe-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="142fe-110">Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="142fe-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="142fe-111">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 de la \_ máscara de opacidad \_ \_ , D2D \_ Rect \_ f \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="142fe-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="142fe-112">Aplica la máscara de opacidad descrita por el mapa de bits especificado a un pincel y usa ese pincel para pintar una región del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="142fe-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="142fe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="142fe-113">Remarks</span></span>

<span data-ttu-id="142fe-114">Para que este método funcione correctamente, el destino de representación debe usar el modo de suavizado de contorno con [**\_ \_ \_ alias del modo de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialias.</span><span class="sxs-lookup"><span data-stu-id="142fe-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="142fe-115">Puede establecer el modo de suavizado de contorno llamando al método [**ID2D1RenderTarget:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .</span><span class="sxs-lookup"><span data-stu-id="142fe-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="142fe-116">Este método no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="142fe-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="142fe-117">Para determinar si una operación de dibujo (como **FillOpacityMask**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="142fe-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="142fe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="142fe-118">Requirements</span></span>



| <span data-ttu-id="142fe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="142fe-119">Requirement</span></span> | <span data-ttu-id="142fe-120">Value</span><span class="sxs-lookup"><span data-stu-id="142fe-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="142fe-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="142fe-121">Library</span></span><br/> | <dl> <span data-ttu-id="142fe-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="142fe-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="142fe-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="142fe-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="142fe-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142fe-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142fe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="142fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142fe-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="142fe-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

