---
title: Compatibilidad heredada con la panorámica con barras de desplazamiento
description: En esta sección se describe la compatibilidad con la panorámica mediante barras de desplazamiento en aplicaciones basadas en Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch, compatibilidad heredada
- panorámica con barras de desplazamiento
- Windows Touch, panorámica con barras de desplazamiento
- Windows Touch, barras de desplazamiento
- barras de desplazamiento, movimiento panorámico
- barras de desplazamiento, compatibilidad heredada
- Windows Touch, gestos
- gestos, panorámica con barras de desplazamiento
- Windows Touch, gestos
- gestos, panorámica con barras de desplazamiento
- gestos, deshabilitar
- Windows Touch, mensajes de la rueda del mouse
- mensajes de la rueda del mouse
- Windows Touch, personalización de movimiento panorámico
- movimiento panorámico, barras de desplazamiento
- panorámica, compatibilidad heredada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571479"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="bee3f-119">Compatibilidad heredada con la panorámica con barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="bee3f-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="bee3f-120">En esta sección se describe la compatibilidad con la panorámica mediante barras de desplazamiento en aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="bee3f-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="bee3f-121">En Windows 7, los gestos de movimiento panorámico generan \_ \* mensajes de desplazamiento de WM para habilitar la compatibilidad heredada con el movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="bee3f-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="bee3f-122">Dado que es posible que las aplicaciones no admitan todos los mensajes de desplazamiento de WM \_ \* , puede que la panorámica no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="bee3f-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="bee3f-123">En este tema se describen los pasos que debe seguir para asegurarse de que la experiencia de movimiento panorámico heredada en las aplicaciones funcione como se espera en los usuarios.</span><span class="sxs-lookup"><span data-stu-id="bee3f-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="bee3f-124">Información general</span><span class="sxs-lookup"><span data-stu-id="bee3f-124">Overview</span></span>

<span data-ttu-id="bee3f-125">En las secciones siguientes se explica cómo habilitar la experiencia de movimiento panorámico heredada:</span><span class="sxs-lookup"><span data-stu-id="bee3f-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="bee3f-126">Cree una aplicación con barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="bee3f-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="bee3f-127">Deshabilitar gestos.</span><span class="sxs-lookup"><span data-stu-id="bee3f-127">Disable flicks.</span></span>
-   <span data-ttu-id="bee3f-128">Personalizar la experiencia de movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="bee3f-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="bee3f-129">Crear una aplicación con barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="bee3f-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="bee3f-130">Inicie un nuevo proyecto de Win32 con el Asistente para Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bee3f-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="bee3f-131">Asegúrese de que el tipo de aplicación está establecido en la aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="bee3f-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="bee3f-132">No es necesario habilitar la compatibilidad con el Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="bee3f-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="bee3f-133">En la imagen siguiente se muestra el aspecto que tendrá el proyecto después de haberse iniciado.</span><span class="sxs-lookup"><span data-stu-id="bee3f-133">The following image shows what your project will look like after you have started it.</span></span>

![captura de pantalla que muestra una ventana sin barras de desplazamiento](images/gpd-1.png)

<span data-ttu-id="bee3f-135">A continuación, habilite las barras de desplazamiento en la imagen.</span><span class="sxs-lookup"><span data-stu-id="bee3f-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="bee3f-136">Cambie el código de creación de la ventana en **InitInstance** para que la llamada a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) cree una ventana con barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="bee3f-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="bee3f-137">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="bee3f-137">The following code shows how to do this.</span></span>


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



<span data-ttu-id="bee3f-138">Después de cambiar el código de creación de la ventana, la aplicación tendrá una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="bee3f-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="bee3f-139">En la imagen siguiente se muestra el aspecto que podría tener la aplicación en este punto.</span><span class="sxs-lookup"><span data-stu-id="bee3f-139">The following image shows how the application might look at this point.</span></span>

![captura de pantalla que muestra una ventana con una barra de desplazamiento vertical pero sin texto](images/gpd-2.png)

<span data-ttu-id="bee3f-141">Después de cambiar el código de creación de la ventana, agregue un objeto de barra de desplazamiento a la aplicación y texto para desplazarse.</span><span class="sxs-lookup"><span data-stu-id="bee3f-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="bee3f-142">Coloque el código siguiente en la parte superior del método **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="bee3f-142">Place the following code into the top of the **WndProc** method.</span></span>


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



<span data-ttu-id="bee3f-143">A continuación, implemente la lógica de la aplicación para configurar los cálculos de texto para las métricas de texto.</span><span class="sxs-lookup"><span data-stu-id="bee3f-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="bee3f-144">El código siguiente debe reemplazar el caso existente de **\_ Create de WM** en la función **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="bee3f-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



<span data-ttu-id="bee3f-145">A continuación, implemente la lógica de la aplicación para volver a calcular el bloque de texto cuando se cambie el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bee3f-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="bee3f-146">El código siguiente debe colocarse en el cambio de mensaje en **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="bee3f-146">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



<span data-ttu-id="bee3f-147">A continuación, implemente la lógica de la aplicación para los mensajes de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="bee3f-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="bee3f-148">El código siguiente debe colocarse en el cambio de mensaje en **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="bee3f-148">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



<span data-ttu-id="bee3f-149">A continuación, actualice el código para volver a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="bee3f-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="bee3f-150">El código siguiente debe reemplazar el caso **de \_ Paint de WM** predeterminado en **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="bee3f-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



<span data-ttu-id="bee3f-151">Ahora, al compilar y ejecutar la aplicación, debe tener el texto reutilizable y una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="bee3f-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="bee3f-152">En la imagen siguiente se muestra el aspecto que podría tener la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bee3f-152">The following image shows how your application might look.</span></span>

![captura de pantalla que muestra una ventana con una barra de desplazamiento vertical y texto](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="bee3f-154">Deshabilitar gestos</span><span class="sxs-lookup"><span data-stu-id="bee3f-154">Disable Flicks</span></span>

<span data-ttu-id="bee3f-155">Para mejorar la experiencia de movimiento panorámico en la aplicación, debe desactivar los gestos.</span><span class="sxs-lookup"><span data-stu-id="bee3f-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="bee3f-156">Para ello, establezca las propiedades de la ventana en el valor *hWnd* cuando se inicializa.</span><span class="sxs-lookup"><span data-stu-id="bee3f-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="bee3f-157">Los valores usados para los gestos se almacenan en el encabezado tpcshrd. h, que también se debe incluir.</span><span class="sxs-lookup"><span data-stu-id="bee3f-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="bee3f-158">El código siguiente debe colocarse en las directivas de inclusión y en la función **InitInstance** después de haber creado el *hWnd*.</span><span class="sxs-lookup"><span data-stu-id="bee3f-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="bee3f-159">Esto resulta útil para las aplicaciones que requieren comentarios inmediatos sobre un evento Touch o Pen Down en lugar de probar un umbral de tiempo o de distancia.</span><span class="sxs-lookup"><span data-stu-id="bee3f-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a><span data-ttu-id="bee3f-160">Personalización de la experiencia de movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="bee3f-160">Customize the Panning Experience</span></span>

<span data-ttu-id="bee3f-161">Es posible que desee una experiencia de movimiento panorámico diferente a la de las ofertas de Windows 7 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bee3f-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="bee3f-162">Para mejorar la experiencia de movimiento panorámico, debe agregar el controlador para el mensaje de [**\_ gesto de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="bee3f-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="bee3f-163">Para obtener más información, consulte [mejorar la experiencia de movimiento panorámico Single-Finger](improving-the-single-finger-panning-experience.md).</span><span class="sxs-lookup"><span data-stu-id="bee3f-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee3f-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bee3f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee3f-165">Gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="bee3f-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 