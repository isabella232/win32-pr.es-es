---
title: Cómo controlar los botones desplegables
description: Un botón desplegable puede presentar a los usuarios una lista de opciones.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062009"
---
# <a name="how-to-handle-drop-down-buttons"></a>Cómo controlar los botones desplegables

Un botón desplegable puede presentar a los usuarios una lista de opciones. Para crear este estilo de botón, especifique el estilo [**\_ BTNS DROPDOWN**](toolbar-control-and-button-styles.md) (también denominado [**TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md) por compatibilidad con versiones anteriores de los controles comunes). Para mostrar un botón desplegable con una flecha, también debe establecer el estilo de barra de herramientas [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) enviando un mensaje [**TB \_ SETEXTENDEDSTYLE.**](tb-setextendedstyle.md)

En la ilustración siguiente se muestra un botón desplegable "Abrir" con el menú contextual abierto y una lista de archivos. En este ejemplo, la barra de herramientas tiene el [**estilo TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![captura de pantalla de un cuadro de diálogo con tres elementos de la barra de herramientas representados por iconos; tiene una flecha desplegable expandida y un menú contextual de tres elementos.](images/tb-dropdown.png)

En la ilustración siguiente se muestra la misma barra de herramientas, esta vez sin el estilo [**TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![captura de pantalla de un cuadro de diálogo anterior, pero el icono con el menú contextual no tiene ninguna flecha desplegable](images/tb-dropdown2.png)

Cuando los usuarios hacen clic en un botón de barra de herramientas que usa el estilo [**\_ DESPLEGABLE de BTNS,**](toolbar-control-and-button-styles.md) el control de barra de herramientas envía a su ventana primaria un código de notificación DE LISTA DESPLEGABLE de [TBN. \_](tbn-dropdown.md)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="handle-a-drop-down-button"></a>Control de un botón desplegable

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

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




