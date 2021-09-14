---
title: Cómo agregar un elemento a un control de encabezado
description: En este tema se muestra cómo agregar un elemento a un control de encabezado.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174293"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Cómo agregar un elemento a un control de encabezado

En este tema se muestra cómo agregar un elemento a un control de encabezado. Normalmente, un control de encabezado tiene varios elementos de encabezado que definen las columnas del control. Puede agregar un elemento a un control de encabezado enviando el [**mensaje \_ INSERTITEM de HDM**](hdm-insertitem.md) al control.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Use el [**mensaje \_ INSERTITEM de HDM**](hdm-insertitem.md) para agregar un elemento al control de encabezado. El mensaje debe incluir la dirección de una [**estructura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Esta estructura define las propiedades del elemento de encabezado, que puede incluir una cadena, una imagen de mapa de bits, un tamaño inicial y un valor de 32 bits definido por la aplicación.

En el ejemplo siguiente se muestra cómo usar el mensaje [**\_ INSERTITEM de HDM**](hdm-insertitem.md) y la [**estructura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) para agregar un elemento a un control de encabezado. El nuevo elemento consta de una cadena que se justifica a la izquierda dentro del rectángulo del elemento.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> <dt>

[Referencia de control de encabezado](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Usar controles de encabezado](using-header-controls.md)
</dt> </dl>

 

 




