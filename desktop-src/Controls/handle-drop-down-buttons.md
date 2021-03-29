---
title: Cómo controlar botones desplegables
description: Un botón desplegable puede presentar a los usuarios una lista de opciones.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789352"
---
# <a name="how-to-handle-drop-down-buttons"></a>Cómo controlar botones desplegables

Un botón desplegable puede presentar a los usuarios una lista de opciones. Para crear este estilo de botón, especifique el estilo de [**\_ lista desplegable BTNS**](toolbar-control-and-button-styles.md) (también denominado [**\_ desplegable TBSTYLE**](toolbar-control-and-button-styles.md) para la compatibilidad con versiones anteriores de los controles comunes). Para mostrar un botón desplegable con una flecha, también debe establecer el estilo de la barra de herramientas [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) mediante el envío de un mensaje [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .

En la ilustración siguiente se muestra un botón "abrir" desplegable con el menú contextual abierto que muestra una lista de archivos. En este ejemplo, la barra de herramientas tiene el estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![captura de pantalla de un cuadro de diálogo con tres elementos de la barra de herramientas representados por iconos; uno tiene una flecha desplegable expandida y un menú contextual de tres elementos](images/tb-dropdown.png)

En la ilustración siguiente se muestra la misma barra de herramientas, esta vez sin el estilo [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![captura de pantalla de un cuadro de diálogo anterior, pero el icono con el menú contextual no tiene ninguna flecha de lista desplegable](images/tb-dropdown2.png)

Cuando los usuarios hacen clic en un botón de la barra de herramientas que usa el estilo [**\_ desplegable BTNS**](toolbar-control-and-button-styles.md) , el control de barra de herramientas envía a su ventana primaria un código de notificación [ \_ desplegable TBN](tbn-dropdown.md) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="handle-a-drop-down-button"></a>Controlar un botón desplegable

En el ejemplo de código siguiente se muestra cómo una aplicación puede admitir un botón desplegable en un control de barra de herramientas.


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




