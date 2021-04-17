---
description: En esta sección se explica cómo realizar tareas asociadas con la interfaz de múltiples documentos.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Usar la interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659963"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="34768-103">Usar la interfaz de varios documentos</span><span class="sxs-lookup"><span data-stu-id="34768-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="34768-104">En esta sección se explica cómo realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="34768-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="34768-105">Registrar clases secundarias y de ventana de marco</span><span class="sxs-lookup"><span data-stu-id="34768-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="34768-106">Crear ventanas de marco y secundarias</span><span class="sxs-lookup"><span data-stu-id="34768-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="34768-107">Escribir el bucle de mensajes principal</span><span class="sxs-lookup"><span data-stu-id="34768-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="34768-108">Escribir el procedimiento de ventana de marco</span><span class="sxs-lookup"><span data-stu-id="34768-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="34768-109">Escribir el procedimiento de ventana secundaria</span><span class="sxs-lookup"><span data-stu-id="34768-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="34768-110">Crear una ventana secundaria</span><span class="sxs-lookup"><span data-stu-id="34768-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="34768-111">Para ilustrar estas tareas, en esta sección se incluyen ejemplos de multipad, una aplicación de interfaz de múltiples documentos (MDI) típica.</span><span class="sxs-lookup"><span data-stu-id="34768-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="34768-112">Registrar clases secundarias y de ventana de marco</span><span class="sxs-lookup"><span data-stu-id="34768-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="34768-113">Una aplicación MDI típica debe registrar dos clases de ventana: una para su ventana de marco y otra para sus ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="34768-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="34768-114">Si una aplicación admite más de un tipo de documento (por ejemplo, una hoja de cálculo y un gráfico), debe registrar una clase de ventana para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="34768-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="34768-115">La estructura de clase de la ventana de marco es similar a la estructura de clase de la ventana principal de las aplicaciones que no son de MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="34768-116">La estructura de clases de las ventanas secundarias MDI difiere ligeramente de la estructura de las ventanas secundarias de las aplicaciones que no son de MDI, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="34768-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="34768-117">La estructura de clase debe tener un icono, porque el usuario puede minimizar una ventana secundaria MDI como si fuera una ventana de aplicación normal.</span><span class="sxs-lookup"><span data-stu-id="34768-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="34768-118">El nombre de menú debe ser **null**, ya que una ventana secundaria MDI no puede tener su propio menú.</span><span class="sxs-lookup"><span data-stu-id="34768-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="34768-119">La estructura de clase debe reservar espacio adicional en la estructura de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34768-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="34768-120">Con este espacio, la aplicación puede asociar datos, como un nombre de archivo, a una ventana secundaria determinada.</span><span class="sxs-lookup"><span data-stu-id="34768-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="34768-121">En el ejemplo siguiente se muestra cómo MULTIPAD registra sus clases de ventana de marco y secundaria.</span><span class="sxs-lookup"><span data-stu-id="34768-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="34768-122">Crear ventanas de marco y secundarias</span><span class="sxs-lookup"><span data-stu-id="34768-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="34768-123">Después de registrar sus clases de ventana, una aplicación MDI puede crear sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="34768-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="34768-124">En primer lugar, crea su ventana de marco mediante la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="34768-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="34768-125">Después de crear la ventana de marco, la aplicación crea su ventana de cliente, de nuevo mediante **CreateWindow** o **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="34768-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="34768-126">La aplicación debe especificar MDICLIENT como el nombre de clase de la ventana del cliente; **MdiClient** es una clase de ventana registrada previamente definida por el sistema.</span><span class="sxs-lookup"><span data-stu-id="34768-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="34768-127">El parámetro *lpvParam* de **CreateWindow** o **CreateWindowEx** debe apuntar a una estructura [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) .</span><span class="sxs-lookup"><span data-stu-id="34768-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="34768-128">Esta estructura contiene los miembros que se describen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="34768-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="34768-129">Miembro</span><span class="sxs-lookup"><span data-stu-id="34768-129">Member</span></span>           | <span data-ttu-id="34768-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="34768-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34768-131">**hWindowMenu**</span><span class="sxs-lookup"><span data-stu-id="34768-131">**hWindowMenu**</span></span>  | <span data-ttu-id="34768-132">Identificador del menú de ventana que se usa para controlar las ventanas secundarias MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="34768-133">A medida que se crean ventanas secundarias, la aplicación agrega sus títulos al menú ventana como elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="34768-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="34768-134">Después, el usuario puede activar una ventana secundaria haciendo clic en su título en el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="34768-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="34768-135">**idFirstChild**</span><span class="sxs-lookup"><span data-stu-id="34768-135">**idFirstChild**</span></span> | <span data-ttu-id="34768-136">Especifica el identificador de la primera ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="34768-137">A la primera ventana secundaria MDI creada se le asigna este identificador.</span><span class="sxs-lookup"><span data-stu-id="34768-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="34768-138">Las ventanas adicionales se crean con identificadores de ventana incrementados.</span><span class="sxs-lookup"><span data-stu-id="34768-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="34768-139">Cuando se destruye una ventana secundaria, el sistema reasigna inmediatamente los identificadores de ventana para mantener su rango contiguo.</span><span class="sxs-lookup"><span data-stu-id="34768-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="34768-140">Cuando se agrega el título de una ventana secundaria al menú ventana, el sistema asigna un identificador a la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="34768-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="34768-141">Cuando el usuario hace clic en el título de una ventana secundaria, la ventana de marco recibe un mensaje de [**\_ comando de WM**](../menurc/wm-command.md) con el identificador en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="34768-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="34768-142">Debe especificar un valor para el miembro **idFirstChild** que no entra en conflicto con los identificadores de elemento de menú en el menú de la ventana marco.</span><span class="sxs-lookup"><span data-stu-id="34768-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="34768-143">El procedimiento de ventana marco de multipad crea la ventana del cliente MDI mientras procesa el mensaje de [**\_ creación de WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="34768-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="34768-144">En el ejemplo siguiente se muestra cómo se crea la ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="34768-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="34768-145">Los títulos de las ventanas secundarias se agregan a la parte inferior del menú ventana.</span><span class="sxs-lookup"><span data-stu-id="34768-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="34768-146">Si la aplicación agrega cadenas al menú ventana mediante la función [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , los títulos de las ventanas secundarias pueden sobrescribir estas cadenas cuando se vuelve a dibujar el menú ventana (siempre que se crea o se destruye una ventana secundaria).</span><span class="sxs-lookup"><span data-stu-id="34768-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="34768-147">Una aplicación MDI que agrega cadenas a su menú ventana debe usar la función [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) y comprobar que los títulos de las ventanas secundarias no han sobrescrito estas nuevas cadenas.</span><span class="sxs-lookup"><span data-stu-id="34768-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="34768-148">Use el estilo **WS \_ CLIPCHILDREN** para crear la ventana del cliente MDI a fin de evitar que la ventana dibuje sobre sus ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="34768-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="34768-149">Escribir el bucle de mensajes principal</span><span class="sxs-lookup"><span data-stu-id="34768-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="34768-150">El bucle de mensajes principal de una aplicación MDI es similar al de las teclas de aceleración de control de aplicaciones que no son MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="34768-151">La diferencia es que el bucle de mensajes MDI llama a la función [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) antes de comprobar las teclas de aceleración definidas por la aplicación o antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="34768-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="34768-152">En el ejemplo siguiente se muestra el bucle de mensajes de una aplicación MDI típica.</span><span class="sxs-lookup"><span data-stu-id="34768-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="34768-153">Tenga en cuenta que [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) puede devolver-1 si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="34768-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="34768-154">La función [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) convierte los mensajes [**\_ KEYDOWN de WM**](../inputdev/wm-keydown.md) en mensajes [**\_ SYSCOMMAND de WM**](../menurc/wm-syscommand.md) y los envía a la ventana secundaria MDI activa.</span><span class="sxs-lookup"><span data-stu-id="34768-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="34768-155">Si el mensaje no es un mensaje de acelerador MDI, la función devuelve **false**, en cuyo caso la aplicación utiliza la función [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) para determinar si se presionó alguna de las teclas de aceleración definidas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34768-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="34768-156">De lo contrario, el bucle envía el mensaje al procedimiento de ventana adecuado.</span><span class="sxs-lookup"><span data-stu-id="34768-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="34768-157">Escribir el procedimiento de ventana de marco</span><span class="sxs-lookup"><span data-stu-id="34768-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="34768-158">El procedimiento de ventana de una ventana de marco MDI es similar al de una ventana principal de la aplicación que no es de MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="34768-159">La diferencia es que un procedimiento de ventana de marco pasa todos los mensajes que no controla a la función [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) en lugar de a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="34768-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="34768-160">Además, el procedimiento de ventana marco también debe pasar algunos mensajes que controla, incluidos los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="34768-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="34768-161">Message</span><span class="sxs-lookup"><span data-stu-id="34768-161">Message</span></span>                                  | <span data-ttu-id="34768-162">Response</span><span class="sxs-lookup"><span data-stu-id="34768-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34768-163">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="34768-164">Activa la ventana secundaria MDI que el usuario elige.</span><span class="sxs-lookup"><span data-stu-id="34768-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="34768-165">Este mensaje se envía cuando el usuario elige una ventana secundaria MDI en el menú ventana de la ventana marco MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="34768-166">El identificador de ventana que acompaña a este mensaje identifica la ventana secundaria MDI que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="34768-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="34768-167">**MENUCHAR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="34768-168">Abre el menú ventana de la ventana secundaria MDI activa cuando el usuario presiona la combinación de teclas ALT + – (menos).</span><span class="sxs-lookup"><span data-stu-id="34768-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="34768-169">**SETFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="34768-170">Pasa el foco del teclado a la ventana del cliente MDI, que a su vez la pasa a la ventana secundaria MDI activa.</span><span class="sxs-lookup"><span data-stu-id="34768-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="34768-171">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="34768-172">Cambia el tamaño de la ventana del cliente MDI para que quepa en el área de cliente de la nueva ventana de marco.</span><span class="sxs-lookup"><span data-stu-id="34768-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="34768-173">Si el procedimiento de la ventana de marco ajusta el tamaño de la ventana del cliente MDI a un tamaño diferente, no debe pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="34768-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="34768-174">El procedimiento de ventana de marco en MULTIPAD se denomina MPFrameWndProc.</span><span class="sxs-lookup"><span data-stu-id="34768-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="34768-175">La administración de otros mensajes por MPFrameWndProc es similar a la de las aplicaciones que no son de MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="34768-176">[**WM \_**](../menurc/wm-command.md) Los mensajes de comando en MULTIPAD se controlan mediante la función CommandHandler definida localmente.</span><span class="sxs-lookup"><span data-stu-id="34768-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="34768-177">En el caso de los mensajes de comando MULTIPAD no controla, CommandHandler llama a la función [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) .</span><span class="sxs-lookup"><span data-stu-id="34768-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="34768-178">Si MULTIPAD no utiliza **DefFrameProc** de forma predeterminada, el usuario no puede activar una ventana secundaria desde el menú ventana, ya que el mensaje de **\_ comando de WM** enviado al hacer clic en el elemento de menú de la ventana se perdería.</span><span class="sxs-lookup"><span data-stu-id="34768-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="34768-179">Escribir el procedimiento de ventana secundaria</span><span class="sxs-lookup"><span data-stu-id="34768-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="34768-180">Al igual que el procedimiento de ventana de marco, un procedimiento de ventana secundaria MDI utiliza una función especial para procesar mensajes de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="34768-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="34768-181">Todos los mensajes que no controla el procedimiento de ventana secundaria se deben pasar a la función [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) en lugar de a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="34768-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="34768-182">Además, algunos mensajes de administración de ventanas se deben pasar a **DefMDIChildProc**, incluso si la aplicación controla el mensaje, para que MDI funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="34768-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="34768-183">A continuación se muestran los mensajes que la aplicación debe pasar a **DefMDIChildProc**.</span><span class="sxs-lookup"><span data-stu-id="34768-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="34768-184">Message</span><span class="sxs-lookup"><span data-stu-id="34768-184">Message</span></span>                                       | <span data-ttu-id="34768-185">Response</span><span class="sxs-lookup"><span data-stu-id="34768-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34768-186">**CHILDACTIVATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="34768-187">Realiza el procesamiento de la activación cuando las ventanas secundarias MDI se cambian de tamaño, se mueven o se muestran.</span><span class="sxs-lookup"><span data-stu-id="34768-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="34768-188">Este mensaje debe pasarse.</span><span class="sxs-lookup"><span data-stu-id="34768-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="34768-189">**GETMINMAXINFO de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="34768-190">Calcula el tamaño de una ventana secundaria MDI maximizada, en función del tamaño actual de la ventana del cliente MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="34768-191">**MENUCHAR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="34768-192">Pasa el mensaje a la ventana de marco MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="34768-193">**movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="34768-194">Vuelve a calcular las barras de desplazamiento del cliente MDI, si están presentes.</span><span class="sxs-lookup"><span data-stu-id="34768-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="34768-195">**SETFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="34768-196">Activa la ventana secundaria, si no es la ventana secundaria MDI activa.</span><span class="sxs-lookup"><span data-stu-id="34768-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="34768-197">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="34768-198">Realiza las operaciones necesarias para cambiar el tamaño de una ventana, sobre todo para maximizar o restaurar una ventana secundaria MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="34768-199">Si no se pasa este mensaje a la función [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , se generan resultados muy no deseados.</span><span class="sxs-lookup"><span data-stu-id="34768-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="34768-200">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="34768-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="34768-201">Comandos de menú de identificadores de ventana (anteriormente conocido como sistema): **SC \_ NEXTWINDOW**, **SC \_ PREVWINDOW**, **SC \_ Move**, **SC \_ size** y **SC \_ Maximize**.</span><span class="sxs-lookup"><span data-stu-id="34768-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="34768-202">Crear una ventana secundaria</span><span class="sxs-lookup"><span data-stu-id="34768-202">Creating a Child Window</span></span>

<span data-ttu-id="34768-203">Para crear una ventana secundaria MDI, una aplicación puede llamar a la función [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o enviar un mensaje de [**WM \_ MDICREATE**](wm-mdicreate.md) a la ventana del cliente MDI.</span><span class="sxs-lookup"><span data-stu-id="34768-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="34768-204">(La aplicación puede usar la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con el estilo **WS \_ ex \_ MDICHILD** para crear ventanas secundarias MDI). Una aplicación MDI de un solo subproceso puede utilizar cualquiera de los métodos para crear una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="34768-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="34768-205">Un subproceso de una aplicación MDI multiproceso debe utilizar la función **CreateMDIWindow** o **CreateWindowEx** para crear una ventana secundaria en un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="34768-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="34768-206">El parámetro *lParam* de un mensaje de [**\_ MDICREATE de WM**](wm-mdicreate.md) es un puntero lejano a una estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="34768-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="34768-207">La estructura incluye cuatro miembros de dimensión  : x **e y**, que indican las posiciones horizontal y vertical de la ventana, y **CX** y **CY**, que indican las extensiones horizontal y vertical de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34768-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="34768-208">La aplicación puede asignar explícitamente cualquiera de estos miembros, o bien se pueden establecer en **CW \_ USEDEFAULT**, en cuyo caso el sistema selecciona una posición, un tamaño o ambos, según un algoritmo en cascada.</span><span class="sxs-lookup"><span data-stu-id="34768-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="34768-209">En cualquier caso, se deben inicializar los cuatro miembros.</span><span class="sxs-lookup"><span data-stu-id="34768-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="34768-210">MULTIPAD usa **CW \_ USEDEFAULT** para todas las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="34768-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="34768-211">El último miembro de la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) es el miembro de **estilo** , que puede contener bits de estilo para la ventana.</span><span class="sxs-lookup"><span data-stu-id="34768-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="34768-212">Para crear una ventana secundaria MDI que puede tener cualquier combinación de estilos de ventana, especifique el estilo de ventana de **MDIS \_ ALLCHILDSTYLES** .</span><span class="sxs-lookup"><span data-stu-id="34768-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="34768-213">Cuando no se especifica este estilo, una ventana secundaria MDI tiene los **estilos \_ WS minimizar**, **WS \_ Maximize**, **WS \_ HSCROLL** y **WS \_ VSCROLL** como valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="34768-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="34768-214">MULTIPAD crea sus ventanas secundarias MDI mediante su función AddFile definida localmente (ubicada en el archivo de código fuente MPFILE. C).</span><span class="sxs-lookup"><span data-stu-id="34768-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="34768-215">La función AddFile establece el título de la ventana secundaria asignando el miembro **szTitle** de la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) de la ventana al nombre del archivo que se está editando o a "sin título".</span><span class="sxs-lookup"><span data-stu-id="34768-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="34768-216">El miembro **szClass** se establece en el nombre de la clase de ventana secundaria MDI registrada en la función InitializeApplication de multipad.</span><span class="sxs-lookup"><span data-stu-id="34768-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="34768-217">El miembro **hOwner** se establece en el identificador de instancia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34768-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="34768-218">En el ejemplo siguiente se muestra la función AddFile en MULTIPAD.</span><span class="sxs-lookup"><span data-stu-id="34768-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="34768-219">El puntero que se pasa en el parámetro *lParam* del mensaje de [**\_ MDICREATE de WM**](wm-mdicreate.md) se pasa a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) y aparece como el primer miembro de la estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , pasado en el mensaje de [**\_ creación de WM**](wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="34768-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="34768-220">En multipad, la ventana secundaria se inicializa automáticamente durante el procesamiento de los mensajes de **\_ creación de WM** Inicializando las variables de documento en sus datos adicionales y creando la ventana secundaria del control de edición.</span><span class="sxs-lookup"><span data-stu-id="34768-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
