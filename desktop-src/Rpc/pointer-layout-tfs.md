---
title: Diseño de puntero
description: El diseño de puntero describe los punteros de una estructura o una matriz.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903721"
---
# <a name="pointer-layout"></a><span data-ttu-id="2c9af-103">Diseño de puntero</span><span class="sxs-lookup"><span data-stu-id="2c9af-103">Pointer Layout</span></span>

<span data-ttu-id="2c9af-104">El diseño de puntero describe los punteros de una estructura o una matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="2c9af-105"><> de diseño de puntero \_</span><span class="sxs-lookup"><span data-stu-id="2c9af-105">pointer\_layout<></span></span>

<span data-ttu-id="2c9af-106">Un \_<> campo de diseño de puntero consta de los caracteres de formato FC \_ PP FC \_ Pad seguido de una o varias descripciones de puntero, como se describe más adelante, y terminando con un \_ carácter de formato final de FC:</span><span class="sxs-lookup"><span data-stu-id="2c9af-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="2c9af-107">Un \_ \_<> campo de diseño de instancia de puntero es una cadena de formato que describe una o varias instancias de punteros.</span><span class="sxs-lookup"><span data-stu-id="2c9af-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="2c9af-108">En estos descriptores se utilizan los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c9af-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="2c9af-109">desplazamiento \_ en \_ memoria</span><span class="sxs-lookup"><span data-stu-id="2c9af-109">offset\_in\_memory</span></span>

    <span data-ttu-id="2c9af-110">Desplazamiento con signo de la ubicación del puntero en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c9af-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="2c9af-111">En el caso de un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles); en el caso de las matrices, el desplazamiento es desde el principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="2c9af-112">desplazamiento \_ en \_ búfer</span><span class="sxs-lookup"><span data-stu-id="2c9af-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="2c9af-113">Desplazamiento con signo en la ubicación del puntero en el búfer.</span><span class="sxs-lookup"><span data-stu-id="2c9af-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="2c9af-114">En el caso de un puntero que reside en una estructura, este desplazamiento es un desplazamiento negativo desde el final de la estructura (el final de la parte no conforme de las estructuras compatibles): para las matrices, el desplazamiento es desde el principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="2c9af-115">desplazamiento \_ a la \_ matriz</span><span class="sxs-lookup"><span data-stu-id="2c9af-115">offset\_to\_array</span></span>

    <span data-ttu-id="2c9af-116">Desplazamiento de una estructura envolvente a la matriz incrustada cuyos punteros se están controlando.</span><span class="sxs-lookup"><span data-stu-id="2c9af-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="2c9af-117">En el caso de las matrices de nivel superior, este campo siempre será cero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="2c9af-118">iteraciones</span><span class="sxs-lookup"><span data-stu-id="2c9af-118">iterations</span></span>

    <span data-ttu-id="2c9af-119">Número total de punteros que tienen el mismo diseño<> describe.</span><span class="sxs-lookup"><span data-stu-id="2c9af-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="2c9af-120">incremento</span><span class="sxs-lookup"><span data-stu-id="2c9af-120">increment</span></span>

    <span data-ttu-id="2c9af-121">Incremento entre punteros sucesivos durante una repetición.</span><span class="sxs-lookup"><span data-stu-id="2c9af-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="2c9af-122">número \_ de \_ punteros</span><span class="sxs-lookup"><span data-stu-id="2c9af-122">number\_of\_pointers</span></span>

    <span data-ttu-id="2c9af-123">Número de punteros diferentes en una instancia de repetición.</span><span class="sxs-lookup"><span data-stu-id="2c9af-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="2c9af-124">Descripción del puntero \_</span><span class="sxs-lookup"><span data-stu-id="2c9af-124">pointer\_description</span></span>

    <span data-ttu-id="2c9af-125">Descripción del puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-125">Pointer description.</span></span>

<span data-ttu-id="2c9af-126">Todos los diseños de instancia de puntero utilizan la siguiente instancia de puntero único \_<8>:</span><span class="sxs-lookup"><span data-stu-id="2c9af-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="2c9af-127">Los descriptores de instancia son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c9af-127">The following are instance descriptors:</span></span>

<span data-ttu-id="2c9af-128">**Instancia única de un puntero a un tipo simple:**</span><span class="sxs-lookup"><span data-stu-id="2c9af-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="2c9af-129">**Puntero de repetición fijo:**</span><span class="sxs-lookup"><span data-stu-id="2c9af-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="2c9af-130">**Puntero de repetición variable:**</span><span class="sxs-lookup"><span data-stu-id="2c9af-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="2c9af-131">En el caso de las instancias de repetición fija y de puntero de repetición variable, hay un conjunto de descripciones de desplazamiento y puntero para cada puntero en la instancia de repetición.</span><span class="sxs-lookup"><span data-stu-id="2c9af-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="2c9af-132">Problemas de diseño del diseño de punteros</span><span class="sxs-lookup"><span data-stu-id="2c9af-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="2c9af-133">En esta sección se abordan los problemas relacionados con el procesamiento de estructuras y punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="2c9af-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="2c9af-134">El problema es que el compilador genera diseños de puntero para estructuras y matrices con cierta redundancia.</span><span class="sxs-lookup"><span data-stu-id="2c9af-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="2c9af-135">Esto es beneficioso, porque la información es útil y, por ejemplo, una estructura compatible puede recorrer un diseño de puntero para atender todos los punteros de la estructura y de la matriz compatible que forma parte de la estructura compatible.</span><span class="sxs-lookup"><span data-stu-id="2c9af-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="2c9af-136">Sin embargo, existen algunas situaciones incrustadas que requieren que el motor NDR realice trabajo adicional para procesar todos los diseños de puntero en la secuencia adecuada, procesando cada puntero exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="2c9af-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="2c9af-137">Lo que genera el compilador</span><span class="sxs-lookup"><span data-stu-id="2c9af-137">What the Compiler Generates</span></span>

<span data-ttu-id="2c9af-138">Cada objeto descrito en esta sección tiene punteros, por lo que, por ejemplo, una estructura compatible tiene punteros en la parte de la estructura, así como en los elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="2c9af-139">El elemento es una estructura simple con un puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="2c9af-140">Estructura compatible, nivel único</span><span class="sxs-lookup"><span data-stu-id="2c9af-140">Conformant structure, single level</span></span>

    <span data-ttu-id="2c9af-141">El descriptor compatible tiene una parte PP donde se describen todos los punteros, tanto de la estructura como de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="2c9af-142">La lista de miembros tiene \_ un valor FC largo en lugar de un puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="2c9af-143">El descriptor de la matriz CARRAy tiene elementos mediante el uso de un complejo incrustado \_ y ningún descriptor de puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="2c9af-144">El elemento todavía tiene su descriptor de puntero único.</span><span class="sxs-lookup"><span data-stu-id="2c9af-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="2c9af-145">El diseño de puntero precede al diseño de miembro en una estructura compatible y descriptores de estructura simples.</span><span class="sxs-lookup"><span data-stu-id="2c9af-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="2c9af-146">Estructura compatible, dos o más niveles</span><span class="sxs-lookup"><span data-stu-id="2c9af-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="2c9af-147">La descripción de PP tiene punteros de todos los niveles.</span><span class="sxs-lookup"><span data-stu-id="2c9af-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="2c9af-148">Reutiliza la misma descripción de la matriz que la estructura compatible interna.</span><span class="sxs-lookup"><span data-stu-id="2c9af-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="2c9af-149">La lista de miembros tiene \_ un valor FC largo en lugar de un puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="2c9af-150">Una estructura incrustada se refiere al uso de un complejo incrustado.</span><span class="sxs-lookup"><span data-stu-id="2c9af-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="2c9af-151">El descriptor de estructura compatible se reutiliza tal cual.</span><span class="sxs-lookup"><span data-stu-id="2c9af-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="2c9af-152">El tamaño de la parte plana de la estructura también viene completo, lo que significa que el tamaño de la estructura de nivel superior incluiría el tamaño plano de la estructura insertada.</span><span class="sxs-lookup"><span data-stu-id="2c9af-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="2c9af-153">Estructura compleja, de un solo nivel</span><span class="sxs-lookup"><span data-stu-id="2c9af-153">Complex structure, single level</span></span>

    <span data-ttu-id="2c9af-154">Los miembros de puntero se marcan mediante el \_ puntero FC.</span><span class="sxs-lookup"><span data-stu-id="2c9af-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="2c9af-155">El diseño de puntero se simplifica de manera que hay un descriptor de puntero (4 bytes) para cada \_ entrada de puntero FC en la lista.</span><span class="sxs-lookup"><span data-stu-id="2c9af-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="2c9af-156">El diseño de puntero se recorre en paralelo con un recorrido de miembro, es decir, un \_ puntero FC hace que se procese la siguiente descripción del puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="2c9af-157">La matriz CARRAy tiene un diseño de puntero con todos los descriptores de la matriz y, a continuación, el elemento, mediante el uso de un complejo incrustado.</span><span class="sxs-lookup"><span data-stu-id="2c9af-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="2c9af-158">El descriptor de elemento se reutiliza.</span><span class="sxs-lookup"><span data-stu-id="2c9af-158">The element descriptor is reused.</span></span> <span data-ttu-id="2c9af-159">El tamaño de la parte plana de la estructura viene completo; en otras palabras, el tamaño plano de la estructura de nivel superior incluye el tamaño plano de la estructura insertada.</span><span class="sxs-lookup"><span data-stu-id="2c9af-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="2c9af-160">El diseño de miembro precede al diseño de puntero para estructuras complejas.</span><span class="sxs-lookup"><span data-stu-id="2c9af-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="2c9af-161">Por lo tanto, la generación de la descripción de la matriz compatible es diferente en función de si se trata de una matriz dentro de una estructura compatible o dentro de una estructura compleja.</span><span class="sxs-lookup"><span data-stu-id="2c9af-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="2c9af-162">Estructura compleja, 2 o más niveles, complejo en complejo</span><span class="sxs-lookup"><span data-stu-id="2c9af-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="2c9af-163">La estructura compleja de nivel superior tiene sus punteros de miembro, la estructura compleja incrustada tiene sus punteros de miembro.</span><span class="sxs-lookup"><span data-stu-id="2c9af-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="2c9af-164">Se reutiliza el descriptor de estructura compatible.</span><span class="sxs-lookup"><span data-stu-id="2c9af-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="2c9af-165">El descriptor de matriz de la parte superior es la matriz reutilizada de la estructura insertada.</span><span class="sxs-lookup"><span data-stu-id="2c9af-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="2c9af-166">Estructura compleja con una estructura compatible incrustada</span><span class="sxs-lookup"><span data-stu-id="2c9af-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="2c9af-167">Top = la estructura compatible con el nivel tiene sus punteros de miembro.</span><span class="sxs-lookup"><span data-stu-id="2c9af-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="2c9af-168">El descriptor de estructura compatible se reutiliza tal cual.</span><span class="sxs-lookup"><span data-stu-id="2c9af-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="2c9af-169">El descriptor de matriz se reutiliza de la estructura compatible con incrustación; en otras palabras, no tiene punteros en el descriptor de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="2c9af-170">El elemento tiene su descriptor de puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="2c9af-171">Matrices de estructuras con punteros</span><span class="sxs-lookup"><span data-stu-id="2c9af-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="2c9af-172">Una matriz de estructuras simples con punteros se genera como SMFARRAY o CARRAy dependiendo de si la matriz tiene un tamaño, pero en ambos casos tiene un diseño de puntero que se completa ( \_ repetición fija o repetición de variables \_ ).</span><span class="sxs-lookup"><span data-stu-id="2c9af-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="2c9af-173">El diseño del puntero viene antes del diseño de los miembros.</span><span class="sxs-lookup"><span data-stu-id="2c9af-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="2c9af-174">Una matriz de estructuras complejas con punteros se genera como una \_ matriz ficticia, independientemente de si está fija o tiene un tamaño, y en ambos casos, no tiene ningún diseño de puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="2c9af-175">Qué hace el motor NDR</span><span class="sxs-lookup"><span data-stu-id="2c9af-175">What the NDR Engine Does</span></span>

<span data-ttu-id="2c9af-176">En esta sección se describe el comportamiento del motor NDR.</span><span class="sxs-lookup"><span data-stu-id="2c9af-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="2c9af-177">**El paso de cálculo de referencias**</span><span class="sxs-lookup"><span data-stu-id="2c9af-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="2c9af-178">Estructuras compatibles y estructura compatible con Embedded.</span><span class="sxs-lookup"><span data-stu-id="2c9af-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="2c9af-179">La estructura de nivel superior se comporta como una estructura de un solo nivel.</span><span class="sxs-lookup"><span data-stu-id="2c9af-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="2c9af-180">Estructura compleja incrustada con matriz compatible</span><span class="sxs-lookup"><span data-stu-id="2c9af-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="2c9af-181">Cualquier estructura compleja obliga a que la estructura exterior sea una estructura compleja.</span><span class="sxs-lookup"><span data-stu-id="2c9af-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="2c9af-182">La estructura insertada nunca calcula las referencias de su matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="2c9af-183">Cada estructura siempre pasa por los punteros incrustados mediante la simple serialización de los miembros y un miembro que está pasando a ser un \_ puntero FC.</span><span class="sxs-lookup"><span data-stu-id="2c9af-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="2c9af-184">Estructura compleja con estructura compatible</span><span class="sxs-lookup"><span data-stu-id="2c9af-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="2c9af-185">La estructura compatible con el nivel superior incrustado calcula las referencias de la matriz compatible y de todos los punteros.</span><span class="sxs-lookup"><span data-stu-id="2c9af-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="2c9af-186">El motor NDR nunca desciende hasta estructuras compatibles de anidación más profundas si hay alguna; Esto simplifica la solución, ya que la estructura compatible es un objeto hoja en lo que respecta a la serialización de objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="2c9af-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="2c9af-187">La estructura compleja de nivel superior omite la serialización de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="2c9af-188">**Desserialización, bufsizing y liberación de pasos**</span><span class="sxs-lookup"><span data-stu-id="2c9af-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="2c9af-189">La anulación de la serialización es simétrica al cálculo de referencias; la primera operación que realiza para estructuras complejas es encontrar la ubicación de los punteros en el búfer mediante una llamada a la función **NdrComplexStructBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="2c9af-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="2c9af-190">A continuación, se anulan las referencias de los punteros en paralelo, lo que permite que el mismo esquema calcule las referencias de los punteros correctamente para su uso.</span><span class="sxs-lookup"><span data-stu-id="2c9af-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="2c9af-191">No debe haber ninguna confusión sobre los objetos y uniones de tamaño; la imagen de memoria no debe usarse para objetos y uniones con tamaño, solo para el contenido del búfer.</span><span class="sxs-lookup"><span data-stu-id="2c9af-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="2c9af-192">Las marcas que se usan para realizar la serialización y la desserialización correctamente se usan de la misma manera en bufsizing y liberan para asegurarse de que los punteros se recorren exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="2c9af-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="2c9af-193">**Orden Pass**</span><span class="sxs-lookup"><span data-stu-id="2c9af-193">**Endianess pass**</span></span>

<span data-ttu-id="2c9af-194">Al principio, el paso orden es algo similar a la serialización o la anulación de la serialización; se requieren dos pasos para procesar estructuras complejas.</span><span class="sxs-lookup"><span data-stu-id="2c9af-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="2c9af-195">El primer paso convierte la parte plana y busca la ubicación de los punteros en el búfer de forma similar a como bufsizing realiza esta operación para la anulación de la serialización.</span><span class="sxs-lookup"><span data-stu-id="2c9af-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="2c9af-196">A continuación, el segundo paso convierte los punteros.</span><span class="sxs-lookup"><span data-stu-id="2c9af-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="2c9af-197">Las pasadas orden difieren de la siguiente manera: cada estructura y cada miembro tiene que ser escalonado hasta que el miembro hoja o el elemento sea un tipo simple.</span><span class="sxs-lookup"><span data-stu-id="2c9af-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="2c9af-198">Esto no es lo mismo que quitar las referencias. en el caso de la desserialización, por ejemplo, nunca es necesario procesar las estructuras compatibles incrustadas en estructuras compatibles, o cualquier miembro de la estructura compatible, para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="2c9af-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="2c9af-199">Otro problema es que la conversión no es una operación idempotente; por lo tanto, el paso de desserialización podría rehacer la anulación de la serialización de algunas partes sin daños, mientras que la conversión se debe realizar en una base de tipo estrictamente una vez por tipo simple.</span><span class="sxs-lookup"><span data-stu-id="2c9af-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="2c9af-200">Por lo tanto, el algoritmo orden se puede resumir como sigue.</span><span class="sxs-lookup"><span data-stu-id="2c9af-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="2c9af-201">NDR tiene una noción de la estructura compatible de nivel superior y una marca para marcarla, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="2c9af-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="2c9af-202">Al caminar por primera vez, por ejemplo, para convertir la parte plana y obtener la ubicación de los punteros, esta noción no se utilizaría.</span><span class="sxs-lookup"><span data-stu-id="2c9af-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="2c9af-203">NDR desaparecerá a través de las partes planas de todos los niveles de estructuras y nunca al procesamiento de punteros.</span><span class="sxs-lookup"><span data-stu-id="2c9af-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="2c9af-204">Por último, el NDR tendría que convertir la matriz en el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2c9af-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="2c9af-205">Al recorrer la segunda vez, la marca se utilizaría para marcar el paso del puntero incrustado a fin de evitar que se escriban niveles más profundos de las estructuras compatibles y, después, la estructura compatible con el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2c9af-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="2c9af-206">De esta manera, la marca forzaría el comportamiento común de serialización y desserialización, lo que es evitar descender en niveles más profundos de estructuras conformes.</span><span class="sxs-lookup"><span data-stu-id="2c9af-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="2c9af-207">El segundo paso para estructuras complejas con matrices compatibles funciona de la siguiente manera: las estructuras complejas funcionan de la manera habitual. lo que significa que los niveles más profundos nunca verían o omitirían su tamaño compatible o sus matrices compatibles, y en su lugar simplemente irían a sus miembros sin tocar la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c9af-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="2c9af-208">En el caso de las estructuras complejas con estructuras compatibles, la estructura compatible debe ser consciente de si es de nivel superior y si está en una estructura compleja.</span><span class="sxs-lookup"><span data-stu-id="2c9af-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="2c9af-209">La parte plana de la matriz se procesa mediante la estructura compatible de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2c9af-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="2c9af-210">En el segundo paso, la estructura compatible con el nivel superior omitiría la parte plana y pasará por el diseño del puntero y devolverá.</span><span class="sxs-lookup"><span data-stu-id="2c9af-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="2c9af-211">La estructura más compleja de nivel superior omitiría su parte plana y omitiría también el diseño del puntero.</span><span class="sxs-lookup"><span data-stu-id="2c9af-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="2c9af-212">**El aspecto sólido de los recorridos de orden**</span><span class="sxs-lookup"><span data-stu-id="2c9af-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="2c9af-213">El recorrido de orden comprueba las condiciones habituales del búfer y realiza otras comprobaciones de una naturaleza no correlacionada.</span><span class="sxs-lookup"><span data-stu-id="2c9af-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="2c9af-214">Las comprobaciones dirigidas a los valores correlacionados (como el argumento de ajuste de tamaño frente al tamaño compatible) no se pueden realizar con este paso. se realizan posteriormente, cuando se anula el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="2c9af-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




