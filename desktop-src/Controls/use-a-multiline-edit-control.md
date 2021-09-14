---
title: Cómo crear un control de edición multilínea
description: En este tema se muestra cómo implementar un procesador de palabras simple agregando un control de edición multilínea al área cliente de una ventana.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165437"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Cómo crear un control de edición multilínea

En este tema se muestra cómo implementar un procesador de palabras simple agregando un control de edición multilínea al área cliente de una ventana. Mediante el control de edición multilínea, el usuario puede seleccionar los comandos de edición en un menú. Estos comandos permiten al usuario realizar operaciones de edición sencillas, como deshacer una acción anterior, cortar o copiar selecciones en el Portapapeles, pegar texto del Portapapeles y eliminar la selección actual.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


La aplicación debe incluir código para crear una instancia de e inicializar un control de edición multilínea y, a continuación, procesar los comandos de edición del usuario.

El siguiente ejemplo de código de C++ implementa gran parte de la funcionalidad de un procesador de palabras simple agregando un control de edición multilínea al área cliente de una ventana. El sistema realiza automáticamente operaciones de ajuste de palabras para el control de edición y también controla el procesamiento de la barra de desplazamiento vertical (creada especificando [**ES \_ AUTOVSCROLL**](edit-control-styles.md) en la llamada a la [**función CreateWindow).**](/windows/desktop/api/winuser/nf-winuser-createwindowa)

Los comandos de edición de usuario se envían al proceso de ventana a través [**de mensajes de notificación DE WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)

> [!Note]  
> Si la ventana incluye la Windows, el tamaño del control de edición debe ajustarse para adaptarse al alto de la cinta de opciones. Para obtener más información, [vea Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).

 



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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de editar controles](about-edit-controls.md)
</dt> <dt>

[Editar referencia de control](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Usar controles de edición](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Editar control](edit-controls.md)
</dt> </dl>

 

 