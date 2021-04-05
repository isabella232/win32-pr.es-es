---
description: En esta sección se describe la sintaxis de las instrucciones condicionales usadas por la función MsiEvaluateCondition y las tablas de secuencia de acciones. Para obtener más información, vea ejemplos de sintaxis de instrucciones condicionales.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintaxis de la instrucción condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909026"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="4dd6d-104">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="4dd6d-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="4dd6d-105">En esta sección se describe la sintaxis de las instrucciones condicionales usadas por la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) y las [tablas de secuencia](using-a-sequence-table.md)de acciones.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="4dd6d-106">Para obtener más información, vea [ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4dd6d-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="4dd6d-107">Resumen de la sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="4dd6d-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="4dd6d-108">En esta tabla y en la lista siguiente se resume la sintaxis que se va a usar en las expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="4dd6d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4dd6d-109">Item</span></span>                | <span data-ttu-id="4dd6d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dd6d-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd6d-111">value</span><span class="sxs-lookup"><span data-stu-id="4dd6d-111">value</span></span>               | <span data-ttu-id="4dd6d-112">\|entero de literal de símbolo \|</span><span class="sxs-lookup"><span data-stu-id="4dd6d-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="4dd6d-113">Comparison-Operator</span><span class="sxs-lookup"><span data-stu-id="4dd6d-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="4dd6d-114">término</span><span class="sxs-lookup"><span data-stu-id="4dd6d-114">term</span></span>                | <span data-ttu-id="4dd6d-115">\|comparación de valores de valor: valor del operador \| (expresión)\|</span><span class="sxs-lookup"><span data-stu-id="4dd6d-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="4dd6d-116">Factor booleano</span><span class="sxs-lookup"><span data-stu-id="4dd6d-116">Boolean-factor</span></span>      | <span data-ttu-id="4dd6d-117">término \| **no** term</span><span class="sxs-lookup"><span data-stu-id="4dd6d-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="4dd6d-118">Término booleano</span><span class="sxs-lookup"><span data-stu-id="4dd6d-118">Boolean-term</span></span>        | <span data-ttu-id="4dd6d-119">Factor booleano \| **y** término de factor booleano</span><span class="sxs-lookup"><span data-stu-id="4dd6d-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="4dd6d-120">expresión</span><span class="sxs-lookup"><span data-stu-id="4dd6d-120">expression</span></span>          | <span data-ttu-id="4dd6d-121">\|Expresión **o** término booleano de término booleano</span><span class="sxs-lookup"><span data-stu-id="4dd6d-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="4dd6d-122">símbolo</span><span class="sxs-lookup"><span data-stu-id="4dd6d-122">symbol</span></span>              | <span data-ttu-id="4dd6d-123">propiedad \| % Environment: variable \| $Component-Action \| ? componente-State \| &característica-acción \| ! Estado de la característica</span><span class="sxs-lookup"><span data-stu-id="4dd6d-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="4dd6d-124">Los nombres y valores de símbolos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="4dd6d-125">Los nombres de las variables de entorno no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="4dd6d-126">El texto literal debe ir entre comillas ("texto").</span><span class="sxs-lookup"><span data-stu-id="4dd6d-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="4dd6d-127">El texto literal que contiene comillas no se puede usar en instrucciones condicionales porque no hay ningún carácter de escape para las comillas dentro del texto literal.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="4dd6d-128">Para realizar una comparación con el texto literal que contiene comillas, el texto literal debe colocarse en una propiedad.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="4dd6d-129">Por ejemplo, para comprobar que la propiedad SERVERNAME no contiene comillas, defina una propiedad denominada QUOTEs en la [tabla de propiedades](property-table.md) con un valor de "y cambie la condición a not ServerName><Quotes.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="4dd6d-130">Los valores de propiedad inexistentes se tratan como cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="4dd6d-131">No se admiten valores numéricos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="4dd6d-132">Los operadores y la prioridad son los mismos que en los lenguajes básico y SQL.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="4dd6d-133">No se admiten los operadores aritméticos.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="4dd6d-134">Los paréntesis se pueden usar para invalidar la precedencia de los operadores.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="4dd6d-135">Los operadores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="4dd6d-136">En las comparaciones de cadenas, una tilde "~" con el prefijo para el operador realiza una comparación que no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="4dd6d-137">La comparación de un entero con un valor de cadena o propiedad que no se puede convertir en un entero es siempre **msiEvaluateConditionFalse**, excepto para el operador de comparación "<>", que devuelve **msiEvaluateConditionTrue**.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="4dd6d-138">Prefijos de acceso</span><span class="sxs-lookup"><span data-stu-id="4dd6d-138">Access Prefixes</span></span>

<span data-ttu-id="4dd6d-139">En la tabla siguiente se muestran los prefijos que se van a usar para tener acceso a diversa información del sistema y del instalador para su uso en expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="4dd6d-140">Tipo de símbolo</span><span class="sxs-lookup"><span data-stu-id="4dd6d-140">Symbol type</span></span>          | <span data-ttu-id="4dd6d-141">Prefijo</span><span class="sxs-lookup"><span data-stu-id="4dd6d-141">Prefix</span></span> | <span data-ttu-id="4dd6d-142">Value</span><span class="sxs-lookup"><span data-stu-id="4dd6d-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="4dd6d-143">Propiedad Installer</span><span class="sxs-lookup"><span data-stu-id="4dd6d-143">Installer property</span></span>   | <span data-ttu-id="4dd6d-144">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="4dd6d-144">(none)</span></span> | <span data-ttu-id="4dd6d-145">Valor de la tabla de propiedades ([propiedad](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="4dd6d-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="4dd6d-146">Variable de entorno</span><span class="sxs-lookup"><span data-stu-id="4dd6d-146">Environment variable</span></span> | %      | <span data-ttu-id="4dd6d-147">Valor de la variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="4dd6d-148">Clave de la tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="4dd6d-148">Component table key</span></span>  | $      | <span data-ttu-id="4dd6d-149">Estado de acción del componente.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="4dd6d-150">Clave de la tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="4dd6d-150">Component table key</span></span>  | <span data-ttu-id="4dd6d-151">?</span><span class="sxs-lookup"><span data-stu-id="4dd6d-151">?</span></span>      | <span data-ttu-id="4dd6d-152">Estado instalado del componente.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="4dd6d-153">Clave de la tabla de características</span><span class="sxs-lookup"><span data-stu-id="4dd6d-153">Feature table key</span></span>    | &      | <span data-ttu-id="4dd6d-154">Estado de acción de la característica.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="4dd6d-155">Clave de la tabla de características</span><span class="sxs-lookup"><span data-stu-id="4dd6d-155">Feature table key</span></span>    | <span data-ttu-id="4dd6d-156">!</span><span class="sxs-lookup"><span data-stu-id="4dd6d-156">!</span></span>      | <span data-ttu-id="4dd6d-157">Estado instalado de la característica.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="4dd6d-158">Operadores lógicos</span><span class="sxs-lookup"><span data-stu-id="4dd6d-158">Logical Operators</span></span>

<span data-ttu-id="4dd6d-159">En la tabla siguiente se muestran los operadores lógicos en expresiones condicionales, en orden de prioridad alta a baja.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="4dd6d-160">Operator</span><span class="sxs-lookup"><span data-stu-id="4dd6d-160">Operator</span></span> | <span data-ttu-id="4dd6d-161">Significado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="4dd6d-162">Not</span><span class="sxs-lookup"><span data-stu-id="4dd6d-162">Not</span></span>      | <span data-ttu-id="4dd6d-163">Prefix (operador unario); invierte el estado del término siguiente.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="4dd6d-164">And</span><span class="sxs-lookup"><span data-stu-id="4dd6d-164">And</span></span>      | <span data-ttu-id="4dd6d-165">TRUE si ambos términos son TRUE.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="4dd6d-166">O bien</span><span class="sxs-lookup"><span data-stu-id="4dd6d-166">Or</span></span>       | <span data-ttu-id="4dd6d-167">TRUE si uno o ambos términos son TRUE.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="4dd6d-168">Xor</span><span class="sxs-lookup"><span data-stu-id="4dd6d-168">Xor</span></span>      | <span data-ttu-id="4dd6d-169">TRUE si, pero no ambos términos, son verdaderos.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="4dd6d-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="4dd6d-170">Eqv</span></span>      | <span data-ttu-id="4dd6d-171">TRUE si ambos términos son TRUE o ambos términos son FALSE.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="4dd6d-172">Imp</span><span class="sxs-lookup"><span data-stu-id="4dd6d-172">Imp</span></span>      | <span data-ttu-id="4dd6d-173">TRUE si el término izquierdo es falso o el término derecho es TRUE.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="4dd6d-174">Operadores de comparación</span><span class="sxs-lookup"><span data-stu-id="4dd6d-174">Comparative Operators</span></span>

<span data-ttu-id="4dd6d-175">En la tabla siguiente se muestran los operadores de comparación que se usan en las expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="4dd6d-176">Estos operadores de comparación solo se pueden producir entre dos valores.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="4dd6d-177">Operator</span><span class="sxs-lookup"><span data-stu-id="4dd6d-177">Operator</span></span> | <span data-ttu-id="4dd6d-178">Significado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="4dd6d-179">TRUE si el valor de la izquierda es igual al valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="4dd6d-180">TRUE si el valor de la izquierda no es igual al valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="4dd6d-181">TRUE si el valor izquierdo es mayor que el valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="4dd6d-182">TRUE si el valor izquierdo es mayor o igual que el valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="4dd6d-183">TRUE si el valor de la izquierda es menor que el valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="4dd6d-184">TRUE si el valor de la izquierda es menor o igual que el valor derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="4dd6d-185">Operadores de subcadena</span><span class="sxs-lookup"><span data-stu-id="4dd6d-185">Substring Operators</span></span>

<span data-ttu-id="4dd6d-186">En la tabla siguiente se muestran los operadores de subcadena utilizados en las expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="4dd6d-187">Se pueden producir operadores de subcadena entre dos valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="4dd6d-188">Operator</span><span class="sxs-lookup"><span data-stu-id="4dd6d-188">Operator</span></span> | <span data-ttu-id="4dd6d-189">Significado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="4dd6d-190">TRUE si la cadena izquierda contiene la cadena derecha.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="4dd6d-191">TRUE si la cadena izquierda comienza con la cadena derecha.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="4dd6d-192">TRUE si la cadena izquierda termina con la cadena derecha.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="4dd6d-193">Operadores numéricos bit a bit</span><span class="sxs-lookup"><span data-stu-id="4dd6d-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="4dd6d-194">En la tabla siguiente se muestran los operadores numéricos bit a bit en expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="4dd6d-195">Estos operadores pueden producirse entre dos valores enteros.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="4dd6d-196">Operator</span><span class="sxs-lookup"><span data-stu-id="4dd6d-196">Operator</span></span> | <span data-ttu-id="4dd6d-197">Significado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="4dd6d-198">And bit a bit, TRUE si los enteros izquierdo y derecho tienen algún bit en común.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="4dd6d-199">True si los 16 bits superiores del entero izquierdo son iguales que el entero derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="4dd6d-200">True si los 16 bits inferiores del entero izquierdo son iguales que el entero derecho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="4dd6d-201">Valores de estado de componentes y características</span><span class="sxs-lookup"><span data-stu-id="4dd6d-201">Feature and Component State Values</span></span>

<span data-ttu-id="4dd6d-202">En la tabla siguiente se muestra dónde es válido usar los símbolos de operador de componentes y características.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="4dd6d-203">Operator <state></span><span class="sxs-lookup"><span data-stu-id="4dd6d-203">Operator <state></span></span> | <span data-ttu-id="4dd6d-204">Donde esta sintaxis es válida</span><span class="sxs-lookup"><span data-stu-id="4dd6d-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd6d-205">$component-acción</span><span class="sxs-lookup"><span data-stu-id="4dd6d-205">$component-action</span></span>      | <span data-ttu-id="4dd6d-206">En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="4dd6d-207">&característica-acción</span><span class="sxs-lookup"><span data-stu-id="4dd6d-207">&feature-action</span></span>        | <span data-ttu-id="4dd6d-208">En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="4dd6d-209">! Estado de la característica</span><span class="sxs-lookup"><span data-stu-id="4dd6d-209">!feature-state</span></span>         | <span data-ttu-id="4dd6d-210">En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="4dd6d-211">? componente-estado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-211">?component-state</span></span>       | <span data-ttu-id="4dd6d-212">En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="4dd6d-213">En la tabla siguiente se muestran los valores de estado de componentes y características que se usan en las expresiones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="4dd6d-214">Estos Estados no se establecen hasta que se llama a [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) , ya sea directamente o mediante la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="4dd6d-215">Estado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-215">State</span></span>                    | <span data-ttu-id="4dd6d-216">Value</span><span class="sxs-lookup"><span data-stu-id="4dd6d-216">Value</span></span> | <span data-ttu-id="4dd6d-217">Significado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="4dd6d-218">INSTALLSTATE \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="4dd6d-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="4dd6d-219">-1</span><span class="sxs-lookup"><span data-stu-id="4dd6d-219">-1</span></span>    | <span data-ttu-id="4dd6d-220">No se realiza ninguna acción en la característica o componente.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="4dd6d-221">INSTALLSTATE \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="4dd6d-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="4dd6d-222">1</span><span class="sxs-lookup"><span data-stu-id="4dd6d-222">1</span></span>     | <span data-ttu-id="4dd6d-223">Característica anunciada.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-223">Advertised feature.</span></span> <span data-ttu-id="4dd6d-224">Este estado no está disponible para los componentes de.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-224">This state is not available for components.</span></span> |
| <span data-ttu-id="4dd6d-225">INSTALLSTATE \_ ausente</span><span class="sxs-lookup"><span data-stu-id="4dd6d-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="4dd6d-226">2</span><span class="sxs-lookup"><span data-stu-id="4dd6d-226">2</span></span>     | <span data-ttu-id="4dd6d-227">La característica o componente no está presente.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="4dd6d-228">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="4dd6d-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="4dd6d-229">3</span><span class="sxs-lookup"><span data-stu-id="4dd6d-229">3</span></span>     | <span data-ttu-id="4dd6d-230">Característica o componente en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="4dd6d-231">origen de INSTALLSTATE \_</span><span class="sxs-lookup"><span data-stu-id="4dd6d-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="4dd6d-232">4</span><span class="sxs-lookup"><span data-stu-id="4dd6d-232">4</span></span>     | <span data-ttu-id="4dd6d-233">La característica o componente se ejecuta desde el origen.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="4dd6d-234">Por ejemplo, la expresión condicional "&función = 3" solo se evalúa como true si la función está cambiando de su estado actual al estado de instalación en el equipo local, INSTALLSTATE \_ local.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="4dd6d-235">Tenga en cuenta que no debe depender de la condición $Component 1 = 3 para comprobar si Component1 está instalado localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="4dd6d-236">Esto puede producir un error si Component1 está instalado por más de un producto.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="4dd6d-237">Una vez instalado Component1 localmente por Product1, el instalador evalúa la condición $Component 1 = 3 como false durante la instalación de product2.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="4dd6d-238">Esto se debe a que el instalador determina la versión del componente mediante la ruta de acceso de la clave del componente y marca el componente para la instalación si su versión es mayor o igual que el componente instalado.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="4dd6d-239">Tenga en cuenta que el instalador no realizará comparaciones directas del tipo de datos de la [versión](version.md) en las instrucciones condicionales.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="4dd6d-240">Por ejemplo, no puede utilizar operadores de comparación para comparar versiones como "01,10" y "1,010" en una instrucción condicional.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="4dd6d-241">En su lugar, use un método válido para buscar una versión, como se describe en [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)y, a continuación, establecer una propiedad.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dd6d-242">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4dd6d-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd6d-243">Usar propiedades en instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="4dd6d-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



