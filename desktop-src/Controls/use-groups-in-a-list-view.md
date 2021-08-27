---
title: Uso de grupos en un List-View
description: En este tema se describe cómo crear una instancia de un grupo y agregarla a un control de vista de lista.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaad657d9ea6b71bac1d06a34a0aa29b99c26e204629e503a9e55531da162b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132125"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Uso de grupos en un List-View

En este tema se describe cómo crear una instancia de un grupo y agregarla a un control de vista de lista. La agrupación permite a un usuario organizar listas en grupos de elementos que se dividen visualmente en la página, mediante un divisor horizontal y un título de grupo.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Para usar grupos en un control de vista de lista, asegúrese de que el control incluye el estilo de [**ventana \_ LVS ALIGNTOP.**](list-view-window-styles.md)

Al agregar un elemento a la lista, se asigna a un grupo estableciendo el miembro **iGroupId** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) del elemento en el valor del miembro **iGroupId** de la estructura [**LVGROUP de**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) los grupos. Un elemento que no está asignado a un grupo no aparece en la lista cuando la vista de grupo está habilitada. Para habilitar o deshabilitar la vista de grupo, use la macro [**\_ EnableGroupView de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)

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

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usar List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 




