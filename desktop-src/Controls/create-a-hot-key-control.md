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
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="190b7-104">Cómo crear un control de tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="190b7-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="190b7-105">En este tema se muestra cómo crear un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="190b7-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="190b7-106">Puede crear un control de tecla de acceso rápido mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la \_ clase de ventana de clase Hotkey.</span><span class="sxs-lookup"><span data-stu-id="190b7-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="190b7-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="190b7-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="190b7-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="190b7-108">Technologies</span></span>

-   [<span data-ttu-id="190b7-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="190b7-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="190b7-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="190b7-110">Prerequisites</span></span>

-   <span data-ttu-id="190b7-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="190b7-111">C/C++</span></span>
-   <span data-ttu-id="190b7-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="190b7-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="190b7-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="190b7-113">Instructions</span></span>


<span data-ttu-id="190b7-114">Antes de crear el control de tecla de acceso rápido, asegúrese de que se carga el archivo DLL de controles comunes.</span><span class="sxs-lookup"><span data-stu-id="190b7-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="190b7-115">En el siguiente ejemplo de código de C++, la función definida por la aplicación llama a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para cargar el archivo dll de control común.</span><span class="sxs-lookup"><span data-stu-id="190b7-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="190b7-116">A continuación, llama a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de **\_ clase Hotkey** , para crear un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="190b7-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="190b7-117">Usa los mensajes [**HKM \_ SETRULES**](hkm-setrules.md) y [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) para inicializar el control y devuelve un identificador al control.</span><span class="sxs-lookup"><span data-stu-id="190b7-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="190b7-118">Este control de teclas de acceso rápido no permite al usuario elegir una tecla de acceso rápido que sea una sola clave no modificada, ni permite al usuario elegir solo el desplazamiento y una tecla.</span><span class="sxs-lookup"><span data-stu-id="190b7-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="190b7-119">Estas reglas impiden de forma eficaz que el usuario elija una tecla de acceso rápido que se puede escribir accidentalmente mientras escribe texto.</span><span class="sxs-lookup"><span data-stu-id="190b7-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="190b7-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="190b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190b7-121">Referencia de control de teclas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="190b7-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="190b7-122">Acerca de los controles de tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="190b7-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="190b7-123">Usar controles de tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="190b7-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 