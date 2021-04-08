---
title: Información general sobre desenfoque de DWM
description: Uno de los efectos de Administrador de ventanas de escritorio de firma (DWM) es un área no cliente translúcida y desenfocada. Las API de DWM permiten a las aplicaciones aplicar estos efectos en el área cliente de las ventanas de nivel superior.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Administrador de ventanas de escritorio (DWM), efecto de desenfoque
- DWM (Administrador de ventanas de escritorio), efecto de desenfoque
- efecto de desenfoque
- efecto traslúcido
- efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), efecto translúcido
- DWM (Administrador de ventanas de escritorio), efecto translúcido
- Administrador de ventanas de escritorio (DWM), efecto de cristal transparente
- DWM (Administrador de ventanas de escritorio), efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), extender el marco de ventana en el área de cliente
- DWM (Administrador de ventanas de escritorio), extender el marco de ventana en el área de cliente
- extender el marco de ventana en el área de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078267"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="50b09-116">Información general sobre desenfoque de DWM</span><span class="sxs-lookup"><span data-stu-id="50b09-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="50b09-117">Uno de los efectos de Administrador de ventanas de escritorio de firma (DWM) es un área no cliente translúcida y desenfocada.</span><span class="sxs-lookup"><span data-stu-id="50b09-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="50b09-118">Las API de DWM permiten a las aplicaciones aplicar estos efectos en el área cliente de las ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="50b09-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="50b09-119">Windows Vista Home Basic Edition no admite el efecto de cristal transparente.</span><span class="sxs-lookup"><span data-stu-id="50b09-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="50b09-120">Las áreas que normalmente se representarían con el efecto de cristal transparente en otras ediciones de Windows se representan como opacas.</span><span class="sxs-lookup"><span data-stu-id="50b09-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="50b09-121">A partir de Windows 8, llamar a esta función no produce el efecto de desenfoque debido a un cambio de estilo en la forma en que se representan las ventanas.</span><span class="sxs-lookup"><span data-stu-id="50b09-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="50b09-122">En este tema se describen los siguientes escenarios de desenfoque de cliente que el DWM habilita.</span><span class="sxs-lookup"><span data-stu-id="50b09-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="50b09-123">Agregar el desenfoque a una región específica del área cliente</span><span class="sxs-lookup"><span data-stu-id="50b09-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="50b09-124">Extender el marco de ventana en el área cliente</span><span class="sxs-lookup"><span data-stu-id="50b09-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="50b09-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50b09-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="50b09-126">Agregar el desenfoque a una región específica del área cliente</span><span class="sxs-lookup"><span data-stu-id="50b09-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="50b09-127">Una aplicación puede aplicar el efecto de desenfoque detrás de toda la región cliente de la ventana o de una subregión específica.</span><span class="sxs-lookup"><span data-stu-id="50b09-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="50b09-128">Esto permite a las aplicaciones agregar barras de búsqueda y trazados de estilo que se separan visualmente del resto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b09-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="50b09-129">La API usada en este escenario es la función [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , que hace uso de las [**constantes de desenfoque de DWM**](dwm-bb-constants.md) y de la estructura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .</span><span class="sxs-lookup"><span data-stu-id="50b09-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="50b09-130">En la función de ejemplo siguiente, `EnableBlurBehind` , se muestra cómo aplicar el efecto de desenfoque detrás a toda la ventana.</span><span class="sxs-lookup"><span data-stu-id="50b09-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="50b09-131">Tenga en cuenta que **null** se especifica en el parámetro *hRgnBlur* .</span><span class="sxs-lookup"><span data-stu-id="50b09-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="50b09-132">Esto indica al DWM que aplique el desenfoque detrás de la ventana completa.</span><span class="sxs-lookup"><span data-stu-id="50b09-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="50b09-133">En la imagen siguiente se muestra el efecto de desenfoque aplicado a toda la ventana.</span><span class="sxs-lookup"><span data-stu-id="50b09-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![efecto de desenfoque aplicado a una ventana](images/dwm-blurbehindwindow.png)

<span data-ttu-id="50b09-135">Para aplicar el desenfoque detrás de una subregión, aplique un identificador de región válido (HRGN) al miembro **hRgnBlur** de la estructura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) y agregue la marca **DWM \_ BB \_ BLURREGION** al miembro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="50b09-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="50b09-136">Cuando se aplica el efecto de desenfoque a una subregión de la ventana, se usa el canal alfa de la ventana para el área no desenfocada.</span><span class="sxs-lookup"><span data-stu-id="50b09-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="50b09-137">Esto puede producir una transparencia inesperada en la región no desenfocada de una ventana.</span><span class="sxs-lookup"><span data-stu-id="50b09-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="50b09-138">Por lo tanto, tenga cuidado al aplicar un efecto de desenfoque a una subregión.</span><span class="sxs-lookup"><span data-stu-id="50b09-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="50b09-139">Extender el marco de ventana en el área cliente</span><span class="sxs-lookup"><span data-stu-id="50b09-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="50b09-140">Una aplicación puede extender el desenfoque del marco de la ventana en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="50b09-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="50b09-141">Esto resulta útil cuando se aplica el efecto de desenfoque detrás de una ventana con una barra de herramientas acoplada o se separan visualmente los controles del resto de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b09-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="50b09-142">Esta funcionalidad se expone mediante la función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="50b09-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="50b09-143">Para habilitar el desenfoque mediante [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use la estructura [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) para indicar el grado de ampliación en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="50b09-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="50b09-144">La siguiente función de ejemplo, `ExtendIntoClientBottom` , alterna la extensión de desenfoque en la parte inferior del marco no cliente en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="50b09-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="50b09-145">En la imagen siguiente se muestra el efecto de desenfoque que se extiende en la parte inferior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="50b09-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![imagen que muestra el efecto de desenfoque subyacente extendido en la parte inferior de un área cliente](images/dwm-extendedbottom.png)

<span data-ttu-id="50b09-147">También está disponible a través del método [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) es el efecto "hoja de cristal", donde el efecto de desenfoque se aplica a toda la superficie de la ventana sin un borde de ventana visible.</span><span class="sxs-lookup"><span data-stu-id="50b09-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="50b09-148">En el ejemplo siguiente se muestra este efecto en el que el área cliente se representa sin un borde de ventana.</span><span class="sxs-lookup"><span data-stu-id="50b09-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="50b09-149">En la imagen siguiente se ilustra el desenfoque en el estilo de ventana "hoja de cristal".</span><span class="sxs-lookup"><span data-stu-id="50b09-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![imagen que muestra el efecto de desenfoque en el estilo de ventana "hoja de cristal"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="50b09-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50b09-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50b09-152">[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)</span><span class="sxs-lookup"><span data-stu-id="50b09-152">[Desktop Window Manager Overview](dwm-overview.md)</span></span>
</dt> <dt>

[<span data-ttu-id="50b09-153">Habilitar y controlar la composición de DWM</span><span class="sxs-lookup"><span data-stu-id="50b09-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="50b09-154">Consideraciones de rendimiento y prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="50b09-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 