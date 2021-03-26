---
title: Warning (Directiva pragma)
description: Directiva pragma que modifica el comportamiento de los mensajes de advertencia del compilador.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- Warning (Directiva pragma) HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994710"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="d2569-104">Warning (Directiva pragma)</span><span class="sxs-lookup"><span data-stu-id="d2569-104">warning pragma Directive</span></span>

<span data-ttu-id="d2569-105">Directiva pragma que modifica el comportamiento de los mensajes de advertencia del compilador.</span><span class="sxs-lookup"><span data-stu-id="d2569-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="d2569-106">\#pragma warning ( *Warning-Specifier* : *Warning-Number-List* \[ ; *Warning-Specifier* : *ADVERTENCIA-número-lista*... \] )</span><span class="sxs-lookup"><span data-stu-id="d2569-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d2569-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2569-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2569-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d2569-108">Item</span></span></th>
<th><span data-ttu-id="d2569-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2569-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2569-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>Warning-Specifier</em></span><span class="sxs-lookup"><span data-stu-id="d2569-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="d2569-111">Comportamiento que se va a establecer para las advertencias especificadas.</span><span class="sxs-lookup"><span data-stu-id="d2569-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="d2569-112">Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d2569-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d2569-113">Value</span><span class="sxs-lookup"><span data-stu-id="d2569-113">Value</span></span></th>
<th><span data-ttu-id="d2569-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2569-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2569-115">once</span><span class="sxs-lookup"><span data-stu-id="d2569-115">once</span></span></td>
<td><span data-ttu-id="d2569-116">Muestra el mensaje de las advertencias con los números especificados una sola vez.</span><span class="sxs-lookup"><span data-stu-id="d2569-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2569-117">default</span><span class="sxs-lookup"><span data-stu-id="d2569-117">default</span></span></td>
<td><span data-ttu-id="d2569-118">Restablezca el comportamiento de las advertencias con los números especificados a su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2569-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="d2569-119">Esto también tiene el efecto de activar una advertencia en que está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d2569-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="d2569-120">La advertencia se generará en su nivel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2569-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2569-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="d2569-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="d2569-122">Aplica el nivel especificado a las advertencias con los números especificados.</span><span class="sxs-lookup"><span data-stu-id="d2569-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="d2569-123">Esto también tiene el efecto de activar una advertencia en que está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d2569-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2569-124">disable</span><span class="sxs-lookup"><span data-stu-id="d2569-124">disable</span></span></td>
<td><span data-ttu-id="d2569-125">No emita las advertencias con los números especificados.</span><span class="sxs-lookup"><span data-stu-id="d2569-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2569-126">error</span><span class="sxs-lookup"><span data-stu-id="d2569-126">error</span></span></td>
<td><span data-ttu-id="d2569-127">Notificar las advertencias con los números especificados como errores.</span><span class="sxs-lookup"><span data-stu-id="d2569-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2569-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>ADVERTENCIA: número-lista</em></span><span class="sxs-lookup"><span data-stu-id="d2569-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="d2569-129">Lista delimitada por espacios en blanco de los números de las advertencias para modificar el comportamiento de.</span><span class="sxs-lookup"><span data-stu-id="d2569-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d2569-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2569-130">Remarks</span></span>

<span data-ttu-id="d2569-131">Puede especificar cualquier número de cambios de comportamiento de advertencia distintos dentro de la misma pragma warning separando los cambios con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="d2569-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="d2569-132">El compilador agregará 4000 a cualquier número de advertencia que esté entre 0 y 999.</span><span class="sxs-lookup"><span data-stu-id="d2569-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="d2569-133">Para los números de advertencia mayores que 4699 (los asociados a la generación de código), la pragma warning solo tiene efecto cuando se colocan fuera de las definiciones de función.</span><span class="sxs-lookup"><span data-stu-id="d2569-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="d2569-134">La Directiva pragma se omite si especifica un número mayor que 4699 y se utiliza dentro de una función.</span><span class="sxs-lookup"><span data-stu-id="d2569-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="d2569-135">La instrucción pragma de advertencia de HLSL no admite la **funcionalidad de** **extracción** y de confirmación de la pragma warning incluida en el compilador de C++.</span><span class="sxs-lookup"><span data-stu-id="d2569-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="d2569-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2569-136">Examples</span></span>

<span data-ttu-id="d2569-137">En el ejemplo siguiente se deshabilitan las advertencias 4507 y 4034, se muestra la advertencia 4385 una vez y se notifica la advertencia 4164 como un error.</span><span class="sxs-lookup"><span data-stu-id="d2569-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="d2569-138">El ejemplo anterior es funcionalmente equivalente a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d2569-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="d2569-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2569-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2569-140">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2569-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="d2569-141">\#pragma (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2569-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





