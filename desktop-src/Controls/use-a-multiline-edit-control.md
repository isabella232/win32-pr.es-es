---
title: Cómo crear un control de edición multilínea
description: En este tema se muestra cómo implementar un procesador de textos sencillo agregando un control de edición multilínea al área cliente de una ventana.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995746"
---
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="549cf-103">Cómo crear un control de edición multilínea</span><span class="sxs-lookup"><span data-stu-id="549cf-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="549cf-104">En este tema se muestra cómo implementar un procesador de textos sencillo agregando un control de edición multilínea al área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="549cf-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="549cf-105">Mediante el control de edición de varias líneas, el usuario puede seleccionar Editar comandos de un menú.</span><span class="sxs-lookup"><span data-stu-id="549cf-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="549cf-106">Estos comandos permiten al usuario realizar operaciones de edición sencillas, como deshacer una acción anterior, cortar o copiar selecciones en el portapapeles, pegar texto del portapapeles y eliminar la selección actual.</span><span class="sxs-lookup"><span data-stu-id="549cf-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="549cf-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="549cf-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="549cf-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="549cf-108">Technologies</span></span>

-   [<span data-ttu-id="549cf-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="549cf-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="549cf-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="549cf-110">Prerequisites</span></span>

-   <span data-ttu-id="549cf-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="549cf-111">C/C++</span></span>
-   <span data-ttu-id="549cf-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="549cf-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="549cf-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="549cf-113">Instructions</span></span>


<span data-ttu-id="549cf-114">La aplicación debe incluir código para crear una instancia de e inicializar un control de edición de varias líneas y, a continuación, procesar los comandos de edición del usuario.</span><span class="sxs-lookup"><span data-stu-id="549cf-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="549cf-115">En el siguiente ejemplo de código de C++ se implementa gran parte de la funcionalidad de un procesador de textos sencillo agregando un control de edición multilínea al área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="549cf-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="549cf-116">El sistema realiza automáticamente operaciones de ajuste de líneas para el control de edición y controla también el procesamiento de la barra de desplazamiento vertical (que se crea especificando [**es \_ AUTOVSCROLL**](edit-control-styles.md) en la llamada a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).</span><span class="sxs-lookup"><span data-stu-id="549cf-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="549cf-117">Los comandos de edición de usuario se envían al proceso de ventana a través de mensajes de notificación de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="549cf-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="549cf-118">Si la ventana incluye la cinta de opciones de Windows, se debe ajustar el tamaño del control de edición para acomodar el alto de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="549cf-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="549cf-119">Para obtener más información, vea [marco de cinta de Windows](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span><span class="sxs-lookup"><span data-stu-id="549cf-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a><span data-ttu-id="549cf-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="549cf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="549cf-121">Acerca de los controles de edición</span><span class="sxs-lookup"><span data-stu-id="549cf-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="549cf-122">Editar referencia de control</span><span class="sxs-lookup"><span data-stu-id="549cf-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="549cf-123">Usar controles de edición</span><span class="sxs-lookup"><span data-stu-id="549cf-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="549cf-124">Control de edición</span><span class="sxs-lookup"><span data-stu-id="549cf-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 