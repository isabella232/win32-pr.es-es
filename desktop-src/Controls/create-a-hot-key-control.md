---
title: Cómo crear un control de tecla de acceso rápido
description: En este tema se muestra cómo crear un control de tecla de acceso rápido. Puede crear un control de tecla de acceso rápido mediante la función CreateWindowEx, especificando la \_ clase de ventana de clase Hotkey.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904914"
---
# <a name="how-to-create-a-hot-key-control"></a>Cómo crear un control de tecla de acceso rápido

En este tema se muestra cómo crear un control de tecla de acceso rápido. Puede crear un control de tecla de acceso rápido mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la \_ clase de ventana de clase Hotkey.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Antes de crear el control de tecla de acceso rápido, asegúrese de que se carga el archivo DLL de controles comunes.

En el siguiente ejemplo de código de C++, la función definida por la aplicación llama a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para cargar el archivo dll de control común. A continuación, llama a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de **\_ clase Hotkey** , para crear un control de tecla de acceso rápido. Usa los mensajes [**HKM \_ SETRULES**](hkm-setrules.md) y [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) para inicializar el control y devuelve un identificador al control.

Este control de teclas de acceso rápido no permite al usuario elegir una tecla de acceso rápido que sea una sola clave no modificada, ni permite al usuario elegir solo el desplazamiento y una tecla. Estas reglas impiden de forma eficaz que el usuario elija una tecla de acceso rápido que se puede escribir accidentalmente mientras escribe texto.



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de teclas de acceso rápido](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Acerca de los controles de tecla de acceso rápido](hot-key-controls.md)
</dt> <dt>

[Usar controles de tecla de acceso rápido](using-hot-key-controls.md)
</dt> </dl>

 

 