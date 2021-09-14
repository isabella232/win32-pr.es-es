---
description: Aunque las funciones que se han analizado en el anterior funcionan bien para muchos lenguajes, es posible que no se acomenten a las necesidades de scripts complejos.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252626"
---
# <a name="complex-scripts"></a>Scripts complejos

Aunque las funciones que se han analizado en el anterior funcionan bien para muchos lenguajes, es posible que no se acomenten a las necesidades de scripts complejos. *Los scripts complejos* son lenguajes cuyo formato impreso no se representa de forma sencilla. Por ejemplo, un script complejo puede permitir la representación bidireccional, la forma contextual de glifos o la combinación de caracteres. Debido a estos requisitos especiales, el control de la salida de texto debe ser muy flexible.

Las funciones que muestran text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut,**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) [**TabbedTextOut,**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta) [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)y [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) se han ampliado para admitir scripts complejos. En general, esta compatibilidad es transparente para la aplicación. Sin embargo, las aplicaciones deben guardar caracteres en un búfer y mostrar una línea de texto completa a la vez, de modo que los módulos de modelado de scripts complejos puedan usar el contexto para reordenar y generar glifos correctamente. Además, dado que el ancho de un glifo puede variar según el contexto, las aplicaciones deben usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar la longitud de línea en lugar de usar anchos de caracteres almacenados en caché.

Además, las aplicaciones complejas compatibles con scripts deben considerar la posibilidad de agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación derecha a sus aplicaciones. Puede alternar el orden de lectura o la alineación entre izquierda y derecha con el código siguiente:


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



Para alternar ambos atributos a la vez, ejecute la siguiente instrucción y, a continuación, llame a [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) y [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), como se ha mostrado anteriormente:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



También puede procesar scripts complejos con Uniscribe. Uniscribe es un conjunto de funciones que permiten un cierto grado de control para scripts complejos. Para obtener más información, [vea Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).

 

 
