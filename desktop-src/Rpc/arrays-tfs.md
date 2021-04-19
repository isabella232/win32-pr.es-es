---
title: Matrices (RPC) (TFS)
description: Entre las categorías de matriz de llamada a procedimiento remoto (RPC) se incluyen el tamaño fijo, el cumplimiento, la estructura variable, la variable y la complejidad.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388817"
---
# <a name="arrays-rpc"></a><span data-ttu-id="75851-103">Matrices (RPC)</span><span class="sxs-lookup"><span data-stu-id="75851-103">Arrays (RPC)</span></span>

<span data-ttu-id="75851-104">Varias categorías de matriz se han definido en función de sus características de rendimiento, principalmente si la matriz puede ser copiada en bloque.</span><span class="sxs-lookup"><span data-stu-id="75851-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="75851-105">En algunas categorías, como una matriz de tamaño fijo, existen dos tipos de descriptores de matriz; se indican con una corrección en el nombre del token de FC inicial.</span><span class="sxs-lookup"><span data-stu-id="75851-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="75851-106">Carácter de formato</span><span class="sxs-lookup"><span data-stu-id="75851-106">Format character</span></span> | <span data-ttu-id="75851-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="75851-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="75851-108">SM</span><span class="sxs-lookup"><span data-stu-id="75851-108">SM</span></span>               | <span data-ttu-id="75851-109">El tamaño total del tipo se puede representar en un int sin signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="75851-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="75851-110">LG</span><span class="sxs-lookup"><span data-stu-id="75851-110">LG</span></span>               | <span data-ttu-id="75851-111">El tamaño total del tipo requiere un valor de unsigned Long de 32 bits para que se represente.</span><span class="sxs-lookup"><span data-stu-id="75851-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="75851-112">Campos comunes a las matrices:</span><span class="sxs-lookup"><span data-stu-id="75851-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="75851-113">\_Tamaño total</span><span class="sxs-lookup"><span data-stu-id="75851-113">total\_size</span></span>

    <span data-ttu-id="75851-114">Tamaño total de la matriz en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="75851-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="75851-115">Es igual que el tamaño de conexión después de la alineación.</span><span class="sxs-lookup"><span data-stu-id="75851-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="75851-116">El tamaño total se calcula para las categorías para las que no existe el problema de relleno y el tamaño es el tamaño real de la matriz.</span><span class="sxs-lookup"><span data-stu-id="75851-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="75851-117">tamaño del elemento \_</span><span class="sxs-lookup"><span data-stu-id="75851-117">element\_size</span></span>

    <span data-ttu-id="75851-118">Tamaño total en memoria de un solo elemento de la matriz, incluido el relleno (esto puede ocurrir solo para matrices complejas).</span><span class="sxs-lookup"><span data-stu-id="75851-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="75851-119">Descripción del elemento \_</span><span class="sxs-lookup"><span data-stu-id="75851-119">element\_description</span></span>

    <span data-ttu-id="75851-120">Descripción del tipo de elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="75851-120">Description of the array element type.</span></span>

-   <span data-ttu-id="75851-121">diseño de puntero \_</span><span class="sxs-lookup"><span data-stu-id="75851-121">pointer\_layout</span></span>

    <span data-ttu-id="75851-122">Vea el tema [diseño de puntero](pointer-layout-tfs.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="75851-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="75851-123">Matrices de tamaño fijo</span><span class="sxs-lookup"><span data-stu-id="75851-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="75851-124">Se genera una cadena de formato de matriz de tamaño fijo para las matrices que tienen un tamaño conocido y, por lo tanto, se puede copiar en bloque en el búfer de serialización.</span><span class="sxs-lookup"><span data-stu-id="75851-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="75851-125">Los dos formatos de descriptor de matriz fijos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="75851-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="75851-126">y</span><span class="sxs-lookup"><span data-stu-id="75851-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="75851-127">Matriz compatible</span><span class="sxs-lookup"><span data-stu-id="75851-127">Conformant Array</span></span>

<span data-ttu-id="75851-128">Una matriz compatible se puede copiar en bloque una vez que se conoce el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="75851-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="75851-129">La descripción del cumplimiento \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="75851-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="75851-130">Matriz variable compatible</span><span class="sxs-lookup"><span data-stu-id="75851-130">Conformant Varying Array</span></span>

<span data-ttu-id="75851-131">Una matriz variable compatible también se puede copiar en bloque.</span><span class="sxs-lookup"><span data-stu-id="75851-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="75851-132">La descripción del cumplimiento \_<> y la \_ Descripción de la varianza<> es un descriptor de correlación y tiene 4 o 6 bytes en función de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="75851-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="75851-133">Matriz variable</span><span class="sxs-lookup"><span data-stu-id="75851-133">Varying Array</span></span>

<span data-ttu-id="75851-134">Las distintas matrices tienen dos posibilidades, dependiendo del tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="75851-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="75851-135">La descripción de la varianza \_<> es un descriptor de correlación y tiene 4 o 6 bytes según el [**/Robust**](/windows/desktop/Midl/-robust) que se está usando.</span><span class="sxs-lookup"><span data-stu-id="75851-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="75851-136">En el caso de las distintas matrices incrustadas dentro de una estructura, el desplazamiento<2> campo de la descripción de la varianza \_<> es un desplazamiento relativo desde la posición de la matriz variable en la estructura hasta el campo de varianza que describe.</span><span class="sxs-lookup"><span data-stu-id="75851-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="75851-137">El desplazamiento suele ser relativo al principio de la estructura.</span><span class="sxs-lookup"><span data-stu-id="75851-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="75851-138">Matrices complejas</span><span class="sxs-lookup"><span data-stu-id="75851-138">Complex Arrays</span></span>

<span data-ttu-id="75851-139">Una matriz compleja es cualquier matriz con un elemento que impide que se copie en bloque y, como tal, se debe realizar una acción adicional.</span><span class="sxs-lookup"><span data-stu-id="75851-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="75851-140">Estos elementos hacen que una matriz sea compleja:</span><span class="sxs-lookup"><span data-stu-id="75851-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="75851-141">tipos simples: ENUM16, \_ \_ INT3264 (solo en plataformas de 64 bits), un entero con \[ [ **rango**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="75851-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="75851-142">punteros de referencia y de interfaz (todos los punteros en plataformas de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="75851-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="75851-143">uniones</span><span class="sxs-lookup"><span data-stu-id="75851-143">unions</span></span>
-   <span data-ttu-id="75851-144">estructuras complejas (consulte el tema de descripción de la estructura compleja para obtener una lista completa de los motivos para que una estructura sea compleja)</span><span class="sxs-lookup"><span data-stu-id="75851-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="75851-145">elementos definidos con \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ cálculo de referencias de usuarios**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="75851-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="75851-146">Todas las matrices multidimensionales con al menos una dimensión compatible y/o variable son complejas, independientemente del tipo de elemento subyacente.</span><span class="sxs-lookup"><span data-stu-id="75851-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="75851-147">La descripción de la matriz compleja es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="75851-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="75851-148">El número \_ de \_ elementos<2> campo es cero si la matriz es compatible.</span><span class="sxs-lookup"><span data-stu-id="75851-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="75851-149">La descripción del cumplimiento \_<> y la \_ Descripción de la varianza<> es un descriptor de correlación y tiene 4 o 6 bytes en función de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="75851-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="75851-150">Si la matriz tiene cumplimiento y/o varianza, la descripción del cumplimiento \_<> y/o la descripción de la varianza \_<> campos tienen descripciones válidas; de lo contrario, los cuatro primeros bytes del descriptor de correlación se establecen en 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="75851-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="75851-151">Las marcas, cuando están presentes, se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="75851-151">The flags, when present, are set to zero.</span></span>

 

 
