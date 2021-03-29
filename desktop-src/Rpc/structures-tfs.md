---
title: Estructuras (RPC)
description: Descripción de varios tipos de estructuras en llamada a procedimiento remoto (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078097"
---
# <a name="structures-rpc"></a><span data-ttu-id="e2521-103">Estructuras (RPC)</span><span class="sxs-lookup"><span data-stu-id="e2521-103">Structures (RPC)</span></span>

<span data-ttu-id="e2521-104">Hay varias categorías de estructuras, progresivamente más complicadas en cuanto a las acciones necesarias para calcular las referencias.</span><span class="sxs-lookup"><span data-stu-id="e2521-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="e2521-105">Comienzan con una estructura simple que se puede copiar en bloque en su totalidad y continuar con una estructura compleja que tiene que ser servicio campo por campo.</span><span class="sxs-lookup"><span data-stu-id="e2521-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="e2521-106">Estructura simple</span><span class="sxs-lookup"><span data-stu-id="e2521-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="e2521-107">Estructura simple con punteros</span><span class="sxs-lookup"><span data-stu-id="e2521-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="e2521-108">Estructura compatible</span><span class="sxs-lookup"><span data-stu-id="e2521-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="e2521-109">Estructura compatible con punteros</span><span class="sxs-lookup"><span data-stu-id="e2521-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="e2521-110">Estructura variable compatible (con o sin punteros)</span><span class="sxs-lookup"><span data-stu-id="e2521-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="e2521-111">Estructura rígida</span><span class="sxs-lookup"><span data-stu-id="e2521-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="e2521-112">Estructura compleja</span><span class="sxs-lookup"><span data-stu-id="e2521-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="e2521-113">Descripción del diseño del miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="e2521-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="e2521-114">Cuando se comparan con las categorías de matriz, queda claro que solo se pueden describir las estructuras de hasta 64 KB de tamaño (el tamaño es para la parte plana de la estructura), es decir, no hay equivalentes de las matrices SM y LG.</span><span class="sxs-lookup"><span data-stu-id="e2521-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="e2521-115">**Miembros comunes a las estructuras**</span><span class="sxs-lookup"><span data-stu-id="e2521-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="e2521-116">**ecuación**</span><span class="sxs-lookup"><span data-stu-id="e2521-116">**alignment**</span></span>

    <span data-ttu-id="e2521-117">La alineación necesaria del búfer antes de calcular las referencias de la estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="e2521-118">Los valores válidos son 0, 1, 3 y 7 (la alineación real menos 1).</span><span class="sxs-lookup"><span data-stu-id="e2521-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="e2521-119">**tamaño de memoria \_**</span><span class="sxs-lookup"><span data-stu-id="e2521-119">**memory\_size**</span></span>

    <span data-ttu-id="e2521-120">Tamaño de la estructura en memoria en bytes; en el caso de las estructuras compatibles, este tamaño no incluye el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e2521-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="e2521-121">**desplazamiento \_ a la descripción de la \_ matriz \_**</span><span class="sxs-lookup"><span data-stu-id="e2521-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="e2521-122">Desplazamiento desde el puntero de cadena de formato actual a la descripción de la matriz compatible incluida en una estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="e2521-123">**diseño de miembros \_**</span><span class="sxs-lookup"><span data-stu-id="e2521-123">**member\_layout**</span></span>

    <span data-ttu-id="e2521-124">Descripción de cada elemento de la estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-124">Description of each element of the structure.</span></span> <span data-ttu-id="e2521-125">Las rutinas de NDR solo necesitan examinar esta parte de la cadena de formato de un tipo si se necesita la transformación endian o si el tipo es una estructura compleja.</span><span class="sxs-lookup"><span data-stu-id="e2521-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="e2521-126">**diseño de puntero \_**</span><span class="sxs-lookup"><span data-stu-id="e2521-126">**pointer\_layout**</span></span>

    <span data-ttu-id="e2521-127">Vea la sección de [diseño de puntero](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="e2521-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="e2521-128">Estructura simple</span><span class="sxs-lookup"><span data-stu-id="e2521-128">Simple Structure</span></span>

<span data-ttu-id="e2521-129">Una estructura simple solo contiene tipos base, matrices fijas y otras estructuras simples.</span><span class="sxs-lookup"><span data-stu-id="e2521-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="e2521-130">La característica principal de la estructura simple es que se puede copiar en bloque en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="e2521-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="e2521-131">Estructura simple con punteros</span><span class="sxs-lookup"><span data-stu-id="e2521-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="e2521-132">Una estructura simple con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y otras estructuras simples con punteros.</span><span class="sxs-lookup"><span data-stu-id="e2521-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="e2521-133">Dado que el diseño<> solo tendrá que visitarse al realizar una conversión orden, se coloca al final de la descripción.</span><span class="sxs-lookup"><span data-stu-id="e2521-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="e2521-134">Estructura compatible</span><span class="sxs-lookup"><span data-stu-id="e2521-134">Conformant Structure</span></span>

<span data-ttu-id="e2521-135">Una estructura compatible solo contiene los tipos base, las matrices fijas y las estructuras simples, y debe contener una cadena compatible o una matriz compatible.</span><span class="sxs-lookup"><span data-stu-id="e2521-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="e2521-136">En realidad, esta matriz puede estar contenida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="e2521-137">Estructura compatible con punteros</span><span class="sxs-lookup"><span data-stu-id="e2521-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="e2521-138">Una estructura compatible con punteros solo contiene tipos base, punteros, matrices fijas, estructuras simples y estructuras simples con punteros. una estructura compatible debe contener una matriz compatible.</span><span class="sxs-lookup"><span data-stu-id="e2521-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="e2521-139">En realidad, esta matriz puede estar incluida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="e2521-140">Estructura variable compatible (con o sin punteros)</span><span class="sxs-lookup"><span data-stu-id="e2521-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="e2521-141">Una estructura variable compatible solo contiene tipos simples, punteros, matrices fijas, estructuras simples y estructuras simples con punteros. una estructura variable ajustada debe contener una cadena compatible o una matriz de variación compatible.</span><span class="sxs-lookup"><span data-stu-id="e2521-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="e2521-142">En realidad, la matriz o cadena compatible puede estar contenida en otra estructura compatible o estructura compatible con punteros que está incrustado en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="e2521-143">Estructura rígida</span><span class="sxs-lookup"><span data-stu-id="e2521-143">Hard Structure</span></span>

<span data-ttu-id="e2521-144">La estructura de hardware era un concepto destinado a eliminar penalizaciones dependientes relacionadas con el procesamiento de estructuras complejas.</span><span class="sxs-lookup"><span data-stu-id="e2521-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="e2521-145">Se deriva de una observación de que una estructura compleja normalmente solo tiene una o dos condiciones que impiden la copia de bloques y, por lo tanto, se estropea su rendimiento en comparación con una estructura simple.</span><span class="sxs-lookup"><span data-stu-id="e2521-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="e2521-146">Los culpable suelen ser uniones o campos de enumeración.</span><span class="sxs-lookup"><span data-stu-id="e2521-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="e2521-147">Una estructura rígida es una estructura que tiene un enum16, un relleno en memoria o una Unión como último miembro.</span><span class="sxs-lookup"><span data-stu-id="e2521-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="e2521-148">Estos tres elementos impiden que la estructura caiga en una de las categorías de estructura anteriores, que disfrutan de una pequeña sobrecarga de interpretación y una posible optimización máxima, pero no la fuerzan en la categoría de estructura muy compleja.</span><span class="sxs-lookup"><span data-stu-id="e2521-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="e2521-149">Enum16 no debe hacer que los tamaños de memoria y de conexión de la estructura difieran.</span><span class="sxs-lookup"><span data-stu-id="e2521-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="e2521-150">La estructura no puede tener ninguna matriz compatible ni ningún puntero (a menos que forme parte de la Unión). los únicos miembros permitidos son los tipos base, las matrices fijas y las estructuras simples.</span><span class="sxs-lookup"><span data-stu-id="e2521-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="e2521-151">El campo de desplazamiento de enumeración \_<2> proporciona el desplazamiento desde el principio de la estructura en memoria hasta un enum16 si contiene uno; de lo contrario, el desplazamiento de enumeración \_<2> campo es – 1.</span><span class="sxs-lookup"><span data-stu-id="e2521-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="e2521-152">El \_ campo Copy size<2> proporciona el número total de bytes de la estructura, que se pueden copiar en bloque en el búfer o desde él.</span><span class="sxs-lookup"><span data-stu-id="e2521-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="e2521-153">Este total no incluye ninguna unión final ni ningún relleno en la memoria.</span><span class="sxs-lookup"><span data-stu-id="e2521-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="e2521-154">Este valor también es la cantidad con la que se debe incrementar el puntero de búfer después de la copia.</span><span class="sxs-lookup"><span data-stu-id="e2521-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="e2521-155">El \_ \_ campo de> copiar incr<2 es el número de bytes que debe incrementar el puntero de memoria después de la copia de bloques antes de controlar cualquier unión final.</span><span class="sxs-lookup"><span data-stu-id="e2521-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="e2521-156">Si se incrementa en esta cantidad (no en \_ el tamaño de copia<2> bytes), se produce un puntero de memoria adecuado a cualquier unión final.</span><span class="sxs-lookup"><span data-stu-id="e2521-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="e2521-157">Estructura compleja</span><span class="sxs-lookup"><span data-stu-id="e2521-157">Complex Structure</span></span>

<span data-ttu-id="e2521-158">Una estructura compleja es cualquier estructura que contenga uno o más campos que impidan que la estructura se copie en bloque o para la que se debe realizar una comprobación adicional durante el cálculo de referencias o la anulación de la serialización (por ejemplo, comprobaciones enlazadas en una enumeración).</span><span class="sxs-lookup"><span data-stu-id="e2521-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="e2521-159">Los siguientes tipos de NDR se encuentran en esta categoría:</span><span class="sxs-lookup"><span data-stu-id="e2521-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="e2521-160">[tipos simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (solo en plataformas de 64 bits), un entero con \[ [ **rango**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="e2521-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="e2521-161">relleno de alineación al final de la estructura</span><span class="sxs-lookup"><span data-stu-id="e2521-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="e2521-162">punteros de interfaz (se usan con un complejo incrustado)</span><span class="sxs-lookup"><span data-stu-id="e2521-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="e2521-163">punteros omitidos (que están relacionados con el \[ atributo [**Ignore**](/windows/desktop/Midl/ignore) \] y el \_ token ignore de FC)</span><span class="sxs-lookup"><span data-stu-id="e2521-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="e2521-164">matrices complejas, matrices variables, matrices de cadenas</span><span class="sxs-lookup"><span data-stu-id="e2521-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="e2521-165">matrices compatibles multidimensionales con al menos una dimensión no fija</span><span class="sxs-lookup"><span data-stu-id="e2521-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="e2521-166">uniones</span><span class="sxs-lookup"><span data-stu-id="e2521-166">unions</span></span>
-   <span data-ttu-id="e2521-167">elementos definidos con \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**representar \_ como**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ serialización de conexión**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ serialización de usuario**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="e2521-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="e2521-168">estructuras complejas incrustadas</span><span class="sxs-lookup"><span data-stu-id="e2521-168">embedded complex structures</span></span>
-   <span data-ttu-id="e2521-169">relleno al final de la estructura</span><span class="sxs-lookup"><span data-stu-id="e2521-169">padding at the end of the structure</span></span>

<span data-ttu-id="e2521-170">Una estructura compleja tiene la siguiente descripción de formato:</span><span class="sxs-lookup"><span data-stu-id="e2521-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="e2521-171">El \_ campo tamaño de memoria<2> es el tamaño de la estructura en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e2521-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="e2521-172">Si la estructura contiene una matriz compatible, el desplazamiento a la \_ \_ \_ \_ descripción de matriz compatible<2> campo proporciona el desplazamiento a la descripción de la matriz compatible; en caso contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="e2521-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="e2521-173">Si la estructura tiene punteros, el desplazamiento \_ al \_ diseño de puntero \_<2> campo proporciona el desplazamiento más allá del diseño de la estructura al diseño del puntero; de lo contrario, este campo es cero.</span><span class="sxs-lookup"><span data-stu-id="e2521-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="e2521-174">El \_ diseño de puntero<> campo de una estructura compleja se controla de forma ligeramente diferente que para otras estructuras.</span><span class="sxs-lookup"><span data-stu-id="e2521-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="e2521-175">El \_ campo<> de diseño de puntero de una estructura compleja solo contiene descripciones de los campos de puntero reales de la propia estructura.</span><span class="sxs-lookup"><span data-stu-id="e2521-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="e2521-176">Los punteros contenidos en las matrices, uniones o estructuras incrustadas no se describen en el campo<> de diseño de punteros de la estructura compleja \_ .</span><span class="sxs-lookup"><span data-stu-id="e2521-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="e2521-177">Esto contrasta con otras estructuras, que duplican la descripción de los punteros contenidos en matrices o estructuras incrustadas en su propio diseño de puntero \_<> campo también.</span><span class="sxs-lookup"><span data-stu-id="e2521-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="e2521-178">El formato de la distribución de punteros de una estructura compleja también es radicalmente diferente.</span><span class="sxs-lookup"><span data-stu-id="e2521-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="e2521-179">Dado que solo contiene descripciones de los miembros de puntero reales y porque se calculan las referencias de una estructura compleja y se anula la serialización de un campo cada vez, el \_ diseño de puntero<> campo contiene simplemente la descripción del puntero de todos los miembros de puntero.</span><span class="sxs-lookup"><span data-stu-id="e2521-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="e2521-180">No se inicia FC \_ PP y ninguno de los diseños de puntero habituales \_<> información.</span><span class="sxs-lookup"><span data-stu-id="e2521-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="e2521-181">Descripción del diseño del miembro de estructura</span><span class="sxs-lookup"><span data-stu-id="e2521-181">Structure Member Layout Description</span></span>

<span data-ttu-id="e2521-182">La descripción del diseño de una estructura contiene uno o varios de los siguientes caracteres de formato:</span><span class="sxs-lookup"><span data-stu-id="e2521-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="e2521-183">Cualquiera de los caracteres de tipo base, como FC \_ Char, etc.</span><span class="sxs-lookup"><span data-stu-id="e2521-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="e2521-184">Directivas de alineación.</span><span class="sxs-lookup"><span data-stu-id="e2521-184">Alignment directives.</span></span> <span data-ttu-id="e2521-185">Hay tres caracteres de formato que especifican la alineación del puntero de memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 y FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="e2521-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="e2521-186">También hay tokens de alineación de búfer, FC \_ ALIGNB2 a través de FC \_ ALIGNM8; no se usan.</span><span class="sxs-lookup"><span data-stu-id="e2521-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="e2521-187">Relleno de memoria.</span><span class="sxs-lookup"><span data-stu-id="e2521-187">Memory padding.</span></span> <span data-ttu-id="e2521-188">Esto solo se produce al final de la descripción de una estructura y denota el número de bytes de relleno en la memoria antes de la matriz compatible en la estructura: FC \_ STRUCTPADn, donde n es el número de bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="e2521-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="e2521-189">Cualquier tipo no base incrustado (tenga en cuenta, sin embargo, que una matriz compatible nunca se produce en el diseño de la estructura).</span><span class="sxs-lookup"><span data-stu-id="e2521-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="e2521-190">Tiene una descripción de 4 bytes:</span><span class="sxs-lookup"><span data-stu-id="e2521-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="e2521-191">donde no se garantiza que el desplazamiento tenga una alineación de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="e2521-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="e2521-192">\_el controlador de memoria<1> es un relleno necesario en la memoria antes del campo complejo.</span><span class="sxs-lookup"><span data-stu-id="e2521-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="e2521-193">offset \_ to \_ description<2> es un desplazamiento de tipo relativo al tipo incrustado.</span><span class="sxs-lookup"><span data-stu-id="e2521-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="e2521-194">También puede haber un controlador FC \_ antes del extremo FC de terminación \_ , si es necesario, para asegurarse de que la cadena de formato se alineará en un límite de 2 bytes después del final de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="e2521-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 