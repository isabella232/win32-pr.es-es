---
title: Métodos ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1.h)
description: Crea una clase ID2D1GradientStopCollection a partir de la matriz especificada de estructuras GRADIENT STOP de D2D1. \_ \_
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Métodos CreateGradientStopCollection de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549420"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="75c37-104">Métodos ID2D1RenderTarget::CreateGradientStopCollection</span><span class="sxs-lookup"><span data-stu-id="75c37-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="75c37-105">Crea una [**clase ID2D1GradientStopCollection a partir**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) de la matriz especificada de estructuras GRADIENT STOP de [**D2D1. \_ \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)</span><span class="sxs-lookup"><span data-stu-id="75c37-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="75c37-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="75c37-106">Overload list</span></span>



| <span data-ttu-id="75c37-107">Método</span><span class="sxs-lookup"><span data-stu-id="75c37-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="75c37-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="75c37-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75c37-109">**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,D2D1 \_ GAMMA,D2D1 \_ EXTEND \_ MODE,ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="75c37-109">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | <span data-ttu-id="75c37-110">Crea una [**clase ID2D1GradientStopCollection a**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) partir de los delimitadores de degradado, gamma de interpolación de color y modo de extensión especificados.</span><span class="sxs-lookup"><span data-stu-id="75c37-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| [<span data-ttu-id="75c37-111">**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="75c37-111">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | <span data-ttu-id="75c37-112">Crea una [**clase ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de los delimitadores de degradado especificados que usa el gamma de interpolación de color [**gamma \_ \_ 2 \_ 2 de D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) y el modo de extensión de la fijación.</span><span class="sxs-lookup"><span data-stu-id="75c37-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="75c37-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75c37-113">Examples</span></span>

<span data-ttu-id="75c37-114">En el ejemplo siguiente se crea una matriz de delimitadores de degradado y, a continuación, se usan para crear un [**elemento ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="75c37-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


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



<span data-ttu-id="75c37-115">En el ejemplo de código siguiente se [**usa ID2D1GradientStopCollection para**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) crear un [**objeto ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)</span><span class="sxs-lookup"><span data-stu-id="75c37-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="75c37-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c37-116">Requirements</span></span>



| <span data-ttu-id="75c37-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c37-117">Requirement</span></span> | <span data-ttu-id="75c37-118">Value</span><span class="sxs-lookup"><span data-stu-id="75c37-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c37-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75c37-119">Header</span></span><br/>  | <dl> <span data-ttu-id="75c37-120"><dt>D2d1 \_ 1.h (incluir D2d1.h)</dt></span><span class="sxs-lookup"><span data-stu-id="75c37-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="75c37-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75c37-121">Library</span></span><br/> | <dl> <span data-ttu-id="75c37-122"><dt>D2d1.lib</dt></span><span class="sxs-lookup"><span data-stu-id="75c37-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="75c37-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75c37-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="75c37-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c37-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="75c37-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75c37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c37-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="75c37-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="75c37-127">**D2D1 \_ GRADIENT \_ STOP**</span><span class="sxs-lookup"><span data-stu-id="75c37-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="75c37-128">Cómo crear un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="75c37-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="75c37-129">Cómo crear un pincel de degradado radial</span><span class="sxs-lookup"><span data-stu-id="75c37-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="75c37-130">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="75c37-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>