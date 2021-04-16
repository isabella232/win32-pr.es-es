---
title: Modificador/w
description: El modificador/W especifica el nivel de advertencia del compilador de MIDL. El nivel de advertencia indica la gravedad de la advertencia.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W modificador MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685636"
---
# <a name="w-switch"></a><span data-ttu-id="20c99-105">Modificador/w</span><span class="sxs-lookup"><span data-stu-id="20c99-105">/W switch</span></span>

<span data-ttu-id="20c99-106">El modificador **/w** especifica el nivel de advertencia del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="20c99-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="20c99-107">El nivel de advertencia indica la gravedad de la advertencia.</span><span class="sxs-lookup"><span data-stu-id="20c99-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="20c99-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="20c99-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="20c99-109">*level*</span><span class="sxs-lookup"><span data-stu-id="20c99-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="20c99-110">Especifica el nivel de advertencia, un entero en el intervalo comprendido entre 0 y 4.</span><span class="sxs-lookup"><span data-stu-id="20c99-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="20c99-111">No hay espacio entre el modificador **/w** y el dígito que indica el valor de nivel de advertencia.</span><span class="sxs-lookup"><span data-stu-id="20c99-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20c99-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20c99-112">Remarks</span></span>

<span data-ttu-id="20c99-113">Los niveles de advertencia oscilan entre 1 y 4, y el valor cero significa que no se muestra ninguna información de advertencia.</span><span class="sxs-lookup"><span data-stu-id="20c99-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="20c99-114">La advertencia de mayor gravedad es el nivel 1.</span><span class="sxs-lookup"><span data-stu-id="20c99-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="20c99-115">En la tabla siguiente se describen las advertencias para cada nivel de advertencia.</span><span class="sxs-lookup"><span data-stu-id="20c99-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="20c99-116">Nivel de advertencia</span><span class="sxs-lookup"><span data-stu-id="20c99-116">Warning level</span></span> | <span data-ttu-id="20c99-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="20c99-117">Description</span></span>                                             | <span data-ttu-id="20c99-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20c99-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="20c99-119">W0 (</span><span class="sxs-lookup"><span data-stu-id="20c99-119">W0</span></span>            | <span data-ttu-id="20c99-120">Sin advertencias.</span><span class="sxs-lookup"><span data-stu-id="20c99-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="20c99-121">W1</span><span class="sxs-lookup"><span data-stu-id="20c99-121">W1</span></span>            | <span data-ttu-id="20c99-122">ADVERTENCIAS graves que pueden provocar errores en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20c99-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="20c99-123">No se especificó ningún identificador de enlace, punteros sin atributos, modificadores en conflicto.</span><span class="sxs-lookup"><span data-stu-id="20c99-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="20c99-124">W2</span><span class="sxs-lookup"><span data-stu-id="20c99-124">W2</span></span>            | <span data-ttu-id="20c99-125">Puede causar problemas en el entorno operativo del usuario.</span><span class="sxs-lookup"><span data-stu-id="20c99-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="20c99-126">La longitud del identificador supera los 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="20c99-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="20c99-127">No se especificó ningún brazo de Unión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20c99-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="20c99-128">W3</span><span class="sxs-lookup"><span data-stu-id="20c99-128">W3</span></span>            | <span data-ttu-id="20c99-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="20c99-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="20c99-130">W4</span><span class="sxs-lookup"><span data-stu-id="20c99-130">W4</span></span>            | <span data-ttu-id="20c99-131">Nivel de advertencia más bajo.</span><span class="sxs-lookup"><span data-stu-id="20c99-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="20c99-132">Construcciones no ANSI C.</span><span class="sxs-lookup"><span data-stu-id="20c99-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="20c99-133">Las advertencias son distintas de los errores.</span><span class="sxs-lookup"><span data-stu-id="20c99-133">Warnings are different from errors.</span></span> <span data-ttu-id="20c99-134">Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="20c99-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="20c99-135">Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="20c99-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="20c99-136">El nivel de advertencia establecido por el modificador **/w** se puede usar con el modificador [**/WX**](-wx.md) para que el compilador MIDL detenga el procesamiento del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="20c99-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="20c99-137">El modificador **/w** se comporta igual que el modificador [**/WARN**](-warn.md) .</span><span class="sxs-lookup"><span data-stu-id="20c99-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="20c99-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="20c99-138">Examples</span></span>

<span data-ttu-id="20c99-139">**MIDL/W2 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="20c99-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="20c99-140">**barra de/W4 de MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="20c99-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="20c99-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="20c99-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c99-142">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="20c99-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="20c99-143">**/WARN**</span><span class="sxs-lookup"><span data-stu-id="20c99-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




