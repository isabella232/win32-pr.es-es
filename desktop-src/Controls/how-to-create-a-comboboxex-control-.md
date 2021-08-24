---
title: Cómo crear un control ComboBoxEx
description: En este tema se muestra cómo crear un control ComboBoxEx.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d051c668e95667948d11a8ec86ed41236f84ff78325911e008c65ad787b958fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576135"
---
# <a name="how-to-create-a-comboboxex-control"></a>Cómo crear un control ComboBoxEx

En este tema se muestra cómo crear un control ComboBoxEx.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para crear un control ComboBoxEx, llame a la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) con [**WC \_ COMBOBOXEX como**](common-control-window-classes.md) clase de ventana. En primer lugar, debe registrar la clase de ventana llamando a la función [**InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) al tiempo que especifica el bit CLASES USEREX DE JAVA en la estructura \_ \_ [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que lo acompaña.

## <a name="complete-example"></a>Ejemplo completo

La siguiente función definida por la aplicación crea un control ComboBoxEx con el estilo DROPDOWN de [**CBS \_**](combo-box-styles.md) en la ventana principal.


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referencia del control ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usar controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 