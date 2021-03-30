---
title: Cómo usar grupos en un List-View
description: En este tema se describe cómo crear una instancia de un grupo y agregarla a un control de vista de lista.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904907"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="81391-103">Cómo usar grupos en un List-View</span><span class="sxs-lookup"><span data-stu-id="81391-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="81391-104">En este tema se describe cómo crear una instancia de un grupo y agregarla a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="81391-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="81391-105">La agrupación permite a un usuario organizar listas en grupos de elementos que se dividen visualmente en la página, mediante un divisor horizontal y un título de grupo.</span><span class="sxs-lookup"><span data-stu-id="81391-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="81391-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="81391-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="81391-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="81391-107">Technologies</span></span>

-   [<span data-ttu-id="81391-108">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="81391-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="81391-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="81391-109">Prerequisites</span></span>

-   <span data-ttu-id="81391-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="81391-110">C/C++</span></span>
-   <span data-ttu-id="81391-111">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="81391-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="81391-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="81391-112">Instructions</span></span>


<span data-ttu-id="81391-113">Para usar grupos en un control de vista de lista, asegúrese de que el control incluye el estilo de ventana de [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="81391-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="81391-114">Al agregar un elemento a la lista, se asigna a un grupo estableciendo el miembro **iGroupId** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento en el valor del miembro **iGroupId** de la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) de los grupos.</span><span class="sxs-lookup"><span data-stu-id="81391-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="81391-115">Un elemento que no está asignado a un grupo no aparece en la lista cuando la vista de grupo está habilitada.</span><span class="sxs-lookup"><span data-stu-id="81391-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="81391-116">Para habilitar o deshabilitar la vista de grupo, use la macro [**\_ EnableGroupView de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .</span><span class="sxs-lookup"><span data-stu-id="81391-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="81391-117">En el ejemplo siguiente se muestra cómo crear un grupo con un encabezado y agregarlo a un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="81391-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="81391-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81391-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81391-119">Referencia de control de vista de lista</span><span class="sxs-lookup"><span data-stu-id="81391-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="81391-120">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="81391-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="81391-121">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="81391-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




