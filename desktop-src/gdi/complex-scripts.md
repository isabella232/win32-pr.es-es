---
description: Aunque las funciones descritas en el anterior funcionan bien para muchos idiomas, es posible que no se ocupen de las necesidades de los scripts complejos.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908507"
---
# <a name="complex-scripts"></a>Scripts complejos

Aunque las funciones descritas en el anterior funcionan bien para muchos idiomas, es posible que no se ocupen de las necesidades de los scripts complejos. Los *scripts complejos* son idiomas cuyo formulario impreso no se representa de una manera sencilla. Por ejemplo, un script complejo puede permitir la representación bidireccional, el modelado de glifos o la combinación de caracteres. Debido a estos requisitos especiales, el control de la salida de texto debe ser muy flexible.

Las funciones que muestran texto [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)y [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) se han ampliado para admitir scripts complejos. En general, esta compatibilidad es transparente para la aplicación. Sin embargo, las aplicaciones deben guardar los caracteres en un búfer y mostrar una línea de texto completa al mismo tiempo, de modo que los módulos complejos de modelado de scripts puedan usar el contexto para reordenar y generar los glifos correctamente. Además, dado que el ancho de un glifo puede variar según el contexto, las aplicaciones deben usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar la longitud de la línea en lugar de utilizar el ancho de caracteres en caché.

Además, las aplicaciones complejas basadas en scripts deben considerar la posibilidad de agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación derecha con sus aplicaciones. Puede alternar el orden de lectura o la alineación entre la izquierda y la derecha con el código siguiente:


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Para alternar ambos atributos a la vez, ejecute la siguiente instrucción y, a continuación, llame a [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) y [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), como se mostró anteriormente:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



También puede procesar scripts complejos con Uniscribe. Uniscribe es un conjunto de funciones que permiten un buen grado de control para los scripts complejos. Para obtener más información, [consulte la](../intl/uniscribe.md) información sobre el [procesamiento de scripts complejos](../intl/processing-complex-scripts.md).

 

 
