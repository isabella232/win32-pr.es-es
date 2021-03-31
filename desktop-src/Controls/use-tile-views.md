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
# <a name="how-to-use-tile-views"></a>Cómo usar vistas en mosaico

En este tema se muestra cómo establecer la vista de mosaico para un control de vista de lista. En la vista de mosaico, cada elemento se representa mediante un icono grande con una o más líneas de texto adjunto. Para ver una ilustración, consulte [acerca de los controles de List-View](list-view-controls-overview.md).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Establezca los parámetros de presentación generales para la vista de mosaico mediante la macro [**\_ SetTileViewInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) . Use la estructura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) que se pasa a esta macro para especificar la posición del texto en relación con el icono, el tamaño de cada mosaico (incluido el texto adjunto) y el número máximo de líneas de texto.

Si no quiere que se ajuste el tamaño de los mosaicos automáticamente, debe establecer **LVTVIF \_ FIXEDSIZE** en el miembro **dwFlags** y LVTVIM en el miembro **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), así como proporcionar las dimensiones en el miembro **\_** **sizeTile** .

En el siguiente ejemplo de código de C++ se establece la información de la vista de mosaico para un control de vista de lista de modo que se muestre un máximo de dos subelementos para cada elemento. También establece el tamaño de cada mosaico.


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



Para cada elemento de la lista, puede establecer más parámetros cuando se inserte el elemento en la lista, o posteriormente. La estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que se usa con [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contiene miembros que especifican las columnas de datos que se van a mostrar debajo del elemento y su alineación. Estos mismos parámetros de presentación también se encuentran en la estructura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) utilizada con [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).

> [!Note]  
> "Columnas" aquí hace referencia no mostrar las columnas en la vista de mosaico sino en los subelementos, que se muestran en las columnas en la vista de detalles.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de vista de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> <dt>

[Usar controles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




