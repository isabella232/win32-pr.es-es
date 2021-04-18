---
title: ID2D1RenderTarget borrar métodos
description: Borra el área de dibujo con el color especificado.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Borrar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660910"
---
# <a name="id2d1rendertargetclear-methods"></a><span data-ttu-id="bdfbd-104">ID2D1RenderTarget:: CLEAR (métodos)</span><span class="sxs-lookup"><span data-stu-id="bdfbd-104">ID2D1RenderTarget::Clear methods</span></span>

<span data-ttu-id="bdfbd-105">Borra el área de dibujo con el color especificado.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-105">Clears the drawing area to the specified color.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bdfbd-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="bdfbd-106">Overload list</span></span>



| <span data-ttu-id="bdfbd-107">Método</span><span class="sxs-lookup"><span data-stu-id="bdfbd-107">Method</span></span>                                                                 | <span data-ttu-id="bdfbd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdfbd-108">Description</span></span>                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="bdfbd-109">[**Borrar (D2D1 de \_ color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="bdfbd-109">[**Clear(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span></span> | <span data-ttu-id="bdfbd-110">Borra el área de dibujo con el color especificado.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-110">Clears the drawing area to the specified color.</span></span> <br/> |
| <span data-ttu-id="bdfbd-111">[**Clear (D2D1 de \_ color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="bdfbd-111">[**Clear(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span></span>  | <span data-ttu-id="bdfbd-112">Borra el área de dibujo con el color especificado.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-112">Clears the drawing area to the specified color.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="bdfbd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdfbd-113">Remarks</span></span>

<span data-ttu-id="bdfbd-114">Direct2D interpreta *clearColor* como alfa recto (no multiplicado previamente).</span><span class="sxs-lookup"><span data-stu-id="bdfbd-114">Direct2D interprets the *clearColor* as straight alpha (not premultiplied).</span></span> <span data-ttu-id="bdfbd-115">Si el modo alfa del destino de representación es el [**\_ \_ modo \_ alfa D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), el canal alfa de *clearColor* se omite y se reemplaza con 1,0 f (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="bdfbd-115">If the render target's alpha mode is [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the alpha channel of *clearColor* is ignored and replaced with 1.0f (fully opaque).</span></span>

<span data-ttu-id="bdfbd-116">Si el destino de representación tiene un clip activo (especificado por [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), el comando borrar solo se aplica al área dentro de la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-116">If the render target has an active clip (specified by [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), the clear command is only applied to the area within the clip region.</span></span>

## <a name="examples"></a><span data-ttu-id="bdfbd-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bdfbd-117">Examples</span></span>

<span data-ttu-id="bdfbd-118">En el ejemplo siguiente se usa el método **Clear** para crear un fondo blanco antes de representar otro contenido.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-118">The following example uses the **Clear** method to create a white background before rendering other content.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="bdfbd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdfbd-119">Requirements</span></span>



| <span data-ttu-id="bdfbd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdfbd-120">Requirement</span></span> | <span data-ttu-id="bdfbd-121">Value</span><span class="sxs-lookup"><span data-stu-id="bdfbd-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfbd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdfbd-122">Library</span></span><br/> | <dl> <span data-ttu-id="bdfbd-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdfbd-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bdfbd-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bdfbd-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdfbd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdfbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfbd-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="bdfbd-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

