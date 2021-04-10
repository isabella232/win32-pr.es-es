---
title: Control de las notificaciones de BCN_DROPDOWN de SplitButtons
description: En este tema se describe una posible manera de responder a la \_ notificación de la lista desplegable BCN en un procedimiento de cuadro de diálogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149675"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Cómo controlar la \_ notificación de la lista desplegable BCN desde un botón de expansión

En este tema se describe una posible manera de responder a la notificación de la [ \_ lista desplegable BCN](bcn-dropdown.md) en un procedimiento de cuadro de diálogo.

La aplicación de C++ recupera las coordenadas de cliente del botón del encabezado de notificación y las convierte en coordenadas de pantalla. Después, crea un menú emergente y lo muestra en la parte inferior del botón. Para simplificar el ejemplo, los métodos abreviados de teclado no se implementan para el menú.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Paso 1: Espere a la notificación de la *\_ lista desplegable BCN* .


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Paso 2: obtener las coordenadas de pantalla del botón.

Use la función [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) para convertir las coordenadas de la ventana del borde izquierdo inferior del botón en coordenadas de pantalla.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Paso 3: crear un menú y agregar elementos.

Utilice la función [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) para crear un menú. Utilice la función [**AppendMenu**](/windows/desktop/menurc/u) para agregar elementos al menú. IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 son constantes definidas por la aplicación para los comandos de menú.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Paso 4: mostrar el menú.

La función [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) muestra un menú contextual en la ubicación especificada y realiza un seguimiento de la selección de elementos en el menú.


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

[\_Código de notificación de desplegable BCN](bcn-dropdown.md)
</dt> <dt>

[Acerca de los botones](about-buttons.md)
</dt> <dt>

[Referencia de control de botón](bumper-button-button-control-reference.md)
</dt> <dt>

[Usar botones](using-buttons.md)
</dt> <dt>

[Botón](buttons.md)
</dt> </dl>

 

 