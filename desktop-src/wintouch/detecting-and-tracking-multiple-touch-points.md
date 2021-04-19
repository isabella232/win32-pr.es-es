---
title: Detección y seguimiento de varios puntos táctiles
description: Detección y seguimiento de varios puntos táctiles
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Touch, varios puntos táctiles
- detección de varios puntos táctiles
- seguimiento de varios puntos táctiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488051"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="579fb-106">Detección y seguimiento de varios puntos táctiles</span><span class="sxs-lookup"><span data-stu-id="579fb-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="579fb-107">En los pasos siguientes se explica cómo realizar un seguimiento de varios puntos táctiles mediante Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="579fb-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="579fb-108">Cree una aplicación y habilite Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="579fb-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="579fb-109">Agregue un controlador para los puntos [**\_ táctiles**](wm-touchdown.md) y de seguimiento de WM.</span><span class="sxs-lookup"><span data-stu-id="579fb-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="579fb-110">Dibuje los puntos.</span><span class="sxs-lookup"><span data-stu-id="579fb-110">Draw the points.</span></span>

<span data-ttu-id="579fb-111">Una vez que la aplicación se esté ejecutando, representará los círculos en cada toque.</span><span class="sxs-lookup"><span data-stu-id="579fb-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="579fb-112">En la siguiente captura de pantalla se muestra el aspecto que tendrá la aplicación mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="579fb-112">The following screen shot shows how your application might look while running.</span></span>

![captura de pantalla que muestra una aplicación que representa los puntos táctiles como círculos verdes y amarillos](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="579fb-114">Creación de una aplicación y habilitación de Windows Touch</span><span class="sxs-lookup"><span data-stu-id="579fb-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="579fb-115">Comience con una aplicación de Microsoft Win32 mediante el Asistente para Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="579fb-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="579fb-116">Una vez completado el asistente, agregue compatibilidad para los mensajes de Windows Touch estableciendo la versión de Windows en targetver. h e incluyendo Windows. h y windowsx. h en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="579fb-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="579fb-117">En el código siguiente se muestra cómo establecer la versión de Windows en targetver. h.</span><span class="sxs-lookup"><span data-stu-id="579fb-117">The following code shows how to set the Windows version in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



<span data-ttu-id="579fb-118">En el código siguiente se muestra cómo se deben agregar las directivas de inclusión.</span><span class="sxs-lookup"><span data-stu-id="579fb-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="579fb-119">Además, puede crear algunas variables globales que se usarán más adelante.</span><span class="sxs-lookup"><span data-stu-id="579fb-119">Also, you can create some global variables that will be used later.</span></span>


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="579fb-120">Agregar controlador para los \_ puntos táctiles y de seguimiento de WM</span><span class="sxs-lookup"><span data-stu-id="579fb-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="579fb-121">En primer lugar, declare algunas variables que usa el controlador [**\_ táctil de WM**](wm-touchdown.md) en [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="579fb-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="579fb-122">Ahora, inicialice las variables usadas para almacenar los puntos táctiles y registre la ventana para la entrada táctil desde el método **InitInstance** .</span><span class="sxs-lookup"><span data-stu-id="579fb-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



<span data-ttu-id="579fb-123">A continuación, controle el mensaje de [**\_ pantalla táctil de WM**](wm-touchdown.md) desde el método [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="579fb-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="579fb-124">En el código siguiente se muestra una implementación del controlador para la **\_ función táctil de WM**.</span><span class="sxs-lookup"><span data-stu-id="579fb-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> <span data-ttu-id="579fb-125">Para poder usar la función [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , debe tener compatibilidad con PPP alta en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="579fb-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="579fb-126">Para obtener más información acerca de la compatibilidad con alta resolución de PPP, consulte la sección [alta de PPP]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="579fb-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="579fb-127">Ahora, cuando un usuario toca la pantalla, las posiciones en las que está tocando se almacenarán en la matriz de puntos.</span><span class="sxs-lookup"><span data-stu-id="579fb-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="579fb-128">El miembro **dwID** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) almacena un identificador que dependerá del hardware.</span><span class="sxs-lookup"><span data-stu-id="579fb-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="579fb-129">Para solucionar el problema del miembro dwID que depende del hardware, el controlador de mayúsculas y minúsculas de [**WM \_**](wm-touchdown.md) usa una función, **GetContactIndex**, que asigna el miembro **dwID** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) a un punto que se dibuja en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="579fb-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="579fb-130">En el código siguiente se muestra una implementación de esta función.</span><span class="sxs-lookup"><span data-stu-id="579fb-130">The following code shows an implementation of this function.</span></span>


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a><span data-ttu-id="579fb-131">Dibujar los puntos</span><span class="sxs-lookup"><span data-stu-id="579fb-131">Draw the Points</span></span>

<span data-ttu-id="579fb-132">Declare las siguientes variables para la rutina de dibujo.</span><span class="sxs-lookup"><span data-stu-id="579fb-132">Declare the following variables for the drawing routine.</span></span>


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



<span data-ttu-id="579fb-133">El contexto de presentación de memoria *memDC* se usa para almacenar un contexto de gráficos temporal que se intercambia con el contexto de presentación representado, *HDC*, para eliminar el parpadeo.</span><span class="sxs-lookup"><span data-stu-id="579fb-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="579fb-134">Implemente la rutina de dibujo, que toma los puntos que ha almacenado y dibuja un círculo en los puntos.</span><span class="sxs-lookup"><span data-stu-id="579fb-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="579fb-135">En el código siguiente se muestra cómo puede implementar el controlador de [**\_ Paint de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="579fb-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



<span data-ttu-id="579fb-136">Al ejecutar la aplicación, ahora debería tener un aspecto similar al de la ilustración del principio de esta sección.</span><span class="sxs-lookup"><span data-stu-id="579fb-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="579fb-137">Por diversión, puede dibujar algunas líneas adicionales alrededor de los puntos de toque.</span><span class="sxs-lookup"><span data-stu-id="579fb-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="579fb-138">En la captura de pantalla siguiente se muestra cómo la aplicación podría mirar con algunas líneas adicionales dibujadas alrededor de los círculos.</span><span class="sxs-lookup"><span data-stu-id="579fb-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![captura de pantalla que muestra una aplicación que representa los puntos táctiles como círculos con líneas a través de los centros y la intersección de los bordes de los puntos táctiles](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="579fb-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="579fb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="579fb-141">Entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="579fb-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 