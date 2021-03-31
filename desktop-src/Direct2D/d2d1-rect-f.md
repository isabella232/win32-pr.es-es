---
title: D2D1_RECT_F (D2DBaseTypes. h)
description: Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior). | D2D1_RECT_F (D2DBaseTypes. h)
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083628"
---
# <a name="d2d1_rect_f"></a><span data-ttu-id="2b7b6-105">D2D1 \_ Rect \_ F</span><span class="sxs-lookup"><span data-stu-id="2b7b6-105">D2D1\_RECT\_F</span></span>

<span data-ttu-id="2b7b6-106">Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).</span><span class="sxs-lookup"><span data-stu-id="2b7b6-106">Represents a rectangle defined by the coordinates of the upper-left corner (left, top) and the coordinates of the lower-right corner (right, bottom).</span></span>


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a><span data-ttu-id="2b7b6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b7b6-107">Remarks</span></span>

<span data-ttu-id="2b7b6-108">**D2D1 \_ RECT \_ f** es un nombre nuevo para el struct [**D2D \_ Rect \_ f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) ya definido.</span><span class="sxs-lookup"><span data-stu-id="2b7b6-108">**D2D1\_RECT\_F** is a new name for the already defined [**D2D\_RECT\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) struct.</span></span>

## <a name="examples"></a><span data-ttu-id="2b7b6-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b7b6-109">Examples</span></span>

<span data-ttu-id="2b7b6-110">En el ejemplo siguiente se usa un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para dibujar y rellenar varios rectángulos.</span><span class="sxs-lookup"><span data-stu-id="2b7b6-110">The following example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw and fill several rectangles.</span></span> <span data-ttu-id="2b7b6-111">Este ejemplo genera un resultado como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="2b7b6-111">This example produces output as shown in the following illustration.</span></span>

![Ilustración de dos rectángulos en un fondo de cuadrícula](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="2b7b6-113">Para ver un tutorial relacionado, consulte [creación de una aplicación de Direct2D simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="2b7b6-113">For a related tutorial, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7b6-114">Requirements</span></span>



| <span data-ttu-id="2b7b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7b6-115">Requirement</span></span> | <span data-ttu-id="2b7b6-116">Value</span><span class="sxs-lookup"><span data-stu-id="2b7b6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7b6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7b6-118">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="2b7b6-118">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2b7b6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7b6-120">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b7b6-120">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2b7b6-121">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7b6-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2b7b6-122">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="2b7b6-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2b7b6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b7b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b7b6-124"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b7b6-124"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2b7b6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b7b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7b6-126">**D2D \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="2b7b6-126">**D2D\_RECT\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[<span data-ttu-id="2b7b6-127">Crear una aplicación de Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="2b7b6-127">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

