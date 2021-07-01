---
title: Gramática
description: Las instrucciones HLSL se construyen mediante las reglas siguientes para la gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129853"
---
# <a name="grammar"></a><span data-ttu-id="fd87e-103">Gramática</span><span class="sxs-lookup"><span data-stu-id="fd87e-103">Grammar</span></span>

<span data-ttu-id="fd87e-104">Las instrucciones HLSL se construyen mediante las reglas siguientes para la gramática.</span><span class="sxs-lookup"><span data-stu-id="fd87e-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="fd87e-105">Espacio en blanco</span><span class="sxs-lookup"><span data-stu-id="fd87e-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="fd87e-106">Números de punto flotante</span><span class="sxs-lookup"><span data-stu-id="fd87e-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="fd87e-107">Números enteros</span><span class="sxs-lookup"><span data-stu-id="fd87e-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="fd87e-108">Caracteres</span><span class="sxs-lookup"><span data-stu-id="fd87e-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="fd87e-109">Cadenas</span><span class="sxs-lookup"><span data-stu-id="fd87e-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="fd87e-110">Identificadores</span><span class="sxs-lookup"><span data-stu-id="fd87e-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="fd87e-111">Operadores</span><span class="sxs-lookup"><span data-stu-id="fd87e-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="fd87e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd87e-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="fd87e-113">Espacio en blanco</span><span class="sxs-lookup"><span data-stu-id="fd87e-113">Whitespace</span></span>

<span data-ttu-id="fd87e-114">Los caracteres siguientes se reconocen como espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="fd87e-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="fd87e-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="fd87e-115">SPACE</span></span>
- <span data-ttu-id="fd87e-116">TAB</span><span class="sxs-lookup"><span data-stu-id="fd87e-116">TAB</span></span>
- <span data-ttu-id="fd87e-117">Eol</span><span class="sxs-lookup"><span data-stu-id="fd87e-117">EOL</span></span>
- <span data-ttu-id="fd87e-118">Comentarios de estilo de C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="fd87e-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="fd87e-119">Comentarios de estilo de C++ (//)</span><span class="sxs-lookup"><span data-stu-id="fd87e-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="fd87e-120">Números de punto flotante</span><span class="sxs-lookup"><span data-stu-id="fd87e-120">Floating point numbers</span></span>

<span data-ttu-id="fd87e-121">Los números de punto flotante se representan en HLSL de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="fd87e-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="fd87e-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="fd87e-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="fd87e-123">digit-sequence exponent-part floating-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="fd87e-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="fd87e-124">fractional-constant :</span><span class="sxs-lookup"><span data-stu-id="fd87e-124">fractional-constant :</span></span>

    <span data-ttu-id="fd87e-125">digit-sequence(opt) .</span><span class="sxs-lookup"><span data-stu-id="fd87e-125">digit-sequence(opt) .</span></span> <span data-ttu-id="fd87e-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="fd87e-126">digit-sequence</span></span>

    <span data-ttu-id="fd87e-127">digit-sequence .</span><span class="sxs-lookup"><span data-stu-id="fd87e-127">digit-sequence .</span></span>

-   <span data-ttu-id="fd87e-128">exponent-part :</span><span class="sxs-lookup"><span data-stu-id="fd87e-128">exponent-part :</span></span>

    <span data-ttu-id="fd87e-129">e sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="fd87e-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="fd87e-130">E sign(opt) digit-sequence</span><span class="sxs-lookup"><span data-stu-id="fd87e-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="fd87e-131">sign : one of</span><span class="sxs-lookup"><span data-stu-id="fd87e-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="fd87e-132">digit-sequence :</span><span class="sxs-lookup"><span data-stu-id="fd87e-132">digit-sequence :</span></span>

    <span data-ttu-id="fd87e-133">digit</span><span class="sxs-lookup"><span data-stu-id="fd87e-133">digit</span></span>

    <span data-ttu-id="fd87e-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="fd87e-134">digit-sequence digit</span></span>

-   <span data-ttu-id="fd87e-135">floating-suffix : one of</span><span class="sxs-lookup"><span data-stu-id="fd87e-135">floating-suffix : one of</span></span>

    <span data-ttu-id="fd87e-136">h H f F l l</span><span class="sxs-lookup"><span data-stu-id="fd87e-136">h H f F l L</span></span>

    <span data-ttu-id="fd87e-137">Use el sufijo "L" para especificar un literal de punto flotante de precisión completa de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fd87e-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="fd87e-138">El valor predeterminado es un literal float de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fd87e-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="fd87e-139">Por ejemplo, el compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 32 bits y omite los bits inferiores:</span><span class="sxs-lookup"><span data-stu-id="fd87e-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="fd87e-140">El compilador reconoce el siguiente valor literal como un literal de punto flotante de precisión de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="fd87e-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="fd87e-141">Números enteros</span><span class="sxs-lookup"><span data-stu-id="fd87e-141">Integer numbers</span></span>

<span data-ttu-id="fd87e-142">Los números enteros se representan en HLSL como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="fd87e-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="fd87e-143">integer-constant integer-suffix(opt)</span><span class="sxs-lookup"><span data-stu-id="fd87e-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="fd87e-144">integer-constant: uno de</span><span class="sxs-lookup"><span data-stu-id="fd87e-144">integer-constant: one of</span></span>

    <span data-ttu-id="fd87e-145">\# (número decimal)</span><span class="sxs-lookup"><span data-stu-id="fd87e-145">\# (decimal number)</span></span>

    <span data-ttu-id="fd87e-146">0 \# (número octal)</span><span class="sxs-lookup"><span data-stu-id="fd87e-146">0\# (octal number)</span></span>

    <span data-ttu-id="fd87e-147">0x \# (número hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="fd87e-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="fd87e-148">integer-suffix puede ser cualquiera de estos:</span><span class="sxs-lookup"><span data-stu-id="fd87e-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="fd87e-149">u U l L</span><span class="sxs-lookup"><span data-stu-id="fd87e-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="fd87e-150">Characters</span><span class="sxs-lookup"><span data-stu-id="fd87e-150">Characters</span></span>

<span data-ttu-id="fd87e-151">Los caracteres se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fd87e-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="fd87e-152">Carácter</span><span class="sxs-lookup"><span data-stu-id="fd87e-152">Character</span></span>                                          | <span data-ttu-id="fd87e-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd87e-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fd87e-154">"c"</span><span class="sxs-lookup"><span data-stu-id="fd87e-154">'c'</span></span>                                       | <span data-ttu-id="fd87e-155">(carácter)</span><span class="sxs-lookup"><span data-stu-id="fd87e-155">(character)</span></span>                                                     |
| <span data-ttu-id="fd87e-156">' \\ a' ' \\ b' ' \\ f' ' \\ b' ' \\ r' ' \\ t' ' \\ v'</span><span class="sxs-lookup"><span data-stu-id="fd87e-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="fd87e-157">(escapes)</span><span class="sxs-lookup"><span data-stu-id="fd87e-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="fd87e-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="fd87e-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="fd87e-159">(escape octal, cada \# uno es un dígito octal)</span><span class="sxs-lookup"><span data-stu-id="fd87e-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="fd87e-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="fd87e-160">'\\x\#'</span></span>                                   | <span data-ttu-id="fd87e-161">(escape hexadecimal, \# es número hexadecimal, cualquier número de dígitos)</span><span class="sxs-lookup"><span data-stu-id="fd87e-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="fd87e-162">' \\ c'</span><span class="sxs-lookup"><span data-stu-id="fd87e-162">'\\c'</span></span>                                     | <span data-ttu-id="fd87e-163">(c es otro carácter, incluidas las barras diagonales inversas y las comillas)</span><span class="sxs-lookup"><span data-stu-id="fd87e-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="fd87e-164">Los escapes no se admiten en expresiones de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="fd87e-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="fd87e-165">Cadenas</span><span class="sxs-lookup"><span data-stu-id="fd87e-165">Strings</span></span>

<span data-ttu-id="fd87e-166">Las cadenas se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fd87e-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="fd87e-167">"s" (s es cualquier cadena con escapes).</span><span class="sxs-lookup"><span data-stu-id="fd87e-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="fd87e-168">Identificadores</span><span class="sxs-lookup"><span data-stu-id="fd87e-168">Identifiers</span></span>

<span data-ttu-id="fd87e-169">Los identificadores se representan en HLSL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fd87e-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="fd87e-170">Operadores</span><span class="sxs-lookup"><span data-stu-id="fd87e-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="fd87e-171">También cualquier otro carácter individual que no coincida con otra regla.</span><span class="sxs-lookup"><span data-stu-id="fd87e-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd87e-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd87e-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd87e-173">Apéndice (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="fd87e-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




