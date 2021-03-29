---
title: Métodos ID2D1RenderTarget CreateRadialGradientBrush (D2d1. h)
description: Crea un objeto ID2D1RadialGradientBrush que se puede usar para pintar áreas con un degradado radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Métodos de CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679224"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a><span data-ttu-id="42455-104">ID2D1RenderTarget:: CreateRadialGradientBrush (métodos)</span><span class="sxs-lookup"><span data-stu-id="42455-104">ID2D1RenderTarget::CreateRadialGradientBrush methods</span></span>

<span data-ttu-id="42455-105">Crea un objeto [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que se puede usar para pintar áreas con un degradado radial.</span><span class="sxs-lookup"><span data-stu-id="42455-105">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) object that can be used to paint areas with a radial gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="42455-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="42455-106">Overload list</span></span>



| <span data-ttu-id="42455-107">Método</span><span class="sxs-lookup"><span data-stu-id="42455-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="42455-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="42455-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42455-109">[**CreateRadialGradientBrush (D2D1 \_ \_ \_ propiedades de pincel de degradado radial \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="42455-109">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>                            | <span data-ttu-id="42455-110">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados, no tiene ninguna transformación y tiene una opacidad base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="42455-110">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="42455-111">[**CreateRadialGradientBrush (D2D1 \_ \_ propiedades de pincel de degradado radial \_ \_&, \_ propiedades del pincel de D2D1 \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="42455-111">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>   | <span data-ttu-id="42455-112">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas.</span><span class="sxs-lookup"><span data-stu-id="42455-112">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="42455-113">[**CreateRadialGradientBrush ( \_ \_ \_ propiedades del pincel de degradado radial \_ de D2D1 \* , \_ propiedades del pincel de D2D1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="42455-113">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span> | <span data-ttu-id="42455-114">Crea un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas.</span><span class="sxs-lookup"><span data-stu-id="42455-114">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="42455-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="42455-115">Examples</span></span>

<span data-ttu-id="42455-116">Para obtener un ejemplo, consulte [creación de un pincel de degradado radial](how-to-create-a-radial-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="42455-116">For an example, see [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42455-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42455-117">Requirements</span></span>



| <span data-ttu-id="42455-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="42455-118">Requirement</span></span> | <span data-ttu-id="42455-119">Value</span><span class="sxs-lookup"><span data-stu-id="42455-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42455-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42455-120">Header</span></span><br/>  | <dl> <span data-ttu-id="42455-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="42455-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="42455-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42455-122">Library</span></span><br/> | <dl> <span data-ttu-id="42455-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42455-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="42455-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42455-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="42455-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42455-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42455-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="42455-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42455-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="42455-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="42455-128">Cómo crear un pincel de degradado radial</span><span class="sxs-lookup"><span data-stu-id="42455-128">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="42455-129">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="42455-129">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="42455-130">�</span><span class="sxs-lookup"><span data-stu-id="42455-130">�</span></span>

<span data-ttu-id="42455-131">�</span><span class="sxs-lookup"><span data-stu-id="42455-131">�</span></span>
