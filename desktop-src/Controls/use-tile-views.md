---
title: Cómo usar vistas en mosaico
description: En este tema se muestra cómo establecer la vista de mosaico para un control de vista de lista.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995744"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="13cf3-103">Cómo usar vistas en mosaico</span><span class="sxs-lookup"><span data-stu-id="13cf3-103">How to Use Tile Views</span></span>

<span data-ttu-id="13cf3-104">En este tema se muestra cómo establecer la vista de mosaico para un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="13cf3-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="13cf3-105">En la vista de mosaico, cada elemento se representa mediante un icono grande con una o más líneas de texto adjunto.</span><span class="sxs-lookup"><span data-stu-id="13cf3-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="13cf3-106">Para ver una ilustración, consulte [acerca de los controles de List-View](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="13cf3-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="13cf3-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="13cf3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="13cf3-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="13cf3-108">Technologies</span></span>

-   [<span data-ttu-id="13cf3-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="13cf3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="13cf3-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13cf3-110">Prerequisites</span></span>

-   <span data-ttu-id="13cf3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="13cf3-111">C/C++</span></span>
-   <span data-ttu-id="13cf3-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="13cf3-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="13cf3-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="13cf3-113">Instructions</span></span>


<span data-ttu-id="13cf3-114">Establezca los parámetros de presentación generales para la vista de mosaico mediante la macro [**\_ SetTileViewInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) .</span><span class="sxs-lookup"><span data-stu-id="13cf3-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="13cf3-115">Use la estructura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) que se pasa a esta macro para especificar la posición del texto en relación con el icono, el tamaño de cada mosaico (incluido el texto adjunto) y el número máximo de líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="13cf3-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="13cf3-116">Si no quiere que se ajuste el tamaño de los mosaicos automáticamente, debe establecer **LVTVIF \_ FIXEDSIZE** en el miembro **dwFlags** y LVTVIM en el miembro **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), así como proporcionar las dimensiones en el miembro **\_** **sizeTile** .</span><span class="sxs-lookup"><span data-stu-id="13cf3-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="13cf3-117">En el siguiente ejemplo de código de C++ se establece la información de la vista de mosaico para un control de vista de lista de modo que se muestre un máximo de dos subelementos para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="13cf3-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="13cf3-118">También establece el tamaño de cada mosaico.</span><span class="sxs-lookup"><span data-stu-id="13cf3-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="13cf3-119">Para cada elemento de la lista, puede establecer más parámetros cuando se inserte el elemento en la lista, o posteriormente.</span><span class="sxs-lookup"><span data-stu-id="13cf3-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="13cf3-120">La estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que se usa con [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contiene miembros que especifican las columnas de datos que se van a mostrar debajo del elemento y su alineación.</span><span class="sxs-lookup"><span data-stu-id="13cf3-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="13cf3-121">Estos mismos parámetros de presentación también se encuentran en la estructura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) utilizada con [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span><span class="sxs-lookup"><span data-stu-id="13cf3-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="13cf3-122">"Columnas" aquí hace referencia no mostrar las columnas en la vista de mosaico sino en los subelementos, que se muestran en las columnas en la vista de detalles.</span><span class="sxs-lookup"><span data-stu-id="13cf3-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="13cf3-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13cf3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cf3-124">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="13cf3-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="13cf3-125">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="13cf3-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="13cf3-126">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="13cf3-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




