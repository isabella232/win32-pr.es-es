---
title: Cómo implementar In-Place información sobre herramientas
description: La información sobre herramientas en contexto se usa para mostrar las cadenas de texto de los objetos que se han recortado. Para ver una ilustración, consulte Acerca de los controles de información sobre herramientas.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078630"
---
# <a name="how-to-implement-in-place-tooltips"></a>Cómo implementar In-Place información sobre herramientas

La información sobre herramientas en contexto se usa para mostrar las cadenas de texto de los objetos que se han recortado. Para ver una ilustración, consulte [acerca de los controles de información sobre herramientas](tooltip-controls.md).

La diferencia entre la información sobre herramientas normal y en contexto es el posicionamiento. De forma predeterminada, cuando el puntero del mouse se mantiene sobre una región que tiene una información sobre herramientas asociada, la información sobre herramientas se muestra junto a la región. Sin embargo, la información sobre herramientas es Windows y se pueden colocar en cualquier lugar que elija llamando a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Crear una información sobre herramientas en contexto es cuestión de colocar la ventana de información sobre herramientas para que se superponga la cadena de texto.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="positioning-an-in-place-tooltip"></a>Colocar una In-Place información sobre herramientas

Debe realizar un seguimiento de tres rectángulos al colocar una información sobre herramientas en contexto:

1.  Rectángulo que rodea el texto de etiqueta completo.
2.  Rectángulo que rodea el texto de la información sobre herramientas. El texto de la información sobre herramientas es idéntico al texto completo de la etiqueta y, normalmente, tiene el mismo tamaño y fuente. Los dos rectángulos de texto suelen tener el mismo tamaño.
3.  Rectángulo de la ventana de información sobre herramientas. Este rectángulo es algo más grande que el rectángulo de texto de información sobre herramientas que se incluye.


Los tres rectángulos se muestran esquemáticamente en la siguiente ilustración. La parte oculta del texto de la etiqueta se indica con un fondo gris.

![diagrama que muestra una cadena larga, la mitad de la cual tiene un fondo gris y, a continuación, la misma cadena dentro de un rectángulo más grande de la ventana de información sobre herramientas](images/inplace.png)

Para crear una información sobre herramientas en contexto, debe colocar el rectángulo de texto de información sobre herramientas para que se superponga el rectángulo de texto de la etiqueta. El procedimiento para alinear los dos rectángulos es relativamente sencillo:

1.  Defina el rectángulo de texto de la etiqueta.
2.  Coloca la ventana de información sobre herramientas para que el rectángulo del texto de información sobre herramientas se superponga al rectángulo de texto de la etiqueta.


En la práctica, normalmente es suficiente para alinear la esquina superior izquierda de los dos rectángulos de texto. Si intenta cambiar el tamaño del rectángulo de texto de información sobre herramientas para que coincida exactamente con el rectángulo de texto de la etiqueta, podrían producirse problemas con la presentación de la información sobre herramientas.

El problema con este esquema simple es que no se puede colocar el rectángulo de texto de información sobre herramientas directamente. En su lugar, debe colocar el rectángulo de la ventana de información sobre herramientas justo encima y a la izquierda del rectángulo de texto de la etiqueta para que las esquinas de los dos rectángulos de texto coincidan. En otras palabras, debe conocer el desplazamiento entre el rectángulo de la ventana de información sobre herramientas y su rectángulo de texto delimitado. En general, no hay ninguna forma sencilla de determinar este desplazamiento.

### <a name="implement-in-place-tooltips"></a>Implementar In-Place información sobre herramientas

En el fragmento de código siguiente se muestra cómo usar un mensaje [**\_ ADJUSTRECT de TTM**](ttm-adjustrect.md) en un controlador [TTN \_ Show](ttn-show.md) para mostrar una información sobre herramientas en contexto. La aplicación indica que el texto de la etiqueta se trunca estableciendo la variable Private *fMyStringIsTruncated* en **true**. El controlador llama a una función definida por la aplicación, **GetMyItemRect**, para recuperar el rectángulo de texto de la etiqueta. Este rectángulo se pasa al control ToolTip con **TTM \_ ADJUSTRECT**, que devuelve el rectángulo de ventana correspondiente. A continuación, se llama a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para colocar la información sobre herramientas sobre la etiqueta.


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



En este ejemplo no se cambia el tamaño de la información sobre herramientas, solo su posición. Los dos rectángulos de texto se alinean en las esquinas superior izquierda, pero no necesariamente con las mismas dimensiones. En la práctica, la diferencia suele ser pequeña y este enfoque se recomienda para la mayoría de los propósitos. Aunque puede, en principio, usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para cambiar el tamaño y cambiar la posición de la información sobre herramientas, puede tener consecuencias imprevisibles.

## <a name="remarks"></a>Observaciones

La [versión 5,80](common-control-versions.md) de los controles comunes simplifica el uso de la información sobre herramientas en contexto mediante la adición de un nuevo mensaje, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md). Envíe este mensaje con las coordenadas del rectángulo de texto de la etiqueta que desea que la información sobre herramientas se superponga y devuelva las coordenadas de un rectángulo de la ventana de información sobre herramientas colocado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 