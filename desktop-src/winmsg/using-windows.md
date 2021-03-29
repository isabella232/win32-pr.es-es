---
description: En los ejemplos de esta sección se describe cómo realizar tareas asociadas al uso de Windows.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Uso de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912606"
---
# <a name="using-windows"></a><span data-ttu-id="75809-103">Uso de Windows</span><span class="sxs-lookup"><span data-stu-id="75809-103">Using Windows</span></span>

<span data-ttu-id="75809-104">En los ejemplos de esta sección se describe cómo realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="75809-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="75809-105">Crear una ventana principal</span><span class="sxs-lookup"><span data-stu-id="75809-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="75809-106">Crear, enumerar y ajustar el tamaño de las ventanas secundarias</span><span class="sxs-lookup"><span data-stu-id="75809-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="75809-107">Destruir una ventana</span><span class="sxs-lookup"><span data-stu-id="75809-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="75809-108">Usar ventanas superpuestas</span><span class="sxs-lookup"><span data-stu-id="75809-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="75809-109">Crear una ventana principal</span><span class="sxs-lookup"><span data-stu-id="75809-109">Creating a Main Window</span></span>

<span data-ttu-id="75809-110">La primera ventana que crea una aplicación es normalmente la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="75809-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="75809-111">La ventana principal se crea mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana, el nombre de la ventana, los estilos de ventana, el tamaño, la posición, el identificador de menú, el identificador de instancia y los datos de creación.</span><span class="sxs-lookup"><span data-stu-id="75809-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="75809-112">Una ventana principal pertenece a una clase de ventana definida por la aplicación, por lo que debe registrar la clase de ventana y proporcionar un procedimiento de ventana para la clase antes de crear la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="75809-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="75809-113">Normalmente, la mayoría de las aplicaciones usan el estilo [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) para crear la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="75809-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="75809-114">Este estilo proporciona a la ventana una barra de título, un menú ventana, un borde de ajuste de tamaño y botones minimizar y maximizar.</span><span class="sxs-lookup"><span data-stu-id="75809-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="75809-115">La función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) devuelve un identificador que identifica de forma única la ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="75809-116">En el ejemplo siguiente se crea una ventana principal que pertenece a una clase de ventana definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75809-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="75809-117">El nombre de la ventana, la **ventana principal**, aparecerá en la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="75809-118">Mediante la combinación de los estilos [**WS \_ VSCROLL**](window-styles.md) y **WS \_ HSCROLL** con el estilo **WS \_ OVERLAPPEDWINDOW** , la aplicación crea una ventana principal con barras de desplazamiento horizontal y vertical además de los componentes proporcionados por el estilo **WS \_ OVERLAPPEDWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="75809-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="75809-119">Las cuatro apariciones de la constante **\_ USEDEFAULT de CW** establecen el tamaño inicial y la posición de la ventana en los valores predeterminados definidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="75809-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="75809-120">Al especificar **null** en lugar de un identificador de menú, la ventana tendrá el menú definido para la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="75809-121">Observe que en el ejemplo anterior se llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) después de crear la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="75809-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="75809-122">Esto se hace porque el sistema no muestra automáticamente la ventana principal después de crearla.</span><span class="sxs-lookup"><span data-stu-id="75809-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="75809-123">Al pasar la marca **SW \_ SHOWDEFAULT** a **ShowWindow**, la aplicación permite que el programa que inició la aplicación establezca el estado de presentación inicial de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="75809-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="75809-124">La función [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) envía la ventana su primer mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="75809-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="75809-125">Crear, enumerar y ajustar el tamaño de las ventanas secundarias</span><span class="sxs-lookup"><span data-stu-id="75809-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="75809-126">Puede dividir el área de cliente de una ventana en distintas áreas funcionales mediante el uso de ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="75809-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="75809-127">La creación de una ventana secundaria es como la creación de una ventana principal: se usa la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="75809-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="75809-128">Para crear una ventana de una clase de ventana definida por la aplicación, debe registrar la clase de ventana y proporcionar un procedimiento de ventana antes de crear la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="75809-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="75809-129">Debe asignar a la ventana secundaria el [**estilo \_ secundario WS**](window-styles.md) y especificar una ventana primaria para la ventana secundaria al crearla.</span><span class="sxs-lookup"><span data-stu-id="75809-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="75809-130">En el ejemplo siguiente se divide el área cliente de la ventana principal de una aplicación en tres áreas funcionales mediante la creación de tres ventanas secundarias de igual tamaño.</span><span class="sxs-lookup"><span data-stu-id="75809-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="75809-131">Cada ventana secundaria tiene el mismo alto que el área cliente de la ventana principal, pero cada una de ellas tiene un ancho de un tercio.</span><span class="sxs-lookup"><span data-stu-id="75809-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="75809-132">La ventana principal crea las ventanas secundarias en respuesta al mensaje de [**\_ creación de WM**](wm-create.md) , que la ventana principal recibe durante su propio proceso de creación de ventanas.</span><span class="sxs-lookup"><span data-stu-id="75809-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="75809-133">Dado que cada ventana secundaria tiene el estilo de [**\_ borde de WS**](window-styles.md) , cada una tiene un borde de línea fino.</span><span class="sxs-lookup"><span data-stu-id="75809-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="75809-134">Además, dado que no se especifica el estilo **\_ visible de WS** , cada ventana secundaria está oculta inicialmente.</span><span class="sxs-lookup"><span data-stu-id="75809-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="75809-135">Observe también que a cada ventana secundaria se le asigna un identificador de ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="75809-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="75809-136">La ventana principal cambia el tamaño de las ventanas secundarias en respuesta al mensaje de [**\_ tamaño de WM**](wm-size.md) , que recibe la ventana principal cuando cambia el tamaño.</span><span class="sxs-lookup"><span data-stu-id="75809-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="75809-137">En respuesta al **\_ tamaño de WM**, la ventana principal recupera las dimensiones de su área de cliente mediante la función [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) y, a continuación, pasa las dimensiones a la función [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) .</span><span class="sxs-lookup"><span data-stu-id="75809-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="75809-138">**EnumChildWindows** pasa el identificador a cada ventana secundaria, a su vez, a la función de devolución de llamada [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75809-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="75809-139">Esta función dimensiona y coloca cada ventana secundaria mediante una llamada a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) . el tamaño y la posición se basan en las dimensiones del área cliente de la ventana principal y el identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="75809-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="75809-140">Después, **EnumChildProc** llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) para que la ventana sea visible.</span><span class="sxs-lookup"><span data-stu-id="75809-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="75809-141">Destruir una ventana</span><span class="sxs-lookup"><span data-stu-id="75809-141">Destroying a Window</span></span>

<span data-ttu-id="75809-142">Puede usar la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir una ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="75809-143">Normalmente, una aplicación envía el mensaje de [**\_ cierre de WM**](wm-close.md) antes de destruir una ventana, con lo que la ventana tiene la oportunidad de solicitar confirmación al usuario antes de que se destruya la ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="75809-144">Una ventana que incluye un menú ventana recibe automáticamente el mensaje de **\_ cierre de WM** cuando el usuario hace clic en **cerrar** en el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="75809-145">Si el usuario confirma que se debe destruir la ventana, la aplicación llama a **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="75809-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="75809-146">El sistema envía el mensaje de [**\_ destrucción de WM**](wm-destroy.md) a la ventana después de quitarlo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="75809-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="75809-147">En respuesta a **la \_ destrucción de WM**, la ventana guarda sus datos y libera todos los recursos que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="75809-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="75809-148">Una ventana principal finaliza su procesamiento de **WM \_ Destroy** mediante una llamada a la función [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) para salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75809-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="75809-149">En el ejemplo siguiente se muestra cómo solicitar confirmación del usuario antes de destruir una ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="75809-150">En respuesta a [**la \_ cierre de WM**](wm-close.md), en el ejemplo se muestra un cuadro de diálogo que contiene los botones **sí**, **no** y **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="75809-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="75809-151">Si el usuario hace clic en **sí**, se llama a [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ; de lo contrario, no se destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="75809-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="75809-152">Dado que la ventana que se va a destruir es una ventana principal, el ejemplo llama a [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) en respuesta a [**WM \_ Destroy**](wm-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="75809-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="75809-153">Usar ventanas superpuestas</span><span class="sxs-lookup"><span data-stu-id="75809-153">Using Layered Windows</span></span>

<span data-ttu-id="75809-154">Para que aparezca un cuadro de diálogo como ventana translúcida, primero debe crear el cuadro de diálogo como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="75809-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="75809-155">Después, en [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md), establezca el bit en capas del estilo extendido de la ventana y llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) con el valor alfa deseado.</span><span class="sxs-lookup"><span data-stu-id="75809-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="75809-156">El código podría tener este aspecto:</span><span class="sxs-lookup"><span data-stu-id="75809-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="75809-157">Tenga en cuenta que el tercer parámetro de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) es un valor comprendido entre 0 y 255, con 0 para que la ventana sea completamente transparente y 255 lo que lo convierte en totalmente opaca.</span><span class="sxs-lookup"><span data-stu-id="75809-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="75809-158">Este parámetro imita el [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) más versátil de la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="75809-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="75809-159">Para que esta ventana vuelva a ser totalmente opaca, quite el bit por **\_ \_ capas de WS ex** llamando a [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) y, a continuación, pida a la ventana que vuelva a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="75809-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="75809-160">Se desea quitar el bit para que el sistema sepa que puede liberar alguna memoria asociada a la disposición en capas y el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="75809-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="75809-161">El código podría tener este aspecto:</span><span class="sxs-lookup"><span data-stu-id="75809-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="75809-162">Para usar las ventanas secundarias superpuestas, la aplicación tiene que declararse como compatible con Windows 8 en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="75809-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
