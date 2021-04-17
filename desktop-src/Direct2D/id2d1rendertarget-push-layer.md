---
title: Métodos de ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a PopLayer.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Métodos de PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691044"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="6fbac-104">ID2D1RenderTarget::P ushLayer métodos)</span><span class="sxs-lookup"><span data-stu-id="6fbac-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="6fbac-105">Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="6fbac-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6fbac-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="6fbac-106">Overload list</span></span>



| <span data-ttu-id="6fbac-107">Método</span><span class="sxs-lookup"><span data-stu-id="6fbac-107">Method</span></span>                                                                                                                            | <span data-ttu-id="6fbac-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fbac-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbac-109">[**PushLayer ( \_ \_ parámetros de nivel D2D1&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="6fbac-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="6fbac-110">Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="6fbac-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="6fbac-111">[**PushLayer ( \_ \_ parámetros de nivel D2D1 \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="6fbac-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="6fbac-112">Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="6fbac-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6fbac-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fbac-113">Remarks</span></span>

<span data-ttu-id="6fbac-114">El método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permite a un llamador comenzar a redirigir la representación a una capa.</span><span class="sxs-lookup"><span data-stu-id="6fbac-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="6fbac-115">Todas las operaciones de representación son válidas en una capa.</span><span class="sxs-lookup"><span data-stu-id="6fbac-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="6fbac-116">La ubicación de la capa se ve afectada por el conjunto de transformación universal en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="6fbac-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="6fbac-117">Cada **PushLayer** debe tener una llamada [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) coincidente.</span><span class="sxs-lookup"><span data-stu-id="6fbac-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="6fbac-118">Si hay más llamadas a **PopLayer** que llamadas a **PushLayer** , el destino de representación se coloca en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="6fbac-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="6fbac-119">Si se llama a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) antes de que se extraigan todos los niveles pendientes, el destino de representación se coloca en un estado de error y se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6fbac-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="6fbac-120">El estado de error se puede borrar mediante una llamada a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="6fbac-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="6fbac-121">Un recurso [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) determinado solo puede estar activo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6fbac-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="6fbac-122">En otras palabras, no puede llamar a un método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y después seguir inmediatamente con otro método **PushLayer** con el mismo recurso de capa.</span><span class="sxs-lookup"><span data-stu-id="6fbac-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="6fbac-123">En su lugar, debe llamar al segundo método **PushLayer** con distintos recursos de capa.</span><span class="sxs-lookup"><span data-stu-id="6fbac-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="6fbac-124">Para obtener un ejemplo, consulte [Cómo recortar una región con capas](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="6fbac-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="6fbac-125">Este método no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6fbac-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="6fbac-126">Para determinar si una operación de dibujo (como **PushLayer**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="6fbac-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="6fbac-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6fbac-127">Examples</span></span>

<span data-ttu-id="6fbac-128">En el ejemplo siguiente se usa una capa para recortar un mapa de bits a una máscara geométrica.</span><span class="sxs-lookup"><span data-stu-id="6fbac-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="6fbac-129">Para obtener el ejemplo completo, consulte [Cómo recortar en una máscara geométrica](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="6fbac-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6fbac-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fbac-130">Requirements</span></span>



| <span data-ttu-id="6fbac-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fbac-131">Requirement</span></span> | <span data-ttu-id="6fbac-132">Value</span><span class="sxs-lookup"><span data-stu-id="6fbac-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbac-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fbac-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6fbac-134"><dt>D2d1 \_ 1. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fbac-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="6fbac-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fbac-135">Library</span></span><br/> | <dl> <span data-ttu-id="6fbac-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fbac-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6fbac-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fbac-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="6fbac-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbac-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="6fbac-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fbac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbac-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="6fbac-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="6fbac-141">Información general sobre capas</span><span class="sxs-lookup"><span data-stu-id="6fbac-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="6fbac-142">�</span><span class="sxs-lookup"><span data-stu-id="6fbac-142">�</span></span>

<span data-ttu-id="6fbac-143">�</span><span class="sxs-lookup"><span data-stu-id="6fbac-143">�</span></span>
