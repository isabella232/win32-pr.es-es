---
title: Marco de ventana personalizado mediante DWM
description: En este tema se muestra cómo usar las API de Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Administrador de ventanas de escritorio (DWM), marcos de ventana personalizados
- DWM (Administrador de ventanas de escritorio), marcos de ventana personalizados
- marcos de ventana personalizados
- quitar fotogramas estándar
- extender fotogramas de cliente
- Administrador de ventanas de escritorio (DWM), extender fotogramas de cliente
- DWM (Administrador de ventanas de escritorio), extender fotogramas de cliente
- Administrador de ventanas de escritorio (DWM), quitar fotogramas estándar
- DWM (Administrador de ventanas de escritorio), quitar fotogramas estándar
- Administrador de ventanas de escritorio (DWM), dibujar en marcos extendidos
- DWM (Administrador de ventanas de escritorio), dibujar en marcos extendidos
- dibujar en marcos extendidos
- comprobación de visitas
- Administrador de ventanas de escritorio (DWM), prueba de posicionamiento
- DWM (Administrador de ventanas de escritorio), prueba de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078337"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="64e68-118">Marco de ventana personalizado mediante DWM</span><span class="sxs-lookup"><span data-stu-id="64e68-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="64e68-119">En este tema se muestra cómo usar las API de Administrador de ventanas de escritorio (DWM) para crear marcos de ventana personalizados para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64e68-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="64e68-120">Introducción</span><span class="sxs-lookup"><span data-stu-id="64e68-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="64e68-121">Extender el marco de cliente</span><span class="sxs-lookup"><span data-stu-id="64e68-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="64e68-122">Quitar el fotograma estándar</span><span class="sxs-lookup"><span data-stu-id="64e68-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="64e68-123">Dibujar en la ventana de marco extendido</span><span class="sxs-lookup"><span data-stu-id="64e68-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="64e68-124">Habilitar la prueba de posicionamiento para el marco personalizado</span><span class="sxs-lookup"><span data-stu-id="64e68-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="64e68-125">Apéndice A: procedimiento de ventana de ejemplo</span><span class="sxs-lookup"><span data-stu-id="64e68-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="64e68-126">Apéndice B: pintar el título del título</span><span class="sxs-lookup"><span data-stu-id="64e68-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="64e68-127">Apéndice C: función HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="64e68-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="64e68-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64e68-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="64e68-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="64e68-129">Introduction</span></span>

<span data-ttu-id="64e68-130">En Windows Vista y versiones posteriores, el DWM controla la apariencia de las áreas no cliente de las ventanas de la aplicación (la barra de título, el icono, el borde de la ventana y los botones de título).</span><span class="sxs-lookup"><span data-stu-id="64e68-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="64e68-131">Con las API de DWM, puede cambiar la forma en que DWM representa el marco de una ventana.</span><span class="sxs-lookup"><span data-stu-id="64e68-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="64e68-132">Una característica de las API de DWM es la capacidad de extender el marco de aplicación en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="64e68-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="64e68-133">Esto le permite integrar un elemento de la interfaz de usuario de cliente (por ejemplo, una barra de herramientas) en el marco, de forma que la interfaz de usuario controla un lugar más destacado en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64e68-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="64e68-134">Por ejemplo, Windows Internet Explorer 7 en Windows Vista integra la barra de navegación en el marco de la ventana extendiendo la parte superior del marco, tal como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="64e68-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![barra de navegación integrada en el marco de la ventana.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="64e68-136">La capacidad de extender el marco de ventana también le permite crear fotogramas personalizados mientras mantiene la apariencia y el funcionamiento de la ventana.</span><span class="sxs-lookup"><span data-stu-id="64e68-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="64e68-137">Por ejemplo, Microsoft Office Word 2007 dibuja el botón de Office y la barra de herramientas de acceso rápido dentro del marco personalizado, a la vez que proporciona los botones estándar minimizar, maximizar y cerrar título, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="64e68-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![botón de Office y barra de herramientas de acceso rápido en Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="64e68-139">Extender el marco de cliente</span><span class="sxs-lookup"><span data-stu-id="64e68-139">Extending the Client Frame</span></span>

<span data-ttu-id="64e68-140">La función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) expone la funcionalidad para extender el marco en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="64e68-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="64e68-141">Para extender el marco, pase el identificador de la ventana de destino junto con los valores de margen de margen a **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="64e68-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="64e68-142">Los valores de bajorrelieve del margen determinan hasta qué punto se extiende el marco en los cuatro lados de la ventana.</span><span class="sxs-lookup"><span data-stu-id="64e68-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="64e68-143">En el código siguiente se muestra el uso de [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) para extender el marco.</span><span class="sxs-lookup"><span data-stu-id="64e68-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="64e68-144">Tenga en cuenta que la extensión de marco se realiza dentro del mensaje de [**\_ activación de WM**](/windows/desktop/inputdev/wm-activate) en lugar del mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="64e68-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="64e68-145">Esto garantiza que la extensión de marco se administra correctamente cuando la ventana tiene el tamaño predeterminado y cuando está maximizada.</span><span class="sxs-lookup"><span data-stu-id="64e68-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="64e68-146">La siguiente imagen muestra un marco de ventana estándar (a la izquierda) y el mismo marco de ventana extendido (a la derecha).</span><span class="sxs-lookup"><span data-stu-id="64e68-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="64e68-147">El marco se extiende mediante el ejemplo de código anterior y el predeterminado Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (color \_ window + 1).</span><span class="sxs-lookup"><span data-stu-id="64e68-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![captura de pantalla de un fotograma estándar (izquierda) y marco extendido (derecha) con fondo blanco](images/white-sidebyside.png)

<span data-ttu-id="64e68-149">La diferencia visual entre estas dos ventanas es muy sutil.</span><span class="sxs-lookup"><span data-stu-id="64e68-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="64e68-150">La única diferencia entre los dos es que en la ventana de la derecha falta el borde de línea negra fina de la región cliente en la ventana de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="64e68-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="64e68-151">El motivo de este borde que falta es que se incorpora en el marco extendido, pero el resto del área cliente no lo está.</span><span class="sxs-lookup"><span data-stu-id="64e68-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="64e68-152">Para que los fotogramas extendidos sean visibles, las regiones subyacentes de cada uno de los lados del marco extendido deben tener datos de píxeles con un valor alfa de 0.</span><span class="sxs-lookup"><span data-stu-id="64e68-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="64e68-153">El borde negro alrededor de la región del cliente tiene datos de píxeles en los que todos los valores de color (rojo, verde, azul y alfa) se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="64e68-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="64e68-154">El resto del fondo no tiene el valor alfa establecido en 0, por lo que el resto del marco extendido no es visible.</span><span class="sxs-lookup"><span data-stu-id="64e68-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="64e68-155">La manera más sencilla de asegurarse de que los fotogramas extendidos están visibles es pintar todo el color de la región cliente.</span><span class="sxs-lookup"><span data-stu-id="64e68-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="64e68-156">Para ello, inicialice el miembro *hbrBackground* de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) o [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en el identificador del pincel negro de acciones \_ .</span><span class="sxs-lookup"><span data-stu-id="64e68-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="64e68-157">La siguiente imagen muestra el mismo marco estándar (izquierda) y el marco extendido (derecha) mostrados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="64e68-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="64e68-158">Sin embargo, esta vez *hbrBackground* se establece en el \_ controlador de pincel negro Obtenido de la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="64e68-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![captura de pantalla de un fotograma estándar (izquierda) y marco extendido (derecha) con fondo negro](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="64e68-160">Quitar el fotograma estándar</span><span class="sxs-lookup"><span data-stu-id="64e68-160">Removing the Standard Frame</span></span>

<span data-ttu-id="64e68-161">Después de extender el marco de la aplicación y hacer que esté visible, puede quitar el fotograma estándar.</span><span class="sxs-lookup"><span data-stu-id="64e68-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="64e68-162">Quitar el fotograma estándar permite controlar el ancho de cada lado del marco en lugar de simplemente extender el fotograma estándar.</span><span class="sxs-lookup"><span data-stu-id="64e68-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="64e68-163">Para quitar el marco de ventana estándar, debe controlar el mensaje de [**\_ NCCALCSIZE de WM**](/windows/desktop/winmsg/wm-nccalcsize) , en concreto cuando el valor de *wParam* es **true** y el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="64e68-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="64e68-164">Al hacerlo, la aplicación usa toda la región de la ventana como el área cliente, quitando el fotograma estándar.</span><span class="sxs-lookup"><span data-stu-id="64e68-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="64e68-165">Los resultados del control del mensaje de [**\_ NCCALCSIZE de WM**](/windows/desktop/winmsg/wm-nccalcsize) no estarán visibles hasta que sea necesario cambiar el tamaño de la región del cliente.</span><span class="sxs-lookup"><span data-stu-id="64e68-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="64e68-166">Hasta ese momento, la vista inicial de la ventana aparece con el marco estándar y los bordes extendidos.</span><span class="sxs-lookup"><span data-stu-id="64e68-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="64e68-167">Para solucionar este error, debe cambiar el tamaño de la ventana o realizar una acción que inicie un mensaje de **\_ NCCALCSIZE de WM** en el momento de la creación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="64e68-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="64e68-168">Esto puede realizarse mediante el uso de la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para desplace la ventana y cambiar su tamaño.</span><span class="sxs-lookup"><span data-stu-id="64e68-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="64e68-169">En el código siguiente se muestra una llamada a **SetWindowPos** que fuerza el envío de un mensaje de **WM \_ NCCALCSIZE** con los atributos de rectángulo de la ventana actual y la \_ marca FRAMECHANGED de SWP.</span><span class="sxs-lookup"><span data-stu-id="64e68-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="64e68-170">En la imagen siguiente se muestra el marco estándar (izquierda) y el fotograma recién extendido sin el marco estándar (derecha).</span><span class="sxs-lookup"><span data-stu-id="64e68-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![captura de pantalla de un fotograma estándar (izquierda) y un fotograma personalizado (derecha)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="64e68-172">Dibujar en la ventana de marco extendido</span><span class="sxs-lookup"><span data-stu-id="64e68-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="64e68-173">Al quitar el fotograma estándar, pierde el dibujo automático del icono de la aplicación y del título.</span><span class="sxs-lookup"><span data-stu-id="64e68-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="64e68-174">Para volver a agregarlos a la aplicación, debe dibujarlos usted mismo.</span><span class="sxs-lookup"><span data-stu-id="64e68-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="64e68-175">Para ello, primero examine el cambio que se ha producido en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="64e68-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="64e68-176">Con la eliminación del fotograma estándar, el área de cliente ahora se compone de toda la ventana, incluido el marco extendido.</span><span class="sxs-lookup"><span data-stu-id="64e68-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="64e68-177">Esto incluye la región donde se dibujan los botones de título.</span><span class="sxs-lookup"><span data-stu-id="64e68-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="64e68-178">En la siguiente comparación en paralelo, el área cliente para el fotograma estándar y el marco extendido personalizado se resaltan en rojo.</span><span class="sxs-lookup"><span data-stu-id="64e68-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="64e68-179">El área cliente de la ventana de marco estándar (izquierda) es la región negra.</span><span class="sxs-lookup"><span data-stu-id="64e68-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="64e68-180">En la ventana marco extendido (derecha), el área cliente es toda la ventana.</span><span class="sxs-lookup"><span data-stu-id="64e68-180">On the extended frame window (right), the client area is the entire window.</span></span>

![captura de pantalla de las áreas de cliente destacadas en rojo en el marco estándar y personalizado](images/clientarea-sidebyside.png)

<span data-ttu-id="64e68-182">Dado que toda la ventana es el área de cliente, puede dibujar simplemente lo que desea en el marco extendido.</span><span class="sxs-lookup"><span data-stu-id="64e68-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="64e68-183">Para agregar un título a la aplicación, solo tiene que dibujar texto en la región adecuada.</span><span class="sxs-lookup"><span data-stu-id="64e68-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="64e68-184">En la imagen siguiente se muestra el texto con los que se dibuja en el marco de título personalizado.</span><span class="sxs-lookup"><span data-stu-id="64e68-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="64e68-185">El título se dibuja con la función [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="64e68-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="64e68-186">Para ver el código que pinta el título, vea [el Apéndice B: pintar el título del](#appendix-b-painting-the-caption-title)título.</span><span class="sxs-lookup"><span data-stu-id="64e68-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![captura de pantalla de un marco personalizado con título](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="64e68-188">Al dibujar en el marco personalizado, tenga cuidado al colocar controles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="64e68-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="64e68-189">Dado que toda la ventana es su región de cliente, debe ajustar la posición del control de interfaz de usuario para cada ancho de marco si no desea que aparezcan en o en el marco extendido.</span><span class="sxs-lookup"><span data-stu-id="64e68-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="64e68-190">Habilitar la prueba de posicionamiento para el marco personalizado</span><span class="sxs-lookup"><span data-stu-id="64e68-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="64e68-191">Un efecto secundario de quitar el fotograma estándar es la pérdida del cambio de tamaño y el comportamiento de movimiento predeterminados.</span><span class="sxs-lookup"><span data-stu-id="64e68-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="64e68-192">Para que la aplicación eMule correctamente el comportamiento estándar de las ventanas, debe implementar la lógica para controlar las pruebas de posicionamiento de los botones de título y el cambio de tamaño o movimiento de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="64e68-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="64e68-193">En el caso de las pruebas de posicionamiento de los botones de título, DWM proporciona la función [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="64e68-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="64e68-194">Para realizar correctamente una prueba de posicionamiento de los botones de título en escenarios de fotogramas personalizados, los mensajes se deben pasar primero a **DwmDefWindowProc** para el control.</span><span class="sxs-lookup"><span data-stu-id="64e68-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="64e68-195">**DwmDefWindowProc** devuelve **true** si se controla un mensaje y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="64e68-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="64e68-196">Si **DwmDefWindowProc** no controla el mensaje, la aplicación debe controlar el mensaje en sí o pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="64e68-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="64e68-197">Para cambiar el tamaño y mover el marco, la aplicación debe proporcionar la lógica de la prueba de posicionamiento y controlar los mensajes de prueba de posicionamiento del marco.</span><span class="sxs-lookup"><span data-stu-id="64e68-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="64e68-198">Los mensajes de prueba de posicionamiento de fotogramas se le envían a través del mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) , incluso si la aplicación crea un marco personalizado sin el marco estándar.</span><span class="sxs-lookup"><span data-stu-id="64e68-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="64e68-199">En el código siguiente se muestra cómo controlar el mensaje de **\_ NCHITTEST de WM** cuando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no lo controla.</span><span class="sxs-lookup"><span data-stu-id="64e68-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="64e68-200">Para ver el código de la `HitTestNCA` función llamada, vea [Apéndice C: función HitTestNCA](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="64e68-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="64e68-201">Apéndice A: procedimiento de ventana de ejemplo</span><span class="sxs-lookup"><span data-stu-id="64e68-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="64e68-202">En el ejemplo de código siguiente se muestra un procedimiento de ventana y sus funciones de trabajo auxiliares que se usan para crear una aplicación de marco personalizada.</span><span class="sxs-lookup"><span data-stu-id="64e68-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="64e68-203">Apéndice B: pintar el título del título</span><span class="sxs-lookup"><span data-stu-id="64e68-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="64e68-204">En el código siguiente se muestra cómo pintar un título de título en el marco extendido.</span><span class="sxs-lookup"><span data-stu-id="64e68-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="64e68-205">Se debe llamar a esta función desde las llamadas a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="64e68-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="64e68-206">Apéndice C: función HitTestNCA</span><span class="sxs-lookup"><span data-stu-id="64e68-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="64e68-207">En el código siguiente se muestra la función que se `HitTestNCA` usa [para habilitar la prueba de posicionamiento para el marco personalizado](#enabling-hit-testing-for-the-custom-frame).</span><span class="sxs-lookup"><span data-stu-id="64e68-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="64e68-208">Esta función controla la lógica de la prueba de posicionamiento para el [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) cuando [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) no controla el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64e68-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="64e68-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64e68-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64e68-210">[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)</span><span class="sxs-lookup"><span data-stu-id="64e68-210">[Desktop Window Manager Overview](dwm-overview.md)</span></span>
</dt> </dl>

 

 