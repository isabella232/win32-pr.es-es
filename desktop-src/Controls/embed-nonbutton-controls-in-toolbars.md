---
title: Cómo insertar controles que no son de botón en las barras de herramientas
description: Las barras de herramientas solo admiten botones; Por lo tanto, si la aplicación requiere otro tipo de control, debe crear una ventana secundaria. En la ilustración siguiente se muestra una barra de herramientas con un control de edición incrustado.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be124fd0759005344bab3338465b3e86f1b8afbded62755171be87a5a01682c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697424"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Cómo insertar controles que no son de botón en las barras de herramientas

Las barras de herramientas solo admiten botones; Por lo tanto, si la aplicación requiere otro tipo de control, debe crear una ventana secundaria. En la ilustración siguiente se muestra una barra de herramientas con un control de edición incrustado.

![captura de pantalla de un cuadro de diálogo con un control de edición en la barra de herramientas, antes de tres iconos de barra de herramientas](images/tb-withedit.png)

> [!Note]  
> Considere la posibilidad [de usar controles Rebar en](rebar-controls.md) lugar de colocar controles en las barras de herramientas.

 

Cualquier tipo de ventana se puede colocar en una barra de herramientas. El código de ejemplo siguiente agrega un control de edición como elemento secundario de la ventana de control de la barra de herramientas. Dado que se crea la barra de herramientas y, a continuación, se agrega el control de edición, debe proporcionar espacio para el control de edición. Una manera de hacerlo es agregar un separador como marcador de posición en la barra de herramientas, estableciendo el ancho del separador en el número de píxeles que desea reservar.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Insertar un control nonbutton en una barra de herramientas

El siguiente fragmento de código crea la barra de herramientas en la ilustración anterior.


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



En este ejemplo se codifican de forma hard las dimensiones de la ventana secundaria; sin embargo, para crear una aplicación más sólida, determine el tamaño de la barra de herramientas y haga que la ventana de control de edición quepa.

Es posible que quiera que las notificaciones de control de edición vayan a otra ventana, como el elemento primario de la barra de herramientas. Para ello, cree el control de edición como elemento secundario de la ventana primaria de la barra de herramientas. A continuación, cambie el elemento primario del control de edición a la barra de herramientas como se muestra a continuación.


```
SetParent (hWndEdit, hWndToolbar);
```



Las notificaciones van al elemento primario original. Por lo tanto, los mensajes de control de edición van al elemento primario de la barra de herramientas aunque la ventana de edición resida en la ventana de la barra de herramientas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de barra de herramientas](using-toolbar-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




