---
title: Controlar BCN_DROPDOWN notificaciones desde SplitButtons
description: En este tema se describe una posible manera de responder a la notificación DROPDOWN de BCN \_ en un procedimiento de diálogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062001"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Cómo controlar la notificación DESPLEGABLE de BCN \_ desde un botón de división

En este tema se describe una posible manera de responder a la notificación DROPDOWN de [BCN \_ ](bcn-dropdown.md) en un procedimiento de diálogo.

La aplicación de C++ recupera las coordenadas de cliente del botón del encabezado de notificación y las convierte en coordenadas de pantalla. A continuación, crea un menú emergente y lo muestra en la parte inferior del botón. Para que el ejemplo sea sencillo, los métodos abreviados de teclado no se implementan para el menú.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Paso 1: Esperar la notificación *DESPLEGABLE \_ de BCN.*


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Paso 2: Obtener las coordenadas de pantalla del botón.

Use la [**función ClientToScreen para**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) convertir las coordenadas de ventana del borde inferior izquierdo del botón en coordenadas de pantalla.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Paso 3: Crear un menú y agregar elementos.

Use la [**función CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) para crear un menú. Use la [**función AppendMenu**](/windows/desktop/menurc/u) para agregar elementos al menú. IDC \_ MENUCOMMAND1 e IDC MENUCOMMAND2 son constantes definidas por la aplicación \_ para los comandos de menú.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Paso 4: Mostrar el menú.

La [**función TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) muestra un menú contextual en la ubicación especificada y realiza un seguimiento de la selección de elementos en el menú.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Ejemplo completo


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de notificación DESPLEGABLE de BCN \_](bcn-dropdown.md)
</dt> <dt>

[Acerca de los botones](about-buttons.md)
</dt> <dt>

[Referencia de control de botón](bumper-button-button-control-reference.md)
</dt> <dt>

[Usar botones](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 