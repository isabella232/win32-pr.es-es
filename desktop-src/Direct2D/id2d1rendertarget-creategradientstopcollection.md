---
title: Métodos de ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1. h)
description: Crea un ID2D1GradientStopCollection a partir de la matriz especificada de \_ estructuras de detención de degradado de D2D1 \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Métodos de CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4a298414d1a84b03d81c80e308113d8731369040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690164"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="e6c91-104">ID2D1RenderTarget:: CreateGradientStopCollection (métodos)</span><span class="sxs-lookup"><span data-stu-id="e6c91-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="e6c91-105">Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de la matriz especificada de estructuras de [**\_ \_ detención de degradado de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="e6c91-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e6c91-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="e6c91-106">Overload list</span></span>



| <span data-ttu-id="e6c91-107">Método</span><span class="sxs-lookup"><span data-stu-id="e6c91-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="e6c91-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6c91-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c91-109">[**CreateGradientStopCollection ( \_ detención de degradado \_ de D2D1 \* , gamma de D2D1 \_ , \_ \_ modo de extensión de D2D1, ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e6c91-109">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span> | <span data-ttu-id="e6c91-110">Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de los delimitadores de degradado, gamma de interpolación de color y modo de extensión especificados.</span><span class="sxs-lookup"><span data-stu-id="e6c91-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| <span data-ttu-id="e6c91-111">[**CreateGradientStopCollection ( \_ \_ detención de degradado de D2D1 \* , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e6c91-111">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span>                                                            | <span data-ttu-id="e6c91-112">Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de los delimitadores de degradado especificados que utiliza la gamma de interpolación de color gamma de [**D2D1 \_ \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) y el modo de extensión de la abrazadera.</span><span class="sxs-lookup"><span data-stu-id="e6c91-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="e6c91-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e6c91-113">Examples</span></span>

<span data-ttu-id="e6c91-114">En el ejemplo siguiente se crea una matriz de delimitadores de degradado y, a continuación, se usan para crear un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="e6c91-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="e6c91-115">En el siguiente ejemplo de código se usa [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para crear un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="e6c91-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="e6c91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6c91-116">Requirements</span></span>



| <span data-ttu-id="e6c91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c91-117">Requirement</span></span> | <span data-ttu-id="e6c91-118">Value</span><span class="sxs-lookup"><span data-stu-id="e6c91-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c91-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6c91-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e6c91-120"><dt>D2d1 \_ 1. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c91-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="e6c91-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6c91-121">Library</span></span><br/> | <dl> <span data-ttu-id="e6c91-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6c91-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e6c91-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6c91-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6c91-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c91-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e6c91-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6c91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c91-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e6c91-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="e6c91-127">**D2D1 delimitador de \_ degradado \_**</span><span class="sxs-lookup"><span data-stu-id="e6c91-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="e6c91-128">Cómo crear un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="e6c91-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="e6c91-129">Cómo crear un pincel de degradado radial</span><span class="sxs-lookup"><span data-stu-id="e6c91-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="e6c91-130">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="e6c91-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>
