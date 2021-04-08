---
title: Cómo agregar List-View columnas
description: En este tema se muestra cómo agregar columnas a un control de vista de lista.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078621"
---
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="292b9-103">Cómo agregar List-View columnas</span><span class="sxs-lookup"><span data-stu-id="292b9-103">How to Add List-View Columns</span></span>

<span data-ttu-id="292b9-104">En este tema se muestra cómo agregar columnas a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="292b9-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="292b9-105">Las columnas se usan para mostrar los elementos y subelementos cuando un control de vista de lista está en la vista de informe (detalles).</span><span class="sxs-lookup"><span data-stu-id="292b9-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="292b9-106">El texto de las columnas seleccionadas también se puede mostrar en la vista en mosaico.</span><span class="sxs-lookup"><span data-stu-id="292b9-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="292b9-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="292b9-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="292b9-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="292b9-108">Technologies</span></span>

-   [<span data-ttu-id="292b9-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="292b9-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="292b9-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="292b9-110">Prerequisites</span></span>

-   <span data-ttu-id="292b9-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="292b9-111">C/C++</span></span>
-   <span data-ttu-id="292b9-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="292b9-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="292b9-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="292b9-113">Instructions</span></span>


<span data-ttu-id="292b9-114">Para agregar una columna a un control de vista de lista, envíe el mensaje [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) o use la macro [**ListView \_ INSERTCOLUMN**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="292b9-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="292b9-115">Para eliminar una columna, use el mensaje [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="292b9-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="292b9-116">En el siguiente ejemplo de código de C++ se llama a la macro [**\_ InsertColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) para agregar columnas a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="292b9-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="292b9-117">Los encabezados de columna se definen en el archivo de encabezado de la aplicación como recursos de cadena, que se numeran consecutivamente a partir de los IDENTIFICADOres \_ FIRSTCOLUMN.</span><span class="sxs-lookup"><span data-stu-id="292b9-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="292b9-118">El número de columnas se define en el archivo de encabezado **como \_ columnas de C**.</span><span class="sxs-lookup"><span data-stu-id="292b9-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="292b9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="292b9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="292b9-120">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="292b9-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="292b9-121">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="292b9-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="292b9-122">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="292b9-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




