---
title: Gramática
description: Las instrucciones de HLSL se construyen con las siguientes reglas para la gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532902"
---
# <a name="grammar"></a><span data-ttu-id="ca4d8-103">Gramática</span><span class="sxs-lookup"><span data-stu-id="ca4d8-103">Grammar</span></span>

<span data-ttu-id="ca4d8-104">Las instrucciones de HLSL se construyen con las siguientes reglas para la gramática.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="ca4d8-105">Eran</span><span class="sxs-lookup"><span data-stu-id="ca4d8-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="ca4d8-106">Números de punto flotante</span><span class="sxs-lookup"><span data-stu-id="ca4d8-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="ca4d8-107">Números enteros</span><span class="sxs-lookup"><span data-stu-id="ca4d8-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="ca4d8-108">Caracteres</span><span class="sxs-lookup"><span data-stu-id="ca4d8-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="ca4d8-109">Cadenas</span><span class="sxs-lookup"><span data-stu-id="ca4d8-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="ca4d8-110">Identificadores</span><span class="sxs-lookup"><span data-stu-id="ca4d8-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="ca4d8-111">Operadores</span><span class="sxs-lookup"><span data-stu-id="ca4d8-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="ca4d8-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca4d8-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="ca4d8-113">Espacio en blanco</span><span class="sxs-lookup"><span data-stu-id="ca4d8-113">Whitespace</span></span>

<span data-ttu-id="ca4d8-114">Los caracteres siguientes se reconocen como un espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="ca4d8-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="ca4d8-115">SPACE</span></span>                      |
| <span data-ttu-id="ca4d8-116">TAB</span><span class="sxs-lookup"><span data-stu-id="ca4d8-116">TAB</span></span>                        |
| <span data-ttu-id="ca4d8-117">EOL</span><span class="sxs-lookup"><span data-stu-id="ca4d8-117">EOL</span></span>                        |
| <span data-ttu-id="ca4d8-118">Comentarios de estilo de C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="ca4d8-119">Comentarios de estilo de C++ (//)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="ca4d8-120">Números de punto flotante</span><span class="sxs-lookup"><span data-stu-id="ca4d8-120">Floating point numbers</span></span>

<span data-ttu-id="ca4d8-121">Los números de punto flotante se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="ca4d8-122">elemento de exponente de constante fraccionaria (OPC) sufijo flotante (OPT)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="ca4d8-123">exponente de secuencia de dígitos-sufijo flotante de parte (OPT)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="ca4d8-124">fraccionario-constante:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-124">fractional-constant :</span></span>

    <span data-ttu-id="ca4d8-125">Digit-Sequence (OPT).</span><span class="sxs-lookup"><span data-stu-id="ca4d8-125">digit-sequence(opt) .</span></span> <span data-ttu-id="ca4d8-126">Digit-Sequence</span><span class="sxs-lookup"><span data-stu-id="ca4d8-126">digit-sequence</span></span>

    <span data-ttu-id="ca4d8-127">secuencia de dígitos.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-127">digit-sequence .</span></span>

-   <span data-ttu-id="ca4d8-128">exponente: parte:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-128">exponent-part :</span></span>

    <span data-ttu-id="ca4d8-129">e signo (OPT) dígito-secuencia</span><span class="sxs-lookup"><span data-stu-id="ca4d8-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="ca4d8-130">E signo (OPT) dígito-secuencia</span><span class="sxs-lookup"><span data-stu-id="ca4d8-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="ca4d8-131">sign : one of</span><span class="sxs-lookup"><span data-stu-id="ca4d8-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="ca4d8-132">Digit-Sequence:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-132">digit-sequence :</span></span>

    <span data-ttu-id="ca4d8-133">digit</span><span class="sxs-lookup"><span data-stu-id="ca4d8-133">digit</span></span>

    <span data-ttu-id="ca4d8-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="ca4d8-134">digit-sequence digit</span></span>

-   <span data-ttu-id="ca4d8-135">floating-suffix : one of</span><span class="sxs-lookup"><span data-stu-id="ca4d8-135">floating-suffix : one of</span></span>

    <span data-ttu-id="ca4d8-136">h H f F l</span><span class="sxs-lookup"><span data-stu-id="ca4d8-136">h H f F l L</span></span>

    <span data-ttu-id="ca4d8-137">Use el sufijo "L" para especificar un literal de punto flotante de precisión de 64 bits completo.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="ca4d8-138">Un literal de punto flotante de 32 bits es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="ca4d8-139">Por ejemplo, el compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 32 bits y omite los bits inferiores:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="ca4d8-140">El compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="ca4d8-141">Números enteros</span><span class="sxs-lookup"><span data-stu-id="ca4d8-141">Integer numbers</span></span>

<span data-ttu-id="ca4d8-142">Los números enteros se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="ca4d8-143">entero: entero constante: sufijo (OPT)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="ca4d8-144">entero: constante: uno de</span><span class="sxs-lookup"><span data-stu-id="ca4d8-144">integer-constant: one of</span></span>

    <span data-ttu-id="ca4d8-145">\# (número decimal)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-145">\# (decimal number)</span></span>

    <span data-ttu-id="ca4d8-146">0 \# (número octal)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-146">0\# (octal number)</span></span>

    <span data-ttu-id="ca4d8-147">0x \# (número hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="ca4d8-148">Integer-Suffix puede ser cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="ca4d8-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="ca4d8-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="ca4d8-150">Characters</span><span class="sxs-lookup"><span data-stu-id="ca4d8-150">Characters</span></span>

<span data-ttu-id="ca4d8-151">Los caracteres se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ca4d8-152">"c"</span><span class="sxs-lookup"><span data-stu-id="ca4d8-152">'c'</span></span>                                       | <span data-ttu-id="ca4d8-153">óptico</span><span class="sxs-lookup"><span data-stu-id="ca4d8-153">(character)</span></span>                                                     |
| <span data-ttu-id="ca4d8-154">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="ca4d8-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="ca4d8-155">escape</span><span class="sxs-lookup"><span data-stu-id="ca4d8-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="ca4d8-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="ca4d8-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="ca4d8-157">(escape octal, cada uno \# es un dígito octal)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="ca4d8-158">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="ca4d8-158">'\\x\#'</span></span>                                   | <span data-ttu-id="ca4d8-159">(escape hexadecimal, \# es un número hexadecimal, cualquier número de dígitos)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="ca4d8-160">' \\ c '</span><span class="sxs-lookup"><span data-stu-id="ca4d8-160">'\\c'</span></span>                                     | <span data-ttu-id="ca4d8-161">(c es otro carácter, incluida la barra diagonal inversa y comillas)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="ca4d8-162">Los escapes no se admiten en expresiones de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="ca4d8-163">Cadenas</span><span class="sxs-lookup"><span data-stu-id="ca4d8-163">Strings</span></span>

<span data-ttu-id="ca4d8-164">Las cadenas se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="ca4d8-165">"s" (s es cualquier cadena con escapes).</span><span class="sxs-lookup"><span data-stu-id="ca4d8-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="ca4d8-166">Identificadores</span><span class="sxs-lookup"><span data-stu-id="ca4d8-166">Identifiers</span></span>

<span data-ttu-id="ca4d8-167">Los identificadores se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca4d8-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="ca4d8-168">Operadores</span><span class="sxs-lookup"><span data-stu-id="ca4d8-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="ca4d8-169">También cualquier otro carácter individual que no coincidía con otra regla.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca4d8-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca4d8-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca4d8-171">Apéndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca4d8-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




