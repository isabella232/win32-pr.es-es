---
title: Habilitar y controlar la composición de DWM
description: Las API de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar información básica que utiliza DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Administrador de ventanas de escritorio (DWM), composición
- DWM (Administrador de ventanas de escritorio), composición
- composición
- composición de escritorio
- coloración
- representación de regiones no cliente
- Administrador de ventanas de escritorio (DWM), coloración
- DWM (Administrador de ventanas de escritorio), coloración
- Administrador de ventanas de escritorio (DWM), representación de regiones no cliente
- DWM (Administrador de ventanas de escritorio), representación de regiones no cliente
- Administrador de ventanas de escritorio (DWM), mensajería
- DWM (Administrador de ventanas de escritorio), mensajería
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903782"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="4943b-116">Habilitar y controlar la composición de DWM</span><span class="sxs-lookup"><span data-stu-id="4943b-116">Enable and control DWM composition</span></span>

<span data-ttu-id="4943b-117">Las API de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar información básica que utiliza DWM.</span><span class="sxs-lookup"><span data-stu-id="4943b-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="4943b-118">Estas API permiten consultar y cambiar el estado de composición.</span><span class="sxs-lookup"><span data-stu-id="4943b-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="4943b-119">Además, puede establecer y consultar la Directiva de representación para los distintos atributos de la ventana de DWM.</span><span class="sxs-lookup"><span data-stu-id="4943b-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="4943b-120">Recuperar información de color</span><span class="sxs-lookup"><span data-stu-id="4943b-120">Retrieving colorization information</span></span>

<span data-ttu-id="4943b-121">El color de la región no cliente de una ventana viene determinado por el tema de color del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="4943b-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="4943b-122">El valor de coloración se proporciona a través de las API de DWM para permitir que la aplicación coincida con la interfaz de usuario del cliente con el tema de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="4943b-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="4943b-123">Para tener acceso a este valor de coloración y supervisar el cambio de color, utilice la función [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) y el mensaje [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4943b-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="4943b-124">En este ejemplo se muestra cómo controlar el mensaje de cambio de color y cómo obtener acceso al nuevo color.</span><span class="sxs-lookup"><span data-stu-id="4943b-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="4943b-125">Controlar la representación de regiones no cliente</span><span class="sxs-lookup"><span data-stu-id="4943b-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="4943b-126">Dos de los efectos visuales que DWM permite son la transparencia de la región no cliente de una ventana y los efectos de la transición.</span><span class="sxs-lookup"><span data-stu-id="4943b-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="4943b-127">Es posible que la aplicación tenga que deshabilitar o volver a habilitar estos efectos por motivos de compatibilidad o estilo.</span><span class="sxs-lookup"><span data-stu-id="4943b-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="4943b-128">Las funciones siguientes se usan para administrar el comportamiento de la transparencia y del efecto de transición.</span><span class="sxs-lookup"><span data-stu-id="4943b-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="4943b-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="4943b-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="4943b-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="4943b-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="4943b-131">Para recuperar el estado actual de representación no cliente de la ventana de una aplicación, llame a [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* establecido en [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span><span class="sxs-lookup"><span data-stu-id="4943b-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="4943b-132">Como puede ver en la documentación de [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), al pasar esa marca a **DwmGetWindowAttribute**, el valor del atributo recuperado es de tipo **bool**.</span><span class="sxs-lookup"><span data-stu-id="4943b-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="4943b-133">Las distintas marcas hacen que **DwmGetWindowAttribute** devuelva valores de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="4943b-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="4943b-134">Aquí tienes un ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="4943b-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="4943b-135">En el ejemplo siguiente se muestra cómo usar la marca [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) con **DwmGetWindowAttribute** para recuperar el rectángulo de límites de marco extendido de una ventana.</span><span class="sxs-lookup"><span data-stu-id="4943b-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="4943b-136">La documentación de esa marca nos indica que el valor del atributo recuperado es de tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="4943b-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="4943b-137">Siga el mismo patrón de programación que se mostró anteriormente al llamar a [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con marcas para los distintos atributos.</span><span class="sxs-lookup"><span data-stu-id="4943b-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="4943b-138">El tema de enumeración [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, en la fila de cada marcador, el tipo de valor al que debe pasar un puntero en el parámetro *pvAttribute* para **DwmGetWindowAttribute**.</span><span class="sxs-lookup"><span data-stu-id="4943b-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="4943b-139">El parámetro *cbAttribute* contiene el tamaño, en bytes, de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="4943b-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="4943b-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permite que la aplicación establezca la Directiva de representación de área no cliente.</span><span class="sxs-lookup"><span data-stu-id="4943b-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="4943b-141">Esa función también determina el modo en que la aplicación debe controlar los efectos de transición de DWM.</span><span class="sxs-lookup"><span data-stu-id="4943b-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="4943b-142">En el siguiente ejemplo se deshabilita la representación del área no cliente.</span><span class="sxs-lookup"><span data-stu-id="4943b-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="4943b-143">Esto hace que se deshabiliten las llamadas anteriores a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="4943b-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="4943b-144">Además de controlar la representación del área no cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) también puede controlar los efectos de transición de DWM.</span><span class="sxs-lookup"><span data-stu-id="4943b-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="4943b-145">Puede establecer el comportamiento de transición mediante **DWMWA \_ Transitions \_ FORCEDISABLED** como el parámetro *dwAttribute* .</span><span class="sxs-lookup"><span data-stu-id="4943b-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="4943b-146">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="4943b-146">Messages</span></span>

<span data-ttu-id="4943b-147">Los mensajes siguientes proporcionan la notificación de eventos de DWM.</span><span class="sxs-lookup"><span data-stu-id="4943b-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="4943b-148">Estos mensajes se pueden usar para supervisar cambios, como cambios de estado de composición y cambios de tema de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="4943b-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="4943b-149">**DWMCOLORIZATIONCOLORCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4943b-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="4943b-150">**DWMCOMPOSITIONCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4943b-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="4943b-151">**DWMNCRENDERINGCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4943b-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="4943b-152">**DWMWINDOWMAXIMIZEDCHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4943b-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="4943b-153">Deshabilitar la composición de DWM (Windows 7 y versiones anteriores)</span><span class="sxs-lookup"><span data-stu-id="4943b-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="4943b-154">La información de esta sección solo se aplica a Windows 7 y sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="4943b-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="4943b-155">Dado que DWM usa la unidad de procesamiento de gráficos (GPU) para la composición del escritorio, es posible que la aplicación tenga que deshabilitar DWM por compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="4943b-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="4943b-156">Las aplicaciones que tienen control total sobre el escritorio, como los juegos que se ejecutan en modo de pantalla completa, deben determinar si DWM está habilitado y, si es así, deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="4943b-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="4943b-157">Para ello, se necesitan dos funciones.</span><span class="sxs-lookup"><span data-stu-id="4943b-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="4943b-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="4943b-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="4943b-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="4943b-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="4943b-160">Una llamada a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *FEnable* establecido en **DWM \_ EC \_ DISABLECOMPOSITION** deshabilita la composición de DWM hasta que el proceso de llamada se ha cerrado o se ha vuelto a habilitar la composición mediante una llamada a **DwmEnableComposition** con *fEnable* establecido en **DWM \_ EC \_ ENABLECOMPOSITION**.</span><span class="sxs-lookup"><span data-stu-id="4943b-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="4943b-161">La composición DWM se reinicia automáticamente en cuanto todas las aplicaciones que tienen la composición deshabilitada se apagan o se vuelven a habilitar manualmente mediante una llamada a **DwmEnableComposition**.</span><span class="sxs-lookup"><span data-stu-id="4943b-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="4943b-162">El DWM deshabilita automáticamente la composición cuando una aplicación intenta dibujar directamente en la superficie de visualización principal.</span><span class="sxs-lookup"><span data-stu-id="4943b-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="4943b-163">La composición se deshabilitará hasta que la superficie del dispositivo principal sea publicada por esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="4943b-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
