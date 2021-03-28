---
title: " If, Elif, Else y endif (directivas)"
description: Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- If, Elif, Else y endif (directivas HLSL)
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149283"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="c423e-104">\#If, \# Elif, \# Else y \# endif (directivas)</span><span class="sxs-lookup"><span data-stu-id="c423e-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="c423e-105">Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="c423e-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="c423e-106">\#Si *ifCondition* ...</span><span class="sxs-lookup"><span data-stu-id="c423e-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="c423e-107">\[\#Elif *elifCondition* ...\]</span><span class="sxs-lookup"><span data-stu-id="c423e-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="c423e-108">\[\#otra cosa...\]</span><span class="sxs-lookup"><span data-stu-id="c423e-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="c423e-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="c423e-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="c423e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c423e-110">Parameters</span></span>



| <span data-ttu-id="c423e-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="c423e-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="c423e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c423e-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c423e-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span><span class="sxs-lookup"><span data-stu-id="c423e-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="c423e-114">Condición primaria que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="c423e-114">Primary condition to evaluate.</span></span> <span data-ttu-id="c423e-115">Si este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta \# Directiva if y la siguiente instancia de la \# Directiva Elif, \# else o \# endif se conserva en la unidad de traducción; de lo contrario, el código fuente subsiguiente no se conserva.</span><span class="sxs-lookup"><span data-stu-id="c423e-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="c423e-116">La condición puede utilizar el operador de preprocesador definido para determinar si se ha definido una constante o una macro de preprocesador específica; Este uso es equivalente al uso de la directiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="c423e-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="c423e-117">Vea la sección Comentarios para conocer las restricciones sobre el valor del parámetro *ifCondition* .</span><span class="sxs-lookup"><span data-stu-id="c423e-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="c423e-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="c423e-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="c423e-119">Otra condición que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="c423e-119">Other condition to evaluate.</span></span> <span data-ttu-id="c423e-120">Si el parámetro *ifCondition* y todas las \# directivas Elif anteriores se evalúan como cero, y este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta \# Directiva Elif y la siguiente instancia de la \# Directiva Elif, \# else o \# endif se conserva en la unidad de traducción; de lo contrario, el código fuente subsiguiente no se conserva.</span><span class="sxs-lookup"><span data-stu-id="c423e-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="c423e-121">La condición puede utilizar el operador de preprocesador definido para determinar si se ha definido una constante o una macro de preprocesador específica; Este uso es equivalente al uso de la directiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="c423e-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="c423e-122">Vea la sección Comentarios para conocer las restricciones sobre el valor del parámetro *elifCondition* .</span><span class="sxs-lookup"><span data-stu-id="c423e-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c423e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c423e-123">Remarks</span></span>

<span data-ttu-id="c423e-124">Cada \# Directiva if en un archivo de código fuente debe coincidir con una \# Directiva de cierre endif.</span><span class="sxs-lookup"><span data-stu-id="c423e-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="c423e-125">Puede aparecer cualquier número de \# directivas Elif entre las \# directivas if y \# endif, pero se permite como máximo una \# Directiva else.</span><span class="sxs-lookup"><span data-stu-id="c423e-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="c423e-126">La \# Directiva else, si está presente, debe ser la última Directiva antes de \# endif.</span><span class="sxs-lookup"><span data-stu-id="c423e-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="c423e-127">Las directivas de compilación condicional contenidas en archivos de inclusión deben cumplir las mismas condiciones.</span><span class="sxs-lookup"><span data-stu-id="c423e-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="c423e-128">Las \# directivas if, \# Elif, \# Else y \# endif pueden anidarse en las partes de texto de otras \# directivas if.</span><span class="sxs-lookup"><span data-stu-id="c423e-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="c423e-129">Cada directiva anidada \# else, \# Elif o \# endif pertenece a la Directiva if anterior más cercana \# .</span><span class="sxs-lookup"><span data-stu-id="c423e-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="c423e-130">Si ninguna condición se evalúa como un valor distinto de cero, el preprocesador selecciona el bloque de texto después de la \# Directiva else.</span><span class="sxs-lookup"><span data-stu-id="c423e-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="c423e-131">Si \# se omite la cláusula else y ninguna condición se evalúa como un valor distinto de cero, no se selecciona ningún bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="c423e-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="c423e-132">Los parámetros *ifCondition* y *elifCondition* cumplen los requisitos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c423e-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="c423e-133">Las expresiones de compilación condicional se tratan como valores [**largos con signo**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) y estas expresiones se evalúan con las mismas reglas que las expresiones en C++.</span><span class="sxs-lookup"><span data-stu-id="c423e-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="c423e-134">Las expresiones deben tener tipo entero y solo pueden incluir constantes de tipo entero, constantes de caracteres y el operador defined.</span><span class="sxs-lookup"><span data-stu-id="c423e-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="c423e-135">Las expresiones no pueden usar **sizeof** o un operador de conversión de tipos.</span><span class="sxs-lookup"><span data-stu-id="c423e-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="c423e-136">Es posible que el entorno de destino no pueda representar todos los intervalos de enteros.</span><span class="sxs-lookup"><span data-stu-id="c423e-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="c423e-137">La traducción representa el tipo [**int**](/windows/desktop/WinProg/windows-data-types) igual que el tipo **Long** y [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) igual que **unsigned Long**.</span><span class="sxs-lookup"><span data-stu-id="c423e-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="c423e-138">El traductor puede traducir constantes de caracteres a un conjunto de valores de código diferentes del conjunto para el entorno de destino.</span><span class="sxs-lookup"><span data-stu-id="c423e-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="c423e-139">Para determinar las propiedades del entorno de destino, compruebe los valores de las macros de LIMITS.H en una aplicación compilada para el entorno de destino.</span><span class="sxs-lookup"><span data-stu-id="c423e-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="c423e-140">La expresión no debe realizar ninguna consulta de ambiente y debe permanecer aislada de los detalles de implementación del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c423e-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="c423e-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c423e-141">Examples</span></span>

<span data-ttu-id="c423e-142">Esta sección contiene ejemplos que muestran cómo usar las directivas de preprocesador de compilación condicional.</span><span class="sxs-lookup"><span data-stu-id="c423e-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="c423e-143">Uso del operador definido</span><span class="sxs-lookup"><span data-stu-id="c423e-143">Use of the defined operator</span></span>

<span data-ttu-id="c423e-144">En el siguiente ejemplo se muestra el uso del operador defined.</span><span class="sxs-lookup"><span data-stu-id="c423e-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="c423e-145">Si se define el crédito del identificador, se compila la llamada a la función de **crédito** .</span><span class="sxs-lookup"><span data-stu-id="c423e-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="c423e-146">Si se define el identificador de débito, se compila la llamada a la función de **débito** .</span><span class="sxs-lookup"><span data-stu-id="c423e-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="c423e-147">Si no se define ningún identificador, se compila la llamada a la función **printerror** .</span><span class="sxs-lookup"><span data-stu-id="c423e-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="c423e-148">Tenga en cuenta que "CREDIT" y "Credit" son identificadores distintos en C y C++ porque sus casos son diferentes.</span><span class="sxs-lookup"><span data-stu-id="c423e-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="c423e-149">Uso de \# directivas if anidadas</span><span class="sxs-lookup"><span data-stu-id="c423e-149">Use of nested \#if directives</span></span>

<span data-ttu-id="c423e-150">En el ejemplo siguiente se muestra cómo anidar \# directivas if.</span><span class="sxs-lookup"><span data-stu-id="c423e-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="c423e-151">En este ejemplo se da por supuesto que se ha definido previamente una constante simbólica denominada DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="c423e-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="c423e-152">Las \# directivas Elif y \# else se usan para tomar una de las cuatro opciones, según el valor de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="c423e-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="c423e-153">La pila de constantes se establece en 0, 100 o 200, en función de la definición de DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="c423e-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="c423e-154">Si DLEVEL es mayor que 5, la pila no está definida.</span><span class="sxs-lookup"><span data-stu-id="c423e-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="c423e-155">Usar para incluir archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c423e-155">Use for including header files</span></span>

<span data-ttu-id="c423e-156">Un uso común para la compilación condicional es evitar inclusiones múltiples del mismo archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c423e-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="c423e-157">En C++, donde las clases suelen definirse en archivos de encabezado, se pueden usar construcciones de compilación condicionales para evitar varias definiciones.</span><span class="sxs-lookup"><span data-stu-id="c423e-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="c423e-158">En el ejemplo siguiente se determina si se define la constante simbólica EXAMPLE \_ H.</span><span class="sxs-lookup"><span data-stu-id="c423e-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="c423e-159">Si es así, el archivo ya se ha incluido y no es necesario volver a procesarlo; Si no es así, se define el ejemplo de constante \_ H para indicar ese ejemplo. H ya se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="c423e-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="c423e-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="c423e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c423e-161">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c423e-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

