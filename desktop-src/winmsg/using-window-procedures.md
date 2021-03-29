---
description: En esta sección se explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana de.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Usar procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912609"
---
# <a name="using-window-procedures"></a><span data-ttu-id="454a0-103">Usar procedimientos de ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-103">Using Window Procedures</span></span>

<span data-ttu-id="454a0-104">En esta sección se explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana de.</span><span class="sxs-lookup"><span data-stu-id="454a0-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="454a0-105">Diseñar un procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="454a0-106">Asociar un procedimiento de ventana a una clase de ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="454a0-107">Subclase de una ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="454a0-108">Diseñar un procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-108">Designing a Window Procedure</span></span>

<span data-ttu-id="454a0-109">En el ejemplo siguiente se muestra la estructura de un procedimiento de ventana típico.</span><span class="sxs-lookup"><span data-stu-id="454a0-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="454a0-110">El procedimiento de ventana utiliza el argumento de mensaje en una instrucción **Switch** con mensajes individuales administrados por instrucciones **Case** independientes.</span><span class="sxs-lookup"><span data-stu-id="454a0-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="454a0-111">Tenga en cuenta que cada caso devuelve un valor específico para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="454a0-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="454a0-112">En el caso de los mensajes que no procesa, el procedimiento de ventana llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="454a0-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



<span data-ttu-id="454a0-113">El mensaje de [**\_ NCCREATE de WM**](wm-nccreate.md) se envía justo después de crear la ventana, pero si una aplicación responde a este mensaje devolviendo **false**, se produce un error en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="454a0-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="454a0-114">El mensaje de [**\_ creación de WM**](wm-create.md) se envía después de que ya se haya creado la ventana.</span><span class="sxs-lookup"><span data-stu-id="454a0-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="454a0-115">El mensaje de [**\_ destrucción de WM**](wm-destroy.md) se envía cuando la ventana está a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="454a0-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="454a0-116">La función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) se encarga de destruir las ventanas secundarias de la ventana que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="454a0-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="454a0-117">El mensaje de [**\_ NCDESTROY de WM**](wm-ncdestroy.md) se envía justo antes de que se destruya una ventana.</span><span class="sxs-lookup"><span data-stu-id="454a0-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="454a0-118">Como mínimo, un procedimiento de ventana debe procesar el mensaje [**de \_ dibujo de WM**](../gdi/wm-paint.md) para dibujarse a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="454a0-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="454a0-119">Normalmente, también debe controlar los mensajes del mouse y del teclado.</span><span class="sxs-lookup"><span data-stu-id="454a0-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="454a0-120">Consulte las descripciones de los mensajes individuales para determinar si el procedimiento de ventana debe controlarlos.</span><span class="sxs-lookup"><span data-stu-id="454a0-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="454a0-121">La aplicación puede llamar a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como parte del procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="454a0-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="454a0-122">En tal caso, la aplicación puede modificar los parámetros del mensaje antes de pasar el mensaje a **DefWindowProc**, o puede continuar con el procesamiento predeterminado después de realizar sus propias operaciones.</span><span class="sxs-lookup"><span data-stu-id="454a0-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="454a0-123">Un procedimiento de cuadro de diálogo recibe un mensaje de [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) en lugar de un mensaje de [**\_ creación de WM**](wm-create.md) y no pasa mensajes no procesados a la función [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="454a0-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="454a0-124">De lo contrario, un procedimiento de cuadro de diálogo es exactamente el mismo que el de un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="454a0-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="454a0-125">Asociar un procedimiento de ventana a una clase de ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="454a0-126">Para asociar un procedimiento de ventana a una clase de ventana, debe registrar la clase.</span><span class="sxs-lookup"><span data-stu-id="454a0-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="454a0-127">Debe rellenar una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con información sobre la clase y el miembro **lpfnWndProc** debe especificar la dirección del procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="454a0-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="454a0-128">Para registrar la clase, pase la dirección de la estructura **WNDCLASS** a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) .</span><span class="sxs-lookup"><span data-stu-id="454a0-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="454a0-129">Una vez que se ha registrado la clase de ventana, el procedimiento de ventana se asocia automáticamente a cada nueva ventana creada con esa clase.</span><span class="sxs-lookup"><span data-stu-id="454a0-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="454a0-130">En el ejemplo siguiente se muestra cómo asociar el procedimiento de ventana en el ejemplo anterior con una clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="454a0-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a><span data-ttu-id="454a0-131">Subclase de una ventana</span><span class="sxs-lookup"><span data-stu-id="454a0-131">Subclassing a Window</span></span>

<span data-ttu-id="454a0-132">Para subclases de una instancia de una ventana, llame a la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) y especifique el identificador de la ventana para subclaser la \_ marca GWL WndProc y un puntero al procedimiento de la subclase.</span><span class="sxs-lookup"><span data-stu-id="454a0-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="454a0-133">**SetWindowLong** devuelve un puntero al procedimiento de ventana original; Utilice este puntero para pasar mensajes al procedimiento original.</span><span class="sxs-lookup"><span data-stu-id="454a0-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="454a0-134">El procedimiento de ventana de subclase debe usar la función [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) para llamar al procedimiento de ventana original.</span><span class="sxs-lookup"><span data-stu-id="454a0-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="454a0-135">Para escribir código que sea compatible con las versiones de Windows de 32 y 64 bits, utilice la función [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) .</span><span class="sxs-lookup"><span data-stu-id="454a0-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="454a0-136">En el ejemplo siguiente se muestra cómo subclase de una instancia de un control de edición en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="454a0-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="454a0-137">El procedimiento de ventana subclase permite que el control de edición reciba toda la entrada del teclado, incluidas las teclas entrar y TAB, siempre que el control tenga el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="454a0-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
