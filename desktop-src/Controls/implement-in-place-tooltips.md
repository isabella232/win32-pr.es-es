---
title: Cómo implementar información sobre herramientas In-Place datos
description: La información sobre herramientas local se usa para mostrar cadenas de texto para los objetos que se han recortado. Para obtener una ilustración, vea Acerca de los controles de información sobre herramientas.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd3b01d30a20b52cbb80121cc8c1d793965acf0ea3cf4f2be1ce4553f4ccb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671738"
---
# <a name="how-to-implement-in-place-tooltips"></a>Cómo implementar información sobre herramientas In-Place datos

La información sobre herramientas local se usa para mostrar cadenas de texto para los objetos que se han recortado. Para obtener una ilustración, vea [Acerca de los controles de información sobre herramientas](tooltip-controls.md).

La diferencia entre la información sobre herramientas normal y local es el posicionamiento. De forma predeterminada, cuando el puntero del mouse mantiene el puntero sobre una región que tiene una información sobre herramientas asociada, la información sobre herramientas se muestra adyacente a la región. Sin embargo, la información sobre herramientas son ventanas y se pueden colocar en cualquier lugar que elija mediante una llamada [**a SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). La creación de información sobre herramientas local es cuestión de colocar la ventana de información sobre herramientas para que superponga la cadena de texto.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="positioning-an-in-place-tooltip"></a>Colocación de una información In-Place datos

Debe realizar un seguimiento de tres rectángulos al colocar una información sobre herramientas local:

1.  Rectángulo que rodea el texto completo de la etiqueta.
2.  Rectángulo que rodea el texto de la información sobre herramientas. El texto de la información sobre herramientas es idéntico al texto completo de la etiqueta y normalmente tiene el mismo tamaño y fuente. Por lo tanto, los dos rectángulos de texto normalmente tendrán el mismo tamaño.
3.  Rectángulo de la ventana de información sobre herramientas. Este rectángulo es algo mayor que el rectángulo de texto de información sobre herramientas que incluye.


Los tres rectángulos se muestran esquemáticamente en la ilustración siguiente. La parte oculta del texto de la etiqueta se indica mediante un fondo gris.

![diagrama que muestra una cadena larga, la mitad de la cual tiene un fondo gris y, a continuación, la misma cadena dentro de un rectángulo de ventana de información sobre herramientas más grande](images/inplace.png)

Para crear una información sobre herramientas local, debe colocar el rectángulo de texto de la información sobre herramientas para que superponga el rectángulo de texto de la etiqueta. El procedimiento para alinear los dos rectángulos es relativamente sencillo:

1.  Defina el rectángulo de texto de la etiqueta.
2.  Coloque la ventana de información sobre herramientas para que el rectángulo de texto de la información sobre herramientas superponga el rectángulo de texto de la etiqueta.


En la práctica, normalmente es suficiente para alinear la esquina superior izquierda de los dos rectángulos de texto. Si intenta cambiar el tamaño del rectángulo de texto de información sobre herramientas para que coincida exactamente con el rectángulo de texto de la etiqueta, podría producir problemas con la presentación de la información sobre herramientas.

El problema con este esquema simple es que no se puede colocar directamente el rectángulo de texto de la información sobre herramientas. En su lugar, debe colocar el rectángulo de la ventana de información sobre herramientas lo suficientemente arriba como a la izquierda del rectángulo de texto de etiqueta para que las esquinas de los dos rectángulos de texto coincidan. En otras palabras, debe conocer el desplazamiento entre el rectángulo de la ventana de información sobre herramientas y su rectángulo de texto delimitado. En general, no hay ninguna manera sencilla de determinar este desplazamiento.

### <a name="implement-in-place-tooltips"></a>Implementación de In-Place información sobre herramientas

En el fragmento de código siguiente se muestra cómo usar un mensaje [**\_ ADJUSTRECT de TTM**](ttm-adjustrect.md) en un controlador [TTN \_ SHOW](ttn-show.md) para mostrar una información sobre herramientas local. La aplicación indica que el texto de la etiqueta se trunca estableciendo la variable *privada fMyStringIsTruncated* en **TRUE.** El controlador llama a una función definida por la aplicación, **GetMyItemRect**, para recuperar el rectángulo de texto de la etiqueta. Este rectángulo se pasa al control de información sobre herramientas **con \_ ADJUSTRECT de TTM,** que devuelve el rectángulo de ventana correspondiente. [**A continuación,**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) se llama a SetWindowPos para colocar la información sobre herramientas sobre la etiqueta.


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



Este ejemplo no cambia el tamaño de la información sobre herramientas, solo su posición. Los dos rectángulos de texto se alinean en sus esquinas superior izquierda, pero no necesariamente con las mismas dimensiones. En la práctica, la diferencia suele ser pequeña y este enfoque se recomienda para la mayoría de los propósitos. Aunque, en principio, puede usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para cambiar el tamaño, así como cambiar la posición de la información sobre herramientas, esto podría tener consecuencias imprevisibles.

## <a name="remarks"></a>Observaciones

La versión [5.80](common-control-versions.md) de los controles comunes simplifica el uso de información sobre herramientas local mediante la adición de un nuevo mensaje, [**EL AJUSTE DE AJUSTE DE LA ZONA \_ ESTÁNDAR**](ttm-adjustrect.md). Envíe este mensaje con las coordenadas del rectángulo de texto de etiqueta que desea que la información sobre herramientas se superponga y devuelve las coordenadas de un rectángulo de ventana de información sobre herramientas situado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 