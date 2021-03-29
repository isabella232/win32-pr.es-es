---
title: Cómo implementar la información sobre herramientas de varias líneas
description: La información sobre herramientas multilínea permite que el texto se muestre en más de una línea.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774197"
---
# <a name="how-to-implement-multiline-tooltips"></a>Cómo implementar la información sobre herramientas de varias líneas

La información sobre herramientas multilínea permite que el texto se muestre en más de una línea.

Son compatibles con la [versión 4,70](common-control-versions.md) y versiones posteriores de los controles comunes. La aplicación crea una información sobre herramientas de varias líneas mediante el envío de un mensaje de [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , que especifica el ancho del rectángulo de presentación. El texto que supera este ancho se ajusta a la línea siguiente en lugar de ensanchar la región de presentación. El alto del rectángulo aumenta según sea necesario para dar cabida a las líneas adicionales. El control ToolTip ajusta las líneas automáticamente, o puede utilizar una combinación de retorno de carro/avance de línea, \\ r \\ n, para forzar saltos de línea en ubicaciones concretas.

La presentación resultante se muestra en la siguiente ilustración.

![captura de pantalla de un cuadro de diálogo con información sobre herramientas que contiene texto organizado como un párrafo de varias líneas](images/tt-multiline.png)

> [!Note]  
> El búfer de texto especificado por el miembro **szText** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) solo puede contener 80 caracteres. Si necesita usar una cadena más larga, apunte el miembro **lpszText** de **NMTTDISPINFO** a un búfer que contenga el texto deseado.

 

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="implement-multiline-tooltips"></a>Implementar información sobre herramientas de varias líneas

El siguiente fragmento de código es un ejemplo de un controlador de notificación simple de [TTN \_ GETDISPINFO](ttn-getdispinfo.md) . Habilita una información sobre herramientas de varias líneas estableciendo el rectángulo de presentación en 150 píxeles. Se inserta un salto de línea manual después de la primera palabra para mostrar que los saltos de línea pueden ser difíciles y flexibles.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




