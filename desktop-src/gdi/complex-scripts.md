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
# <a name="complex-scripts"></a><span data-ttu-id="a5214-103">Scripts complejos</span><span class="sxs-lookup"><span data-stu-id="a5214-103">Complex Scripts</span></span>

<span data-ttu-id="a5214-104">Aunque las funciones descritas en el anterior funcionan bien para muchos idiomas, es posible que no se ocupen de las necesidades de los scripts complejos.</span><span class="sxs-lookup"><span data-stu-id="a5214-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="a5214-105">Los *scripts complejos* son idiomas cuyo formulario impreso no se representa de una manera sencilla.</span><span class="sxs-lookup"><span data-stu-id="a5214-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="a5214-106">Por ejemplo, un script complejo puede permitir la representación bidireccional, el modelado de glifos o la combinación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a5214-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="a5214-107">Debido a estos requisitos especiales, el control de la salida de texto debe ser muy flexible.</span><span class="sxs-lookup"><span data-stu-id="a5214-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="a5214-108">Las funciones que muestran texto [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)y [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) se han ampliado para admitir scripts complejos.</span><span class="sxs-lookup"><span data-stu-id="a5214-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="a5214-109">En general, esta compatibilidad es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5214-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="a5214-110">Sin embargo, las aplicaciones deben guardar los caracteres en un búfer y mostrar una línea de texto completa al mismo tiempo, de modo que los módulos complejos de modelado de scripts puedan usar el contexto para reordenar y generar los glifos correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5214-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="a5214-111">Además, dado que el ancho de un glifo puede variar según el contexto, las aplicaciones deben usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar la longitud de la línea en lugar de utilizar el ancho de caracteres en caché.</span><span class="sxs-lookup"><span data-stu-id="a5214-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="a5214-112">Además, las aplicaciones complejas basadas en scripts deben considerar la posibilidad de agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación derecha con sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a5214-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="a5214-113">Puede alternar el orden de lectura o la alineación entre la izquierda y la derecha con el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5214-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


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



<span data-ttu-id="a5214-114">Para alternar ambos atributos a la vez, ejecute la siguiente instrucción y, a continuación, llame a [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) y [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), como se mostró anteriormente:</span><span class="sxs-lookup"><span data-stu-id="a5214-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="a5214-115">También puede procesar scripts complejos con Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="a5214-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="a5214-116">Uniscribe es un conjunto de funciones que permiten un buen grado de control para los scripts complejos.</span><span class="sxs-lookup"><span data-stu-id="a5214-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="a5214-117">Para obtener más información, [consulte la](../intl/uniscribe.md) información sobre el [procesamiento de scripts complejos](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="a5214-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
