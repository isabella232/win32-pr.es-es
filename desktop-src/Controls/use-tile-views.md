---
title: Uso de vistas de mosaico
description: En este tema se muestra cómo establecer la vista de mosaico para un control list-view.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d746bc74b816a6c14447a7f1e7d57a552bf1a08581cbcbba3e51f48a2143caab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132045"
---
# <a name="how-to-use-tile-views"></a>Uso de vistas de mosaico

En este tema se muestra cómo establecer la vista de mosaico para un control list-view. En la vista de mosaico, cada elemento se representa mediante un icono grande con una o varias líneas de texto adjunto. Para obtener una ilustración, vea [Acerca de List-View controles](list-view-controls-overview.md).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Establezca los parámetros de visualización generales para la vista de mosaico mediante la macro [**\_ ListView SetTileViewInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) Use la estructura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) que se pasa a esta macro para especificar la posición del texto en relación con el icono, el tamaño de cada icono (incluido el texto adjunto) y el número máximo de líneas de texto.

Si no desea que los iconos se ajusten automáticamente, debe establecer **LVTVIF \_ FIXEDSIZE** en el miembro **dwFlags** y **LVTVIM \_ TILESIZE** en el miembro **dwMask** de [**LVTILEVIEWINFO,**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)así como proporcionar las dimensiones en el **miembro sizeTile.**

En el ejemplo de código de C++ siguiente se establece la información de vista de mosaico para un control de vista de lista para que se muestre un máximo de dos subelementos para cada elemento. También establece el tamaño de cada icono.


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



Para cada elemento de la lista, puede establecer parámetros adicionales cuando el elemento se inserta en la lista o posterior. La [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que se usa con [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contiene miembros que especifican qué columnas de datos se mostrarán debajo del elemento y su alineación. Estos mismos parámetros de visualización también se encuentran en la [**estructura LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) usada con [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).

> [!Note]  
> "Columnas" aquí hace referencia no a mostrar columnas en la vista de mosaico, sino a subelementos, que se muestran en columnas en la vista de detalles.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Uso de List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 




