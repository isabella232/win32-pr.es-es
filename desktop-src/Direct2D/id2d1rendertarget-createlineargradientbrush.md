---
title: Métodos ID2D1RenderTarget CreateLinearGradientBrush (D2d1. h)
description: Crea un objeto ID2D1LinearGradientBrush para dibujar áreas con un degradado lineal.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Métodos de CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690162"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a><span data-ttu-id="4402c-104">ID2D1RenderTarget:: CreateLinearGradientBrush (métodos)</span><span class="sxs-lookup"><span data-stu-id="4402c-104">ID2D1RenderTarget::CreateLinearGradientBrush methods</span></span>

<span data-ttu-id="4402c-105">Crea un objeto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para dibujar áreas con un degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="4402c-105">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) object for painting areas with a linear gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4402c-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="4402c-106">Overload list</span></span>



| <span data-ttu-id="4402c-107">Método</span><span class="sxs-lookup"><span data-stu-id="4402c-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="4402c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4402c-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4402c-109">[**CreateLinearGradientBrush (D2D1 \_ \_ \_ propiedades de pincel de degradado lineal \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4402c-109">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>                            | <span data-ttu-id="4402c-110">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados, no tiene ninguna transformación y tiene una opacidad base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="4402c-110">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="4402c-111">[**CreateLinearGradientBrush (D2D1 \_ \_ propiedades de \_ pincel de degradado lineal \_&, \_ propiedades del pincel de D2D1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4402c-111">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>   | <span data-ttu-id="4402c-112">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas.</span><span class="sxs-lookup"><span data-stu-id="4402c-112">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="4402c-113">[**CreateLinearGradientBrush ( \_ \_ \_ propiedades del pincel de degradado lineal \_ de D2D1 \* , \_ propiedades del pincel de D2D1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4402c-113">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span> | <span data-ttu-id="4402c-114">Crea un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contiene los delimitadores de degradado especificados y tiene la transformación y la opacidad base especificadas.</span><span class="sxs-lookup"><span data-stu-id="4402c-114">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="4402c-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4402c-115">Examples</span></span>

<span data-ttu-id="4402c-116">Para ver un ejemplo en el que se muestra cómo crear una colección de delimitadores de degradado y cómo usarla para definir un degradado lineal, vea [Cómo crear un pincel de degradado lineal](how-to-create-a-linear-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="4402c-116">For an example showing how to create a gradient stop collection and use it to define a linear gradient, see [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4402c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4402c-117">Requirements</span></span>



| <span data-ttu-id="4402c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4402c-118">Requirement</span></span> | <span data-ttu-id="4402c-119">Value</span><span class="sxs-lookup"><span data-stu-id="4402c-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4402c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4402c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4402c-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="4402c-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="4402c-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4402c-122">Library</span></span><br/> | <dl> <span data-ttu-id="4402c-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4402c-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="4402c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4402c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4402c-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4402c-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4402c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4402c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4402c-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="4402c-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="4402c-128">**CreateGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="4402c-128">**CreateGradientStopCollection**</span></span>](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[<span data-ttu-id="4402c-129">**ID2D1GradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="4402c-129">**ID2D1GradientStopCollection**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[<span data-ttu-id="4402c-130">**ID2D1LinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="4402c-130">**ID2D1LinearGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[<span data-ttu-id="4402c-131">**ID2D1RadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="4402c-131">**ID2D1RadialGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[<span data-ttu-id="4402c-132">Cómo crear un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="4402c-132">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="4402c-133">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="4402c-133">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="4402c-134">�</span><span class="sxs-lookup"><span data-stu-id="4402c-134">�</span></span>

<span data-ttu-id="4402c-135">�</span><span class="sxs-lookup"><span data-stu-id="4402c-135">�</span></span>
