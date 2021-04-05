---
title: Cómo subclase de un cuadro combinado
description: En este tema se muestra cómo subclases de los cuadros combinados.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078469"
---
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="e59ab-103">Cómo subclase de un cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="e59ab-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="e59ab-104">En este tema se muestra cómo subclases de los cuadros combinados.</span><span class="sxs-lookup"><span data-stu-id="e59ab-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="e59ab-105">La aplicación de ejemplo de C++ crea una ventana de barra de herramientas que contiene dos cuadros combinados.</span><span class="sxs-lookup"><span data-stu-id="e59ab-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="e59ab-106">Mediante la subclase de los controles de edición dentro de los cuadros combinados, la ventana de la barra de herramientas intercepta las teclas TAB, entrar y ESC que, de lo contrario, se pasarían por alto.</span><span class="sxs-lookup"><span data-stu-id="e59ab-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e59ab-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="e59ab-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e59ab-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="e59ab-108">Technologies</span></span>

-   [<span data-ttu-id="e59ab-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="e59ab-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e59ab-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e59ab-110">Prerequisites</span></span>

-   <span data-ttu-id="e59ab-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e59ab-111">C/C++</span></span>
-   <span data-ttu-id="e59ab-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="e59ab-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e59ab-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e59ab-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="e59ab-114">Procesar el mensaje de creación de WM \_</span><span class="sxs-lookup"><span data-stu-id="e59ab-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="e59ab-115">La aplicación procesa el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) para crear dos controles de cuadro combinado como ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="e59ab-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



<span data-ttu-id="e59ab-116">A continuación, la aplicación subclase los controles de edición (campos de selección) en cada cuadro combinado, ya que reciben la entrada de caracteres para el cuadro combinado simple y desplegable.</span><span class="sxs-lookup"><span data-stu-id="e59ab-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="e59ab-117">Finalmente, llama a la función [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) para recuperar el identificador de cada control de edición.</span><span class="sxs-lookup"><span data-stu-id="e59ab-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="e59ab-118">Para subclaser los controles de edición, la aplicación llama a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , reemplazando el puntero al procedimiento de ventana de clase con un puntero a la función **SubClassProc** definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e59ab-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="e59ab-119">El puntero al procedimiento de ventana original se guarda en la variable global *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="e59ab-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="e59ab-120">**SubClassProc** intercepta las teclas TAB, ENTER y ESC, y notifica a la ventana de la barra de herramientas mediante el envío de mensajes definidos por la aplicación ( \_ pestaña WM, \_ escape ESC y WM \_ entrar).</span><span class="sxs-lookup"><span data-stu-id="e59ab-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="e59ab-121">**SubClassProc** usa la función [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) para pasar la mayoría de los mensajes al procedimiento de ventana original, *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="e59ab-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="e59ab-122">Procesar el mensaje de SETFOCUS de WM \_</span><span class="sxs-lookup"><span data-stu-id="e59ab-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="e59ab-123">Cuando la ventana de la barra de herramientas recibe el foco de entrada, establece inmediatamente el foco en el primer cuadro combinado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e59ab-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="e59ab-124">Para ello, el ejemplo llama a la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) en respuesta al mensaje [**de \_ SetFocus de WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="e59ab-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="e59ab-125">Procesar mensajes de Application-Defined</span><span class="sxs-lookup"><span data-stu-id="e59ab-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="e59ab-126">La función **SubClassProc** envía mensajes definidos por la aplicación a la ventana de la barra de herramientas cuando el usuario presiona la tecla Tab, entrar o Esc en un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e59ab-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="e59ab-127">El mensaje de la **\_ pestaña de WM** se envía para la tecla Tab, el mensaje **\_ ESC de WM** para la tecla ESC y el mensaje de **\_ entrada de WM** para la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="e59ab-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="e59ab-128">En el ejemplo se procesa el mensaje de la **\_ pestaña de WM** estableciendo el foco en el siguiente cuadro combinado de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e59ab-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="e59ab-129">Procesa el mensaje **de \_ ESC de WM** estableciendo el foco en la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e59ab-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



<span data-ttu-id="e59ab-130">En respuesta al mensaje **de \_ entrada de WM** , el ejemplo garantiza que la selección actual del cuadro combinado es válida y, a continuación, establece el foco en la ventana de la aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="e59ab-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="e59ab-131">Si el cuadro combinado no contiene ninguna selección actual, el ejemplo utiliza el mensaje [**CB \_ FindExactString con**](cb-findstringexact.md) para buscar un elemento de lista que coincida con el contenido del campo de selección.</span><span class="sxs-lookup"><span data-stu-id="e59ab-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="e59ab-132">Si hay una coincidencia, el ejemplo establece la selección actual; de lo contrario, agrega un nuevo elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="e59ab-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a><span data-ttu-id="e59ab-133">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="e59ab-133">Complete example</span></span>

<span data-ttu-id="e59ab-134">A continuación se muestran el procedimiento de ventana de la barra de herramientas y el procedimiento de subclase para los dos cuadros combinados.</span><span class="sxs-lookup"><span data-stu-id="e59ab-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="e59ab-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e59ab-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59ab-136">Acerca de los cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="e59ab-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="e59ab-137">Referencia de controles ComboBox</span><span class="sxs-lookup"><span data-stu-id="e59ab-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e59ab-138">Usar cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="e59ab-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="e59ab-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="e59ab-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 