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
# <a name="how-to-use-groups-in-a-list-view"></a>Cómo usar grupos en un List-View

En este tema se describe cómo crear una instancia de un grupo y agregarla a un control de vista de lista. La agrupación permite a un usuario organizar listas en grupos de elementos que se dividen visualmente en la página, mediante un divisor horizontal y un título de grupo.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Para usar grupos en un control de vista de lista, asegúrese de que el control incluye el estilo de ventana de [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .

Al agregar un elemento a la lista, se asigna a un grupo estableciendo el miembro **iGroupId** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento en el valor del miembro **iGroupId** de la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) de los grupos. Un elemento que no está asignado a un grupo no aparece en la lista cuando la vista de grupo está habilitada. Para habilitar o deshabilitar la vista de grupo, use la macro [**\_ EnableGroupView de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .

En el ejemplo siguiente se muestra cómo crear un grupo con un encabezado y agregarlo a un control de vista de lista.


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de vista de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




