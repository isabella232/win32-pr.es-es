---
title: Mejora de la experiencia de movimiento panorámico Single-Finger
description: Si compila una aplicación destinada a Windows Touch, proporciona automáticamente compatibilidad básica con el movimiento panorámico. Sin embargo, puede usar el \_ mensaje de gestos de WM para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Touch de Windows, movimiento panorámico con un solo dedor
- Windows Touch, movimiento panorámico
- Windows Touch, barras de desplazamiento
- Windows Touch, gestos
- Touch de Windows, mensajes de movimiento panorámico
- Windows Touch, comentarios de límite
- movimiento panorámico con un solo dedo
- movimiento panorámico, un dedo
- movimiento panorámico, comentarios de los límites
- barras de desplazamiento, movimiento panorámico con un solo dedo
- gestos, movimiento panorámico con un solo dedor
- barras de desplazamiento, deshabilitar
- gestos, deshabilitar
- gestos, mensajes de movimiento panorámico
- movimiento panorámico, mensajes de movimiento panorámico
- Comentarios de los límites, movimiento panorámico con un solo dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792165"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="c354b-120">Mejora de la experiencia de movimiento panorámico Single-Finger</span><span class="sxs-lookup"><span data-stu-id="c354b-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="c354b-121">Si compila una aplicación destinada a Windows Touch, proporciona automáticamente compatibilidad básica con el movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="c354b-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="c354b-122">Sin embargo, puede usar el mensaje de [**\_ gestos de WM**](wm-gesture.md) para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo dedo.</span><span class="sxs-lookup"><span data-stu-id="c354b-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="c354b-123">Información general</span><span class="sxs-lookup"><span data-stu-id="c354b-123">Overview</span></span>

<span data-ttu-id="c354b-124">Para mejorar la experiencia de movimiento panorámico con un solo dedo, siga estos pasos, como se explica en secciones posteriores de este tema:</span><span class="sxs-lookup"><span data-stu-id="c354b-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="c354b-125">Cree una aplicación con barras de desplazamiento y con los gestos deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="c354b-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="c354b-126">Agregar compatibilidad para mensajes de movimiento panorámico de gestos.</span><span class="sxs-lookup"><span data-stu-id="c354b-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="c354b-127">Habilitar rebote.</span><span class="sxs-lookup"><span data-stu-id="c354b-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="c354b-128">Crear una aplicación con barras de desplazamiento y con gestos deshabilitados</span><span class="sxs-lookup"><span data-stu-id="c354b-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="c354b-129">Antes de comenzar, debe crear una aplicación con barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c354b-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="c354b-130">En la sección [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) se explica este proceso.</span><span class="sxs-lookup"><span data-stu-id="c354b-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="c354b-131">Si desea empezar con el contenido del ejemplo, vaya a esa sección y cree una aplicación con barras de desplazamiento y, a continuación, deshabilite los gestos.</span><span class="sxs-lookup"><span data-stu-id="c354b-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="c354b-132">Si ya tiene una aplicación con barras de desplazamiento en funcionamiento, deshabilite los gestos tal y como se describe en esa sección.</span><span class="sxs-lookup"><span data-stu-id="c354b-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="c354b-133">Incorporación de compatibilidad personalizada de movimiento panorámico para mensajes de movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="c354b-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="c354b-134">Para admitir mensajes de movimiento panorámico de gestos, debe controlarlos en el método **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="c354b-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="c354b-135">Los mensajes de gestos se usan para determinar los diferencias horizontales y verticales de los mensajes de pan.</span><span class="sxs-lookup"><span data-stu-id="c354b-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="c354b-136">Las diferencias se utilizan para actualizar el objeto de barra de desplazamiento, que actualiza la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c354b-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="c354b-137">En primer lugar, actualice la configuración de la versión de Windows en el archivo targetver. h para habilitar Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="c354b-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="c354b-138">En el código siguiente se muestran los distintos valores de la versión de Windows que deben reemplazarse en targetver. h.</span><span class="sxs-lookup"><span data-stu-id="c354b-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="c354b-139">A continuación, agregue el archivo UXTheme. h al proyecto y agregue la biblioteca uxtheme. lib a las dependencias adicionales del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c354b-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="c354b-140">A continuación, agregue las siguientes variables al principio de la función **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="c354b-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="c354b-141">Se usarán en los cálculos para la panorámica.</span><span class="sxs-lookup"><span data-stu-id="c354b-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="c354b-142">A continuación, agregue el controlador del mensaje de [**\_ gestos de WM**](wm-gesture.md) para que las barras de desplazamiento se actualicen con deltas basadas en gestos de movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="c354b-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="c354b-143">Esto le ofrece un control mucho más preciso de la panorámica.</span><span class="sxs-lookup"><span data-stu-id="c354b-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="c354b-144">En el código siguiente se obtiene la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) de *lParam*, se guarda la última coordenada y de la estructura y se determina el cambio en la posición para actualizar el objeto de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c354b-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="c354b-145">El código siguiente debe colocarse en la instrucción del modificador **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="c354b-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="c354b-146">Ahora, cuando realice el gesto de panorámica en la ventana, verá el texto desplazarse con inercia.</span><span class="sxs-lookup"><span data-stu-id="c354b-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="c354b-147">En este punto, es posible que desee cambiar el texto para que tenga más líneas para poder explorar grandes secciones de texto.</span><span class="sxs-lookup"><span data-stu-id="c354b-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="c354b-148">Comentarios de los límites en WndProc</span><span class="sxs-lookup"><span data-stu-id="c354b-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="c354b-149">Los comentarios de los límites son un tipo de comentarios visuales que se conceden a los usuarios cuando llegan al final de un área panorámica.</span><span class="sxs-lookup"><span data-stu-id="c354b-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="c354b-150">Lo desencadena la aplicación cuando se alcanza un límite.</span><span class="sxs-lookup"><span data-stu-id="c354b-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="c354b-151">En la implementación de ejemplo anterior del mensaje de [**\_ gestos de WM**](wm-gesture.md) , se usa la condición de finalización del `(si.nPos == si.yPos)` caso de **\_ gestos de WM** para probar que se ha alcanzado el final de una región de movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="c354b-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="c354b-152">Las variables siguientes se utilizan para realizar el seguimiento de los valores y los errores de prueba.</span><span class="sxs-lookup"><span data-stu-id="c354b-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="c354b-153">El caso de gestos de panorámica se actualiza para desencadenar los comentarios de los límites.</span><span class="sxs-lookup"><span data-stu-id="c354b-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="c354b-154">En el código siguiente se muestra el caso de **\_ pan GID** del controlador de mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="c354b-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="c354b-155">Ahora la ventana de la aplicación debe tener comentarios sobre los límites cuando un usuario se desplaza más allá de la parte inferior del área de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c354b-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c354b-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c354b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c354b-157">Gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="c354b-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="c354b-158">**BeginPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="c354b-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="c354b-159">**EndPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="c354b-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="c354b-160">**UpdatePanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="c354b-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 