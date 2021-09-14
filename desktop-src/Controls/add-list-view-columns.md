---
title: Adición de List-View columnas
description: En este tema se muestra cómo agregar columnas a un control list-view.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174294"
---
# <a name="how-to-add-list-view-columns"></a>Adición de List-View columnas

En este tema se muestra cómo agregar columnas a un control list-view. Las columnas se usan para mostrar los elementos y subelementos cuando un control de vista de lista está en la vista de informe (detalles). El texto de las columnas seleccionadas también se puede mostrar en la vista de mosaico.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para agregar una columna a un control de vista de lista, envíe el mensaje [**\_ LVM INSERTCOLUMN**](lvm-insertcolumn.md) o use la macro [**\_ ListView InsertColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) Para eliminar una columna, use el [**mensaje LVM \_ DELETECOLUMN.**](lvm-deletecolumn.md)

En el siguiente ejemplo de código de C++ se llama a la macro [**\_ ListView InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) para agregar columnas a un control de vista de lista. Los encabezados de columna se definen en el archivo de encabezado de la aplicación como recursos de cadena, que se numeran consecutivamente a partir de IDS \_ FIRSTCOLUMN. El número de columnas se define en el archivo de encabezado como **C \_ COLUMNS**.


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 




