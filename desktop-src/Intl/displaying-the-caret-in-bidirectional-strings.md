---
description: En texto unidireccional, la posición del símbolo de intercalación no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Mostrar el símbolo de intercalación en cadenas bidireccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653007"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="22915-103">Mostrar el símbolo de intercalación en cadenas bidireccionales</span><span class="sxs-lookup"><span data-stu-id="22915-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="22915-104">En texto unidireccional, la posición del símbolo de intercalación no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior.</span><span class="sxs-lookup"><span data-stu-id="22915-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="22915-105">Sin embargo, en texto bidireccional, la posición del símbolo de intercalación entre ejecuciones de dirección opuesta es ambigua.</span><span class="sxs-lookup"><span data-stu-id="22915-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="22915-106">Por ejemplo, en el párrafo de izquierda a derecha "hellosalaam", la última letra de "Hello" precede inmediatamente a la primera letra de "Salaam".</span><span class="sxs-lookup"><span data-stu-id="22915-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="22915-107">La mejor posición en la que se muestra el símbolo de intercalación depende de si se considera que sigue la "o" de "Hola" o antes de "s" de "Salaam".</span><span class="sxs-lookup"><span data-stu-id="22915-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="22915-108">Uniscribe utiliza las convenciones de posición del símbolo de intercalación que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="22915-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="22915-109">Situación</span><span class="sxs-lookup"><span data-stu-id="22915-109">Situation</span></span>       | <span data-ttu-id="22915-110">Selección de ubicación del símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="22915-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="22915-111">Escritura</span><span class="sxs-lookup"><span data-stu-id="22915-111">Typing</span></span>          | <span data-ttu-id="22915-112">Borde final del último carácter escrito.</span><span class="sxs-lookup"><span data-stu-id="22915-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="22915-113">Pegar</span><span class="sxs-lookup"><span data-stu-id="22915-113">Pasting</span></span>         | <span data-ttu-id="22915-114">Borde final del último carácter pegado.</span><span class="sxs-lookup"><span data-stu-id="22915-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="22915-115">Avance del símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="22915-115">Caret advancing</span></span> | <span data-ttu-id="22915-116">Borde final del último carácter pasado.</span><span class="sxs-lookup"><span data-stu-id="22915-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="22915-117">Retirado del símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="22915-117">Caret retiring</span></span>  | <span data-ttu-id="22915-118">Borde inicial del último carácter pasado.</span><span class="sxs-lookup"><span data-stu-id="22915-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="22915-119">Página principal</span><span class="sxs-lookup"><span data-stu-id="22915-119">Home</span></span>            | <span data-ttu-id="22915-120">Borde inicial de la línea.</span><span class="sxs-lookup"><span data-stu-id="22915-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="22915-121">End</span><span class="sxs-lookup"><span data-stu-id="22915-121">End</span></span>             | <span data-ttu-id="22915-122">Borde final de la línea.</span><span class="sxs-lookup"><span data-stu-id="22915-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="22915-123">El símbolo de intercalación se puede colocar tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="22915-123">The caret can be positioned as shown in the following example:</span></span>


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



<span data-ttu-id="22915-124">La posición del símbolo de intercalación puede ser más sencilla, como se muestra a continuación, dado un valor *fAdvancing* restringido a **true** o **false**:</span><span class="sxs-lookup"><span data-stu-id="22915-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="22915-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) controla las posiciones fuera del intervalo de forma lógica.</span><span class="sxs-lookup"><span data-stu-id="22915-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="22915-126">Devuelve el borde inicial de la ejecución de *iCharPos* <0, y el borde final de la ejecución de *iCharPos* >= length.</span><span class="sxs-lookup"><span data-stu-id="22915-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="22915-127">Para obtener más información, vea [administrar la colocación del símbolo de intercalación y la prueba de posicionamiento](managing-caret-placement-and-hit-testing.md) .</span><span class="sxs-lookup"><span data-stu-id="22915-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="22915-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22915-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22915-129">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="22915-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



