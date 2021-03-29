---
title: Información general sobre interoperabilidad de Direct2D y GDI
description: Describe cómo usar Direct2D y GDI juntos.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interoperación de GDI
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- Direct3D, interoperabilidad
- Direct3D, interoperación de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793396"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="f01a6-111">Información general sobre interoperabilidad de Direct2D y GDI</span><span class="sxs-lookup"><span data-stu-id="f01a6-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="f01a6-112">En este tema se describe cómo usar Direct2D y [GDI](/windows/desktop/gdi/windows-gdi) juntos.</span><span class="sxs-lookup"><span data-stu-id="f01a6-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="f01a6-113">Hay dos maneras de combinar Direct2D con GDI: puede escribir contenido GDI en un destino de representación compatible con GDI de Direct2D o puede escribir contenido de Direct2D en un [contexto de dispositivo GDI (DC)](/windows/desktop/gdi/device-contexts).</span><span class="sxs-lookup"><span data-stu-id="f01a6-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="f01a6-114">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f01a6-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f01a6-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f01a6-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="f01a6-116">Dibujar contenido de Direct2D en un contexto de dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="f01a6-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="f01a6-117">ID2D1DCRenderTargets, transformaciones de GDI y compilaciones de idiomas de derecha a izquierda de Windows</span><span class="sxs-lookup"><span data-stu-id="f01a6-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="f01a6-118">Dibujar contenido GDI en un destino de representación de GDI-Compatible de Direct2D</span><span class="sxs-lookup"><span data-stu-id="f01a6-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="f01a6-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f01a6-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="f01a6-120">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f01a6-120">Prerequisites</span></span>

<span data-ttu-id="f01a6-121">En esta información general se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f01a6-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="f01a6-122">Para ver un tutorial, consulte la guía de [Inicio rápido de Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="f01a6-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="f01a6-123">También se supone que está familiarizado con las operaciones de dibujo de GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="f01a6-124">Dibujar contenido de Direct2D en un contexto de dispositivo GDI</span><span class="sxs-lookup"><span data-stu-id="f01a6-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="f01a6-125">Para dibujar contenido de Direct2D en un controlador de dominio de GDI, se usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="f01a6-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="f01a6-126">Para crear un destino de representación de DC, se usa el método [**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="f01a6-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="f01a6-127">Este método toma dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="f01a6-127">This method takes two parameters.</span></span>

<span data-ttu-id="f01a6-128">El primer parámetro, una estructura de propiedades de destino de representación de D2D1, especifica la representación, la comunicación remota, el PPP, el formato de píxel y la información de uso. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)</span><span class="sxs-lookup"><span data-stu-id="f01a6-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="f01a6-129">Para habilitar el destino de representación del controlador de dominio para que funcione con GDI, establezca el formato de DXGI en el [formato de dxgi \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) y el modo alfa en [**D2D1 de \_ \_ modo alfa \_ premultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o en **\_ \_ modo alfa \_ de D2D1**.</span><span class="sxs-lookup"><span data-stu-id="f01a6-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="f01a6-130">El segundo parámetro es la dirección del puntero que recibe la referencia de destino de representación del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f01a6-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="f01a6-131">En el código siguiente se crea un destino de representación de DC.</span><span class="sxs-lookup"><span data-stu-id="f01a6-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="f01a6-132">En el código anterior, *m \_ pD2DFactory* es un puntero a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)y *m \_ pDCRT* es un puntero a un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="f01a6-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="f01a6-133">Antes de poder representar con el destino de representación del controlador de dominio, debe usar su método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) para asociarlo con un controlador de dominio de GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="f01a6-134">Esto se hace cada vez que se usa un controlador de dominio diferente o el tamaño del área que se desea dibujar en los cambios.</span><span class="sxs-lookup"><span data-stu-id="f01a6-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="f01a6-135">El método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) toma dos parámetros, *HDC* y *pSubRect*.</span><span class="sxs-lookup"><span data-stu-id="f01a6-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="f01a6-136">El parámetro *HDC* proporciona un identificador para el contexto de dispositivo que recibe la salida del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f01a6-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="f01a6-137">El parámetro *pSubRect* es un rectángulo que describe la parte del contexto del dispositivo en el que se representa el contenido.</span><span class="sxs-lookup"><span data-stu-id="f01a6-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="f01a6-138">El destino de representación de DC actualiza su tamaño para que coincida con el área de contexto de dispositivo que describe *pSubRect*, en caso de que cambie el tamaño.</span><span class="sxs-lookup"><span data-stu-id="f01a6-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="f01a6-139">El código siguiente enlaza un controlador de dominio a un destino de representación de DC.</span><span class="sxs-lookup"><span data-stu-id="f01a6-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f01a6-140">C++</span><span class="sxs-lookup"><span data-stu-id="f01a6-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f01a6-141">Después de asociar el destino de representación del controlador de dominio a un controlador de dominio, puede usarlo para dibujar.</span><span class="sxs-lookup"><span data-stu-id="f01a6-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="f01a6-142">El código siguiente dibuja contenido de Direct2D y GDI mediante un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f01a6-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="f01a6-143">Este código genera salidas como se muestra en la siguiente ilustración (se han agregado llamadas para resaltar la diferencia entre la representación de Direct2D y GDI).</span><span class="sxs-lookup"><span data-stu-id="f01a6-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![Ilustración de dos gráficos circulares representados con direct2d y GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="f01a6-145">ID2D1DCRenderTargets, transformaciones de GDI y compilaciones de idiomas de derecha a izquierda de Windows</span><span class="sxs-lookup"><span data-stu-id="f01a6-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="f01a6-146">Cuando se usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), representa el contenido de Direct2D en un mapa de bits interno y, a continuación, representa el mapa de bits en el controlador de dominio con GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="f01a6-147">Es posible que GDI aplique una transformación GDI (a través del método [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) u otro efecto al mismo controlador de dominio que usa el destino de representación, en cuyo caso GDI transforma el mapa de bits generado por Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f01a6-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="f01a6-148">El uso de una transformación GDI para transformar el contenido de Direct2D tiene la posibilidad de degradar la calidad visual de la salida, ya que se está transformando un mapa de bits para el que ya se han calculado el posicionamiento antialias y subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="f01a6-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="f01a6-149">Por ejemplo, supongamos que usa el destino de representación para dibujar una escena que contiene geometrías y texto con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="f01a6-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="f01a6-150">Si usa una transformación de GDI para aplicar una transformación de escala al DC y escala la escena para que sea 10 veces más grande, verá los bordes escalonados y en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f01a6-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="f01a6-151">(Si, sin embargo, ha aplicado una transformación similar mediante Direct2D, la calidad visual de la escena no se degradará).</span><span class="sxs-lookup"><span data-stu-id="f01a6-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="f01a6-152">En algunos casos, podría no ser obvio que GDI está realizando un procesamiento adicional que podría degradar la calidad del contenido de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f01a6-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="f01a6-153">Por ejemplo, en una compilación de derecha a izquierda (RTL) de Windows, el contenido representado por un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) podría invertirse horizontalmente cuando GDI lo copia en su destino.</span><span class="sxs-lookup"><span data-stu-id="f01a6-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="f01a6-154">El hecho de que el contenido se invierta realmente depende de la configuración actual del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f01a6-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="f01a6-155">En función del tipo de contenido que se esté representando, puede que desee evitar la inversión.</span><span class="sxs-lookup"><span data-stu-id="f01a6-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="f01a6-156">Si el contenido de Direct2D incluye texto ClearType, esta inversión disminuirá la calidad del texto.</span><span class="sxs-lookup"><span data-stu-id="f01a6-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="f01a6-157">Puede controlar el comportamiento de representación RTL mediante la función GDI de [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) .</span><span class="sxs-lookup"><span data-stu-id="f01a6-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="f01a6-158">Para evitar la creación de reflejo, llame a la función GDI de **SetLayout** y especifique **layout \_ BITMAPORIENTATIONPRESERVED** como el único valor para el segundo parámetro (no lo combine con el **diseño \_ RTL**), como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f01a6-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="f01a6-159">Dibujar contenido GDI en un destino de representación de GDI-Compatible de Direct2D</span><span class="sxs-lookup"><span data-stu-id="f01a6-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="f01a6-160">En la sección anterior se describe cómo escribir contenido de Direct2D en un controlador de dominio de GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="f01a6-161">También puede escribir contenido GDI en un destino de representación compatible con GDI de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f01a6-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="f01a6-162">Este enfoque es útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de representar con GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="f01a6-163">Para representar el contenido GDI en un destino de representación compatible con GDI de Direct2D, use un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que proporciona acceso a un contexto de dispositivo que puede aceptar llamadas a Draw GDI.</span><span class="sxs-lookup"><span data-stu-id="f01a6-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="f01a6-164">A diferencia de otras interfaces, no se crea directamente un objeto **ID2D1GdiInteropRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="f01a6-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="f01a6-165">En su lugar, use el método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de una instancia de destino de representación existente.</span><span class="sxs-lookup"><span data-stu-id="f01a6-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="f01a6-166">El código siguiente muestra cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="f01a6-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="f01a6-167">En el código anterior, *m \_ pD2DFactory* es un puntero a un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)y *m \_ pGDIRT* es un puntero a un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="f01a6-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="f01a6-168">Tenga en cuenta que la marca de [**\_ uso de \_ \_ \_ GDI \_ compatible con el destino de representación D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) se especifica al crear el destino de representación compatible con GDI de HWND.</span><span class="sxs-lookup"><span data-stu-id="f01a6-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="f01a6-169">Si se requiere un formato de píxel, use el [formato de DXGI \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f01a6-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="f01a6-170">Si se requiere un modo alfa, use el modo alfa [**D2D1 \_ \_ \_ premultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o el **\_ \_ modo \_ alfa D2D1**.</span><span class="sxs-lookup"><span data-stu-id="f01a6-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="f01a6-171">Tenga en cuenta que el método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) siempre se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f01a6-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="f01a6-172">Para probar si los métodos de la interfaz [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funcionarán para un destino de representación determinado, cree una propiedad de destino de representación de D2D1 que especifique la compatibilidad de GDI y el formato de píxel adecuado y, a continuación, llame al método [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) del destino de representación para ver si el destino de representación es compatible con GDI. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)</span><span class="sxs-lookup"><span data-stu-id="f01a6-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="f01a6-173">En el ejemplo siguiente se muestra cómo dibujar un gráfico circular (contenido GDI) en el destino de representación compatible con GDI de HWND.</span><span class="sxs-lookup"><span data-stu-id="f01a6-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="f01a6-174">El código genera gráficos como se muestra en la siguiente ilustración con llamadas para resaltar la diferencia de calidad de representación.</span><span class="sxs-lookup"><span data-stu-id="f01a6-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="f01a6-175">El gráfico circular derecho (contenido de GDI) tiene una calidad de representación inferior que el gráfico circular izquierdo (contenido de Direct2D).</span><span class="sxs-lookup"><span data-stu-id="f01a6-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="f01a6-176">Esto se debe a que Direct2D es capaz de representar con suavizado de contorno</span><span class="sxs-lookup"><span data-stu-id="f01a6-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![Ilustración de dos gráficos circulares representados en un destino de representación compatible con GDI de direct2d](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="f01a6-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f01a6-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01a6-179">**ID2D1Factory::CreateDCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="f01a6-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="f01a6-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="f01a6-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="f01a6-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="f01a6-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="f01a6-182">**\_Propiedades de \_ destino de representación de D2D1 \_**</span><span class="sxs-lookup"><span data-stu-id="f01a6-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="f01a6-183">Contextos de dispositivos GDI</span><span class="sxs-lookup"><span data-stu-id="f01a6-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="f01a6-184">SDK DE GDI</span><span class="sxs-lookup"><span data-stu-id="f01a6-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 