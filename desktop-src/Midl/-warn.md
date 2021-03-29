---
title: /WARN (modificador)
description: El modificador/WARN especifica el nivel de advertencia del compilador de MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /WARN (modificador MIDL)
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783736"
---
# <a name="warn-switch"></a><span data-ttu-id="c6c3c-104">/WARN (modificador)</span><span class="sxs-lookup"><span data-stu-id="c6c3c-104">/warn switch</span></span>

<span data-ttu-id="c6c3c-105">El modificador **/WARN** especifica el nivel de advertencia del compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="c6c3c-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="c6c3c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c6c3c-107">*level*</span><span class="sxs-lookup"><span data-stu-id="c6c3c-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c3c-108">Especifica el nivel de advertencia, un entero en el intervalo comprendido entre 0 y 4.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="c6c3c-109">No hay espacio entre el modificador **/WARN** y el dígito que indica el valor de nivel de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6c3c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6c3c-110">Remarks</span></span>

<span data-ttu-id="c6c3c-111">El nivel de advertencia indica la gravedad de la advertencia.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="c6c3c-112">Los niveles de advertencia oscilan entre 1 y 4, y el valor cero significa que no se muestra ninguna información de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="c6c3c-113">La advertencia de mayor gravedad es el nivel 1.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="c6c3c-114">En la tabla siguiente se describen las advertencias para cada nivel de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="c6c3c-115">Nivel de advertencia</span><span class="sxs-lookup"><span data-stu-id="c6c3c-115">Warning level</span></span> | <span data-ttu-id="c6c3c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6c3c-116">Description</span></span>                                             | <span data-ttu-id="c6c3c-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6c3c-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c6c3c-118">0</span><span class="sxs-lookup"><span data-stu-id="c6c3c-118">0</span></span>             | <span data-ttu-id="c6c3c-119">Sin advertencias.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="c6c3c-120">1</span><span class="sxs-lookup"><span data-stu-id="c6c3c-120">1</span></span>             | <span data-ttu-id="c6c3c-121">ADVERTENCIAS graves que pueden provocar errores en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="c6c3c-122">No se especificó ningún identificador de enlace, punteros sin atributos, modificadores en conflicto.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="c6c3c-123">2</span><span class="sxs-lookup"><span data-stu-id="c6c3c-123">2</span></span>             | <span data-ttu-id="c6c3c-124">Puede causar problemas en el entorno operativo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="c6c3c-125">La longitud del identificador supera los 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="c6c3c-126">No se especificó ningún brazo de Unión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="c6c3c-127">3</span><span class="sxs-lookup"><span data-stu-id="c6c3c-127">3</span></span>             | <span data-ttu-id="c6c3c-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="c6c3c-129">4</span><span class="sxs-lookup"><span data-stu-id="c6c3c-129">4</span></span>             | <span data-ttu-id="c6c3c-130">Nivel de advertencia más bajo.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="c6c3c-131">Construcciones no ANSI C.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="c6c3c-132">Las advertencias son distintas de los errores.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-132">Warnings are different from errors.</span></span> <span data-ttu-id="c6c3c-133">Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="c6c3c-134">Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="c6c3c-135">El nivel de advertencia establecido por el modificador **/WARN** se puede usar con el modificador [**WX**](-wx.md) para hacer que el compilador MIDL detenga el procesamiento del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c6c3c-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="c6c3c-136">El modificador **/WARN** se comporta igual que el modificador [**/w**](-w.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c3c-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="c6c3c-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c6c3c-137">Examples</span></span>

<span data-ttu-id="c6c3c-138">**MIDL/warn2 nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="c6c3c-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="c6c3c-139">**barra de/warn4 de MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="c6c3c-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c6c3c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6c3c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c3c-141">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="c6c3c-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




