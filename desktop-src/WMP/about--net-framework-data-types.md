---
title: Acerca de los tipos de datos .NET Framework
description: Acerca de los tipos de datos .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player, .NET Framework
- Modelo de objetos de Windows Media Player, .NET Framework
- modelo de objetos, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Control ActiveX de Windows Media Player, .NET Framework
- Control ActiveX móvil de Windows Media Player, .NET Framework
- Control ActiveX, .NET Framework
- .NET Framework, tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076222"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="d0906-111">Acerca de los tipos de datos .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d0906-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="d0906-112">Esta sección contiene la información necesaria para traducir la referencia del modelo de objetos orientado a scripts en tipos de datos base de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d0906-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="d0906-113">La referencia de script de Windows Media Player tiene casi toda la información necesaria para usar el control de Windows Media Player en un programa basado en .NET Framework y, en la mayoría de los casos, la sintaxis será similar a la de otros lenguajes de scripting como Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="d0906-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="d0906-114">La referencia de Media Player de Windows proporciona el tipo de datos de JScript y, si es necesario, la conversión de C++.</span><span class="sxs-lookup"><span data-stu-id="d0906-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="d0906-115">Por ejemplo, un método puede devolver un **número** .</span><span class="sxs-lookup"><span data-stu-id="d0906-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="d0906-116">JScript trata todos los números de la misma manera, pero otros lenguajes distinguen entre los distintos tipos de números (entero, punto flotante, etc.).</span><span class="sxs-lookup"><span data-stu-id="d0906-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="d0906-117">La referencia proporciona la conversión de C++ para los tipos de datos numéricos, ya que los números pueden procesarse de manera diferente en C++.</span><span class="sxs-lookup"><span data-stu-id="d0906-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="d0906-118">Por ejemplo, C++ usa el tipo de datos **int** para la aritmética de enteros y **float** para el punto flotante.</span><span class="sxs-lookup"><span data-stu-id="d0906-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="d0906-119">El .NET Framework utiliza un sistema ligeramente diferente de tipos de datos base.</span><span class="sxs-lookup"><span data-stu-id="d0906-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="d0906-120">En la tabla siguiente se muestran las diferencias en los tipos de datos comunes que es probable que use.</span><span class="sxs-lookup"><span data-stu-id="d0906-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="d0906-121">Para obtener más información sobre los tipos de datos base de .NET Framework y la conversión a otros sistemas de tipo de datos, vea la guía del desarrollador de .NET Framework sobre los tipos de datos base del espacio de nombres del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0906-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="d0906-122">En esta tabla se proporciona el nombre de clase .NET Framework y el tipo de datos de C#.</span><span class="sxs-lookup"><span data-stu-id="d0906-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="d0906-123">Los tipos de datos para otros idiomas se definen para cada idioma en sus referencias de idioma respectivas.</span><span class="sxs-lookup"><span data-stu-id="d0906-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="d0906-124">Tipo de datos de script</span><span class="sxs-lookup"><span data-stu-id="d0906-124">Script data type</span></span> | <span data-ttu-id="d0906-125">Tipo de datos de C++</span><span class="sxs-lookup"><span data-stu-id="d0906-125">C++ data type</span></span>     | <span data-ttu-id="d0906-126">Clase .NET Framework (tipo de datos de C#)</span><span class="sxs-lookup"><span data-stu-id="d0906-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="d0906-127">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0906-127">**Number**</span></span>       | <span data-ttu-id="d0906-128">**int**</span><span class="sxs-lookup"><span data-stu-id="d0906-128">**int**</span></span>           | <span data-ttu-id="d0906-129">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="d0906-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="d0906-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0906-130">**Number**</span></span>       | <span data-ttu-id="d0906-131">**long**</span><span class="sxs-lookup"><span data-stu-id="d0906-131">**long**</span></span>          | <span data-ttu-id="d0906-132">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="d0906-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="d0906-133">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0906-133">**Number**</span></span>       | <span data-ttu-id="d0906-134">**double**</span><span class="sxs-lookup"><span data-stu-id="d0906-134">**double**</span></span>        | <span data-ttu-id="d0906-135">**Double** (**doble**)</span><span class="sxs-lookup"><span data-stu-id="d0906-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="d0906-136">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0906-136">**Number**</span></span>       | <span data-ttu-id="d0906-137">**float**</span><span class="sxs-lookup"><span data-stu-id="d0906-137">**float**</span></span>         | <span data-ttu-id="d0906-138">**Single** (**float**)</span><span class="sxs-lookup"><span data-stu-id="d0906-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="d0906-139">**String**</span><span class="sxs-lookup"><span data-stu-id="d0906-139">**String**</span></span>       | <span data-ttu-id="d0906-140">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="d0906-140">**BSTR**</span></span>          | <span data-ttu-id="d0906-141">**String** (**cadena**)</span><span class="sxs-lookup"><span data-stu-id="d0906-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="d0906-142">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d0906-142">**Boolean**</span></span>      | <span data-ttu-id="d0906-143">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d0906-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="d0906-144">**Booleano** (**bool**)</span><span class="sxs-lookup"><span data-stu-id="d0906-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="d0906-145">**Object**</span><span class="sxs-lookup"><span data-stu-id="d0906-145">**Object**</span></span>       | <span data-ttu-id="d0906-146">**Object**</span><span class="sxs-lookup"><span data-stu-id="d0906-146">**Object**</span></span>        | <span data-ttu-id="d0906-147">**Object** (**objeto**)</span><span class="sxs-lookup"><span data-stu-id="d0906-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="d0906-148">Si usa Visual Studio, puede usar la tecnología de Microsoft IntelliSense para determinar qué tipo de datos se espera para una función específica.</span><span class="sxs-lookup"><span data-stu-id="d0906-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0906-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0906-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0906-150">**Incrustar el control Media Player de Windows en una solución de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="d0906-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="d0906-151">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="d0906-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




