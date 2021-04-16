---
description: ALL bit a bit y algunas palabras clave bit a bit se usan para probar los bits en un tipo entero.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL bit a bit y SOME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540654"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="62d30-103">ALL bit a bit y SOME</span><span class="sxs-lookup"><span data-stu-id="62d30-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="62d30-104">**All bit a bit** y algunas palabras clave **bit a bit** se usan para probar los bits en un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="62d30-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="62d30-105">Si todos los bits establecidos en una propiedad coinciden con la máscara, **All bit a bit** es true.</span><span class="sxs-lookup"><span data-stu-id="62d30-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="62d30-106">Si al menos uno de los bits establecidos en una propiedad coincide con la máscara, **algún bit a bit** es true.</span><span class="sxs-lookup"><span data-stu-id="62d30-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="62d30-107">Los operadores se pueden aplicar tanto a las propiedades escalares (de valor único) como a las propiedades de vector (varios valores).</span><span class="sxs-lookup"><span data-stu-id="62d30-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="62d30-108">En el ejemplo de código siguiente se muestra cómo se prueban los valores de propiedad con **todos los** **bits y bit a bit.**</span><span class="sxs-lookup"><span data-stu-id="62d30-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="62d30-109">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="62d30-109">Comparison Operators</span></span>

<span data-ttu-id="62d30-110">En la tabla siguiente se enumeran los operadores de comparación admitidos para las pruebas bit a bit.</span><span class="sxs-lookup"><span data-stu-id="62d30-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="62d30-111">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="62d30-111">Comparison operator</span></span> | <span data-ttu-id="62d30-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="62d30-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="62d30-113">Igual a</span><span class="sxs-lookup"><span data-stu-id="62d30-113">Equal to</span></span>     |
| <span data-ttu-id="62d30-114">! = o <></span><span class="sxs-lookup"><span data-stu-id="62d30-114">!= or <></span></span>      | <span data-ttu-id="62d30-115">No es igual a</span><span class="sxs-lookup"><span data-stu-id="62d30-115">Not equal to</span></span> |



 

<span data-ttu-id="62d30-116">En la tabla siguiente se muestra la lógica de las pruebas bit a bit.</span><span class="sxs-lookup"><span data-stu-id="62d30-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="62d30-117">Operador de comparación y prueba bit a bit</span><span class="sxs-lookup"><span data-stu-id="62d30-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="62d30-118">Lógica</span><span class="sxs-lookup"><span data-stu-id="62d30-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="62d30-119">= ALL BIT A BIT</span><span class="sxs-lookup"><span data-stu-id="62d30-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="62d30-120">Propiedad & Máscara = máscara</span><span class="sxs-lookup"><span data-stu-id="62d30-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="62d30-121">= ALGUNOS BITS</span><span class="sxs-lookup"><span data-stu-id="62d30-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="62d30-122">Propiedad & máscara! = 0</span><span class="sxs-lookup"><span data-stu-id="62d30-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="62d30-123"><> TODOS LOS BITS</span><span class="sxs-lookup"><span data-stu-id="62d30-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="62d30-124">Propiedad & Mask! = Mask</span><span class="sxs-lookup"><span data-stu-id="62d30-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="62d30-125"><> ALGUNOS BITS</span><span class="sxs-lookup"><span data-stu-id="62d30-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="62d30-126">Propiedad & máscara = 0</span><span class="sxs-lookup"><span data-stu-id="62d30-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="62d30-127">La siguiente tabla de verdad usa valores binarios y hexadecimales de ejemplo para demostrar la lógica de las pruebas bit a bit.</span><span class="sxs-lookup"><span data-stu-id="62d30-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="62d30-128">Propiedad en binario (hex)</span><span class="sxs-lookup"><span data-stu-id="62d30-128">Property in binary (hex)</span></span> | <span data-ttu-id="62d30-129">Máscara en binario (hex)</span><span class="sxs-lookup"><span data-stu-id="62d30-129">Mask in binary (hex)</span></span> | <span data-ttu-id="62d30-130">Propiedad & máscara = binaria (hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="62d30-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="62d30-131">= ALGUNOS BITS</span><span class="sxs-lookup"><span data-stu-id="62d30-131">= SOME BITWISE</span></span> | <span data-ttu-id="62d30-132">= ALL BIT A BIT</span><span class="sxs-lookup"><span data-stu-id="62d30-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="62d30-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-133">0001 (0x1)</span></span>               | <span data-ttu-id="62d30-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-134">0001 (0x1)</span></span>           | <span data-ttu-id="62d30-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-135">0001 (0x1)</span></span>                     | <span data-ttu-id="62d30-136">True</span><span class="sxs-lookup"><span data-stu-id="62d30-136">True</span></span>           | <span data-ttu-id="62d30-137">True</span><span class="sxs-lookup"><span data-stu-id="62d30-137">True</span></span>          |
| <span data-ttu-id="62d30-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-138">0001 (0x1)</span></span>               | <span data-ttu-id="62d30-139">0011 (0X3)</span><span class="sxs-lookup"><span data-stu-id="62d30-139">0011 (0x3)</span></span>           | <span data-ttu-id="62d30-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-140">0001 (0x1)</span></span>                     | <span data-ttu-id="62d30-141">True</span><span class="sxs-lookup"><span data-stu-id="62d30-141">True</span></span>           | <span data-ttu-id="62d30-142">False</span><span class="sxs-lookup"><span data-stu-id="62d30-142">False</span></span>         |
| <span data-ttu-id="62d30-143">0011 (0X3)</span><span class="sxs-lookup"><span data-stu-id="62d30-143">0011 (0x3)</span></span>               | <span data-ttu-id="62d30-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-144">0001 (0x1)</span></span>           | <span data-ttu-id="62d30-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-145">0001 (0x1)</span></span>                     | <span data-ttu-id="62d30-146">True</span><span class="sxs-lookup"><span data-stu-id="62d30-146">True</span></span>           | <span data-ttu-id="62d30-147">True</span><span class="sxs-lookup"><span data-stu-id="62d30-147">True</span></span>          |
| <span data-ttu-id="62d30-148">0010 (0X2)</span><span class="sxs-lookup"><span data-stu-id="62d30-148">0010 (0x2)</span></span>               | <span data-ttu-id="62d30-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="62d30-149">0001 (0x1)</span></span>           | <span data-ttu-id="62d30-150">0000 (0X0)</span><span class="sxs-lookup"><span data-stu-id="62d30-150">0000 (0x0)</span></span>                     | <span data-ttu-id="62d30-151">False</span><span class="sxs-lookup"><span data-stu-id="62d30-151">False</span></span>          | <span data-ttu-id="62d30-152">False</span><span class="sxs-lookup"><span data-stu-id="62d30-152">False</span></span>         |
| <span data-ttu-id="62d30-153">11110000 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="62d30-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="62d30-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="62d30-154">00000011 (0x03)</span></span>      | <span data-ttu-id="62d30-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="62d30-155">00000000 (0x00)</span></span>                | <span data-ttu-id="62d30-156">False</span><span class="sxs-lookup"><span data-stu-id="62d30-156">False</span></span>          | <span data-ttu-id="62d30-157">False</span><span class="sxs-lookup"><span data-stu-id="62d30-157">False</span></span>         |
| <span data-ttu-id="62d30-158">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="62d30-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="62d30-159">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="62d30-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="62d30-160">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="62d30-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="62d30-161">True</span><span class="sxs-lookup"><span data-stu-id="62d30-161">True</span></span>           | <span data-ttu-id="62d30-162">True</span><span class="sxs-lookup"><span data-stu-id="62d30-162">True</span></span>          |
| <span data-ttu-id="62d30-163">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="62d30-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="62d30-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="62d30-164">00000011 (0x03)</span></span>      | <span data-ttu-id="62d30-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="62d30-165">00000010 (0x02)</span></span>                | <span data-ttu-id="62d30-166">True</span><span class="sxs-lookup"><span data-stu-id="62d30-166">True</span></span>           | <span data-ttu-id="62d30-167">False</span><span class="sxs-lookup"><span data-stu-id="62d30-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="62d30-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62d30-168">Example</span></span>

<span data-ttu-id="62d30-169">El siguiente es un ejemplo del predicado **bit a bit All** .</span><span class="sxs-lookup"><span data-stu-id="62d30-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="62d30-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62d30-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62d30-171">**Vista**</span><span class="sxs-lookup"><span data-stu-id="62d30-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62d30-172">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="62d30-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="62d30-173">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="62d30-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



