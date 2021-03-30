---
description: Un script complejo es un script para el que el miembro fComplex de \_ las propiedades de script está establecido en true. En este tema se detallan las propiedades que puede tener un script complejo.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Acerca de los scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082935"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="9760e-104">Acerca de los scripts complejos</span><span class="sxs-lookup"><span data-stu-id="9760e-104">About Complex Scripts</span></span>

<span data-ttu-id="9760e-105">Un [script complejo](uniscribe-glossary.md) es un script para el que  el miembro fComplex [**de \_ las propiedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="9760e-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="9760e-106">En este tema se detallan las propiedades que puede tener un script complejo.</span><span class="sxs-lookup"><span data-stu-id="9760e-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="9760e-107">Representación bidireccional</span><span class="sxs-lookup"><span data-stu-id="9760e-107">Bidirectional Rendering</span></span>

<span data-ttu-id="9760e-108">La representación bidireccional es el tratamiento del texto que lee de izquierda a derecha y de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="9760e-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="9760e-109">Por ejemplo, en la representación bidireccional de árabe, la dirección de lectura predeterminada del texto es de derecha a izquierda, pero es de izquierda a derecha para algunos números.</span><span class="sxs-lookup"><span data-stu-id="9760e-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="9760e-110">El procesamiento de un script complejo debe tener en cuenta la diferencia entre el orden lógico de pulsación de teclas y el orden visual de los glifos.</span><span class="sxs-lookup"><span data-stu-id="9760e-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="9760e-111">Además, el procesamiento debe tratar correctamente el movimiento del símbolo de intercalación y la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="9760e-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="9760e-112">La asignación entre la posición de la pantalla y un índice de caracteres requiere la comprensión de los algoritmos de diseño de la pantalla determinada, por ejemplo, la selección de texto o la presentación del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="9760e-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="9760e-113">Modelado contextual</span><span class="sxs-lookup"><span data-stu-id="9760e-113">Contextual Shaping</span></span>

<span data-ttu-id="9760e-114">En el modelado contextual, los caracteres de script cambian de forma en función de los caracteres que los rodean.</span><span class="sxs-lookup"><span data-stu-id="9760e-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="9760e-115">Este tipo de modelado se produce en escritura cursiva en inglés cuando la forma "l" minúscula cambia según el carácter que lo precede, como una "a" (se conecta bajo a la "l") o una "o" (se conecta alto).</span><span class="sxs-lookup"><span data-stu-id="9760e-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="9760e-116">Por ejemplo, el árabe es un script que exhibe el modelado contextual.</span><span class="sxs-lookup"><span data-stu-id="9760e-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="9760e-117">Combinar caracteres</span><span class="sxs-lookup"><span data-stu-id="9760e-117">Combining Characters</span></span>

<span data-ttu-id="9760e-118">La combinación de caracteres, también denominados "ligaduras", son caracteres que se unen en un carácter cuando se colocan juntos.</span><span class="sxs-lookup"><span data-stu-id="9760e-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="9760e-119">Arabic es un script que tiene muchos caracteres combinables.</span><span class="sxs-lookup"><span data-stu-id="9760e-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="9760e-120">Un ejemplo del uso de caracteres de combinación es la "a" seguida de "combinación de acento grave", para la que la representación representada es "à".</span><span class="sxs-lookup"><span data-stu-id="9760e-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="9760e-121">La secuencia Unicode "U + 0061 U + 0300" requiere cierto procesamiento para asegurarse de que el "acento grave" está colocado correctamente encima de la "a".</span><span class="sxs-lookup"><span data-stu-id="9760e-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="9760e-122">Separación y justificación de palabras especializadas</span><span class="sxs-lookup"><span data-stu-id="9760e-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="9760e-123">Algunos scripts, por ejemplo, tailandés, tienen reglas complejas para dividir palabras entre líneas o para justificar texto en una línea.</span><span class="sxs-lookup"><span data-stu-id="9760e-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="9760e-124">Filtrar por combinaciones de caracteres no válidas</span><span class="sxs-lookup"><span data-stu-id="9760e-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="9760e-125">Un script complejo, por ejemplo, tailandés, puede filtrar las combinaciones de caracteres no válidas cuando un lenguaje no permite determinadas combinaciones de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9760e-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="9760e-126">Reserva de fuentes</span><span class="sxs-lookup"><span data-stu-id="9760e-126">Font Fallback</span></span>

<span data-ttu-id="9760e-127">La reserva de fuentes es la selección automatizada de una fuente distinta de la fuente seleccionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9760e-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="9760e-128">En Uniscribe, la función [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) aplica la reserva de fuentes cuando todo o parte del texto está en un script que no admite la fuente seleccionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9760e-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="9760e-129">Para obtener más información, vea [usar la reserva de fuentes](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="9760e-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9760e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9760e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9760e-131">Acerca de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="9760e-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



