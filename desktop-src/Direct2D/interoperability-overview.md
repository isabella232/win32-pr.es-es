---
title: Información general sobre interoperabilidad
description: Resume las diferentes tecnologías que puede usar con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interoperación de GDI
- Direct2D, interoperación GDI+
- Direct2D, interoperabilidad
- Interoperación de Direct2D, DirectWrite
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- interoperabilidad, GDI+
- Interoperabilidad de DirectWrite
- interoperabilidad, DirectWrite
- Windows Imaging Component (WIC)
- WIC (componente de Windows Imaging)
- interoperabilidad, componente de creación de imágenes de Windows (WIC)
- Direct2D, interoperación de WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420887"
---
# <a name="interoperability-overview"></a><span data-ttu-id="4d798-119">Información general sobre interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="4d798-119">Interoperability Overview</span></span>

<span data-ttu-id="4d798-120">Una de las características clave de Direct2d es la habilitación de la interoperabilidad entre Direct2D y otras plataformas de representación para que los desarrolladores puedan usar los puntos fuertes específicos de cada plataforma sin tener que estar en peligro eligiendo una plataforma para todas las necesidades.</span><span class="sxs-lookup"><span data-stu-id="4d798-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="4d798-121">En este tema se resumen las distintas plataformas con las que Direct2D es interoperable.</span><span class="sxs-lookup"><span data-stu-id="4d798-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="4d798-122">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="4d798-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="4d798-123">Interoperabilidad con GDI</span><span class="sxs-lookup"><span data-stu-id="4d798-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="4d798-124">Interoperabilidad con GDI+</span><span class="sxs-lookup"><span data-stu-id="4d798-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="4d798-125">Interoperabilidad de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4d798-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="4d798-126">Interoperabilidad de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="4d798-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="4d798-127">Interoperabilidad de Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="4d798-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="4d798-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d798-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="4d798-129">En el diagrama siguiente se resumen las distintas plataformas con las que Direct2D es interoperable y se enumeran algunos métodos e interfaces que proporcionan interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="4d798-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![diagrama de plataformas con el que direct2d interopera, incluidos Direct3D 10,1, directwrite, WIC, GDI+ y GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="4d798-131">Interoperabilidad con GDI</span><span class="sxs-lookup"><span data-stu-id="4d798-131">GDI Interoperability</span></span>

<span data-ttu-id="4d798-132">Direct2D habilita la interoperabilidad bidireccional con GDI.</span><span class="sxs-lookup"><span data-stu-id="4d798-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="4d798-133">Puede usar un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en un [contexto de dispositivo](/windows/desktop/gdi/device-contexts) GDI (DC) o puede usar [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obtener una representación de DC de un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4d798-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="4d798-134">Para obtener más información y ejemplos, vea [información general sobre la interoperabilidad de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4d798-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="4d798-135">Interoperabilidad con GDI+</span><span class="sxs-lookup"><span data-stu-id="4d798-135">GDI+ Interoperability</span></span>

<span data-ttu-id="4d798-136">Puede usar GDI+ con Direct2D de la misma manera que GDI.</span><span class="sxs-lookup"><span data-stu-id="4d798-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="4d798-137">Puede usar un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para escribir contenido de Direct2D en el mismo DC que el contenido de GDI+.</span><span class="sxs-lookup"><span data-stu-id="4d798-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="4d798-138">Este enfoque permite empezar a agregar contenido de Direct2D a las aplicaciones que se representan principalmente mediante GDI+.</span><span class="sxs-lookup"><span data-stu-id="4d798-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="4d798-139">También puede usar un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para proporcionar acceso a un controlador de dominio de GDI que escribe mediante Direct2D y, a continuación, usar el método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para crear un objeto.</span><span class="sxs-lookup"><span data-stu-id="4d798-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="4d798-140">Este enfoque es útil para las aplicaciones que se representan principalmente con Direct2D, pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de presentar con GDI+.</span><span class="sxs-lookup"><span data-stu-id="4d798-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="4d798-141">Interoperabilidad de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4d798-141">Direct3D Interoperability</span></span>

<span data-ttu-id="4d798-142">Direct2D puede usar un destino de representación de la superficie de DXGI (creado por el método [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) para escribir en un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span><span class="sxs-lookup"><span data-stu-id="4d798-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="4d798-143">Esta acción le permite agregar las interfaces y los trabajos en segundo plano a las escenas 3D y usar el contenido de Direct2D como textura para un modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="4d798-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="4d798-144">Direct2D también puede tomar un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) y usar el método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear una representación de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="4d798-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="4d798-145">Para obtener más información y ejemplos, vea [información general sobre interoperabilidad de Direct2D y Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4d798-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="4d798-146">Interoperabilidad de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="4d798-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="4d798-147">Direct2D se integra estrechamente con DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="4d798-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="4d798-148">Direct2D facilita el procesamiento de contenido de DirectWrite proporcionando los métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)y [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="4d798-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="4d798-149">Interoperabilidad de Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="4d798-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="4d798-150">Direct2D proporciona los métodos [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)y [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular los mapas de bits de WIC.</span><span class="sxs-lookup"><span data-stu-id="4d798-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d798-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d798-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d798-152">Información general sobre interoperabilidad de Direct2D y GDI</span><span class="sxs-lookup"><span data-stu-id="4d798-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="4d798-153">Introducción a la interoperabilidad de Direct2D y Direct3D</span><span class="sxs-lookup"><span data-stu-id="4d798-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 