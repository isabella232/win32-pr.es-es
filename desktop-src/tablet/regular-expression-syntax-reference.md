---
description: Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que comprenden algunos de los reconocedores de escritura a mano de Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referencia de sintaxis de expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279739"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="0a168-103">Referencia de sintaxis de expresiones regulares</span><span class="sxs-lookup"><span data-stu-id="0a168-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="0a168-104">Puede definir y asignar ámbitos de entrada personalizados mediante la sintaxis de expresiones regulares de escritura a mano que comprenden algunos de los reconocedores de escritura a mano de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a168-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="0a168-105">La sintaxis es un subconjunto de la [implementación del lenguaje de expresiones regulares](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0a168-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="0a168-106">Hay algunas diferencias en la forma en que se usan las expresiones regulares de escritura a mano y en la forma en que se usan los otros tipos de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="0a168-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="0a168-107">La sintaxis de escritura a mano se usa para especificar una cadena exacta que coincidirá con el motor de reconocimiento y no con una subcadena.</span><span class="sxs-lookup"><span data-stu-id="0a168-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="0a168-108">Por ejemplo, las expresiones regulares s ( \[ a-z \] +) p devolverán coincidencias para "sopa", "STOP", "inStep" y "esophagus".</span><span class="sxs-lookup"><span data-stu-id="0a168-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="0a168-109">Mientras que una expresión regular de escritura a mano equivalente, como s (! IS \_ ONECHAR) + p, coincidiría con "sopa" y "STOP", pero no con "inStep" y "esophagus".</span><span class="sxs-lookup"><span data-stu-id="0a168-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="0a168-110">Las expresiones regulares de escritura a mano no admiten espacios de no separación dentro de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="0a168-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="0a168-111">Es decir, no puede usar la entidad "nbsp" dentro de una expresión regular de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="0a168-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="0a168-112">En las secciones siguientes se describe la sintaxis con más detalle.</span><span class="sxs-lookup"><span data-stu-id="0a168-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="0a168-113">Operadores válidos</span><span class="sxs-lookup"><span data-stu-id="0a168-113">Valid Operators</span></span>

<span data-ttu-id="0a168-114">Los operadores siguientes son válidos para crear expresiones regulares para definir ámbitos de entrada para reconocedores de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="0a168-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="0a168-115">Operator</span><span class="sxs-lookup"><span data-stu-id="0a168-115">Operator</span></span>      | <span data-ttu-id="0a168-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a168-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="0a168-117">Operador unario de postfijo que indica cero o más repeticiones del operando.</span><span class="sxs-lookup"><span data-stu-id="0a168-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="0a168-118">Operador unario postfijo que indica una o más repeticiones del operando.</span><span class="sxs-lookup"><span data-stu-id="0a168-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="0a168-119">?</span><span class="sxs-lookup"><span data-stu-id="0a168-119">?</span></span><br/>  | <span data-ttu-id="0a168-120">Operador unario de postfijo que indica cero o una repetición del operando.</span><span class="sxs-lookup"><span data-stu-id="0a168-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="0a168-121">Significado del operador binario de infijo "or".</span><span class="sxs-lookup"><span data-stu-id="0a168-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="0a168-122">()</span><span class="sxs-lookup"><span data-stu-id="0a168-122">()</span></span><br/> | <span data-ttu-id="0a168-123">Se utiliza para agrupar elementos.</span><span class="sxs-lookup"><span data-stu-id="0a168-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="0a168-124">La implementación de Microsoft de expresiones regulares para reconocedores de escritura a mano permite aplicaciones repetidas de operadores unarios de postfijo.</span><span class="sxs-lookup"><span data-stu-id="0a168-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="0a168-125">Por ejemplo, a \* \* = (a \* ) \* = a \* , b??</span><span class="sxs-lookup"><span data-stu-id="0a168-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="0a168-126">= (b?)?</span><span class="sxs-lookup"><span data-stu-id="0a168-126">= (b?)?</span></span> <span data-ttu-id="0a168-127">= b?.</span><span class="sxs-lookup"><span data-stu-id="0a168-127">= b?.</span></span> <span data-ttu-id="0a168-128">También permiten repeticiones no consecutivas, por ejemplo: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* .</span><span class="sxs-lookup"><span data-stu-id="0a168-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="0a168-129">Esto es diferente de .NET Framework expresiones regulares, que solo permiten el?</span><span class="sxs-lookup"><span data-stu-id="0a168-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="0a168-130">operador que se va a repetir.</span><span class="sxs-lookup"><span data-stu-id="0a168-130">operator to be repeated.</span></span>

<span data-ttu-id="0a168-131">Otra diferencia de .NET Framework expresiones regulares es que las expresiones regulares de escritura a mano no admiten una expresión vacía designada con un par de paréntesis vacío, ().</span><span class="sxs-lookup"><span data-stu-id="0a168-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="0a168-132">Solo se admiten caracteres en la página de códigos 1252 para las expresiones regulares de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="0a168-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="0a168-133">Usar ámbitos de entrada</span><span class="sxs-lookup"><span data-stu-id="0a168-133">Using Input Scopes</span></span>

<span data-ttu-id="0a168-134">También puede usar el conjunto de ámbitos de entrada normales que se definen como parte de la función [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) en las expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="0a168-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="0a168-135">Por ejemplo, el valor de month (numérica) es \_ Date \_ month.</span><span class="sxs-lookup"><span data-stu-id="0a168-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="0a168-136">La sintaxis para especificar un ámbito de entrada como parte de una expresión regular es anteponer el valor enumerado del ámbito de entrada con un paréntesis de apertura y un signo de exclamación, (! y colocar un paréntesis de cierre,) al final.</span><span class="sxs-lookup"><span data-stu-id="0a168-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="0a168-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0a168-137">For example:</span></span>

<span data-ttu-id="0a168-138">(! Es \_ mes de la fecha \_ )</span><span class="sxs-lookup"><span data-stu-id="0a168-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="0a168-139">Si combina el ámbito de \_ entrada predeterminado de is oring con cualquier otro ámbito de entrada, el efecto es que el reconocedor puede devolver cualquier expresión única que admita el modelo de lenguaje predeterminado (por ejemplo, una palabra del Diccionario del sistema o una fecha) con o sin puntuación, o cualquier valor que cumpla el resto de la expresión regular pasada al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="0a168-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="0a168-140">Los siguientes miembros de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) no se admiten en expresiones regulares: is \_ PHRASELIST, is REGULAREXPRESSION, IS \_ \_ SRGS, is \_ xml.</span><span class="sxs-lookup"><span data-stu-id="0a168-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="0a168-141">Operadores no admitidos</span><span class="sxs-lookup"><span data-stu-id="0a168-141">Unsupported Operators</span></span>

<span data-ttu-id="0a168-142">No se admiten los siguientes operadores de expresión regular al crear expresiones regulares de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="0a168-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="0a168-143">Operator</span><span class="sxs-lookup"><span data-stu-id="0a168-143">Operator</span></span>                                     | <span data-ttu-id="0a168-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a168-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0a168-145">.</span><span class="sxs-lookup"><span data-stu-id="0a168-145">.</span></span><br/>                                 | <span data-ttu-id="0a168-146">Carácter de punto.</span><span class="sxs-lookup"><span data-stu-id="0a168-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="0a168-147">Corchetes.</span><span class="sxs-lookup"><span data-stu-id="0a168-147">Square brackets.</span></span> <span data-ttu-id="0a168-148">Use paréntesis para agrupar elementos.</span><span class="sxs-lookup"><span data-stu-id="0a168-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="0a168-149">Llaves.</span><span class="sxs-lookup"><span data-stu-id="0a168-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="0a168-150">(?\# comentario) y \# \[ Comentario\]</span><span class="sxs-lookup"><span data-stu-id="0a168-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="0a168-151">Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0a168-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="0a168-152">Carácter de signo de dólar.</span><span class="sxs-lookup"><span data-stu-id="0a168-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="0a168-153">Carácter de intercalación.</span><span class="sxs-lookup"><span data-stu-id="0a168-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="0a168-154">Carácter de guión.</span><span class="sxs-lookup"><span data-stu-id="0a168-154">Dash character.</span></span> <span data-ttu-id="0a168-155">Debe o ( \| ) juntos todos los conjuntos de elementos.</span><span class="sxs-lookup"><span data-stu-id="0a168-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="0a168-156">Evitar caracteres</span><span class="sxs-lookup"><span data-stu-id="0a168-156">Escaping Characters</span></span>

<span data-ttu-id="0a168-157">Los caracteres ordinarios, excepto los de la tabla siguiente, coinciden.</span><span class="sxs-lookup"><span data-stu-id="0a168-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="0a168-158">Es decir, una "a" en una expresión regular especifica que la entrada debe coincidir con una "a".</span><span class="sxs-lookup"><span data-stu-id="0a168-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="0a168-159">Otra diferencia significativa en la escritura de expresiones regulares de escritura a mano es que solo puede escapar un conjunto limitado de caracteres dentro de una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="0a168-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="0a168-160">En la tabla siguiente se describe el conjunto de caracteres permitido que se puede usar como carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="0a168-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="0a168-161">Cualquier otro intento de escapar un carácter producirá un error producido por el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="0a168-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="0a168-162">Carácter</span><span class="sxs-lookup"><span data-stu-id="0a168-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="0a168-163">\\?</span><span class="sxs-lookup"><span data-stu-id="0a168-163">\\?</span></span><br/>  |
| <span data-ttu-id="0a168-164">\\(</span><span class="sxs-lookup"><span data-stu-id="0a168-164">\\(</span></span><br/>  |
| <span data-ttu-id="0a168-165">\\)</span><span class="sxs-lookup"><span data-stu-id="0a168-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="0a168-166">\\!</span><span class="sxs-lookup"><span data-stu-id="0a168-166">\\!</span></span><br/>  |
| <span data-ttu-id="0a168-167">\\.</span><span class="sxs-lookup"><span data-stu-id="0a168-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="0a168-168">\\{</span><span class="sxs-lookup"><span data-stu-id="0a168-168">\\{</span></span><br/>  |
| <span data-ttu-id="0a168-169">\\}</span><span class="sxs-lookup"><span data-stu-id="0a168-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 