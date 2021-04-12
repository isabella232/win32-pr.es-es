---
title: Uniones RPC
description: Uniones encapsuladas y no encapsuladas y su formato con la llamada a procedimiento remoto (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487743"
---
# <a name="rpc-unions"></a><span data-ttu-id="17e3c-103">Uniones RPC</span><span class="sxs-lookup"><span data-stu-id="17e3c-103">RPC unions</span></span>

<span data-ttu-id="17e3c-104">Tanto las uniones encapsuladas como las no encapsuladas comparten el \_ formato de<> selector de ARM de la Unión común \_ :</span><span class="sxs-lookup"><span data-stu-id="17e3c-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="17e3c-105">El campo Union de la Unión \_<2> consta de dos partes.</span><span class="sxs-lookup"><span data-stu-id="17e3c-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="17e3c-106">Si la Unión es una Unión de estilo MIDL 1,0, los 4 bits superiores contienen la alineación del brazo de la Unión (alineación de la ARM más alineada).</span><span class="sxs-lookup"><span data-stu-id="17e3c-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="17e3c-107">De lo contrario, los cuatro bits superiores son cero.</span><span class="sxs-lookup"><span data-stu-id="17e3c-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="17e3c-108">Los 12 bits inferiores contienen el número de ramas de la Unión.</span><span class="sxs-lookup"><span data-stu-id="17e3c-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="17e3c-109">En otras palabras:</span><span class="sxs-lookup"><span data-stu-id="17e3c-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="17e3c-110">El desplazamiento \_ a la \_ Descripción de ARM \_<2> campos contienen un desplazamiento con signo relativo a la descripción del tipo de ARM.</span><span class="sxs-lookup"><span data-stu-id="17e3c-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="17e3c-111">Sin embargo, el campo se sobrecarga con optimización para tipos simples.</span><span class="sxs-lookup"><span data-stu-id="17e3c-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="17e3c-112">Para estos, el byte superior de este campo de desplazamiento es \_ el byte de Unión mágica de FC \_ \_ (0x80) y el byte inferior del Short es el tipo de carácter de formato real del brazo.</span><span class="sxs-lookup"><span data-stu-id="17e3c-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="17e3c-113">Como tal, hay dos intervalos para los valores de desplazamiento: "80 *XX*" significa que *XX* es una cadena de formato de tipo; y todo lo demás dentro del intervalo (80 FF..</span><span class="sxs-lookup"><span data-stu-id="17e3c-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="17e3c-114">7F FF) significa un desplazamiento real.</span><span class="sxs-lookup"><span data-stu-id="17e3c-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="17e3c-115">Esto hace que los desplazamientos del intervalo <80 00..</span><span class="sxs-lookup"><span data-stu-id="17e3c-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="17e3c-116">80 FF > no disponible como desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="17e3c-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="17e3c-117">El compilador comprueba que a partir de la versión de MIDL 5.1.164.</span><span class="sxs-lookup"><span data-stu-id="17e3c-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="17e3c-118">La descripción predeterminada de \_ arm \_<2> campo indica el tipo de ARM de Unión para el ARM predeterminado, si existe.</span><span class="sxs-lookup"><span data-stu-id="17e3c-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="17e3c-119">Si no hay ningún brazo predeterminado especificado para la Unión, el \_ campo Descripción predeterminada de arm \_<2> es 0xFFFF y se produce una excepción si el valor del modificador \_ es no coincide con ninguno de los valores de caso ARM.</span><span class="sxs-lookup"><span data-stu-id="17e3c-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="17e3c-120">Si se especifica el ARM predeterminado pero está vacío, el \_ campo Descripción predeterminada de arm \_<2> es cero.</span><span class="sxs-lookup"><span data-stu-id="17e3c-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="17e3c-121">De lo contrario, el \_ campo Descripción predeterminada de arm \_<2> tiene la misma semántica que el desplazamiento \_ para la descripción de \_ ARM \_<2> campos.</span><span class="sxs-lookup"><span data-stu-id="17e3c-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="17e3c-122">El siguiente es un resumen:</span><span class="sxs-lookup"><span data-stu-id="17e3c-122">The following is a summary:</span></span>

-   <span data-ttu-id="17e3c-123">0: valor predeterminado vacío</span><span class="sxs-lookup"><span data-stu-id="17e3c-123">0 - empty default</span></span>
-   <span data-ttu-id="17e3c-124">FFFF: sin valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="17e3c-124">FFFF - no default</span></span>
-   <span data-ttu-id="17e3c-125">80xx-tipo simple</span><span class="sxs-lookup"><span data-stu-id="17e3c-125">80xx - simple type</span></span>
-   <span data-ttu-id="17e3c-126">otro desplazamiento relativo</span><span class="sxs-lookup"><span data-stu-id="17e3c-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="17e3c-127">Uniones encapsuladas</span><span class="sxs-lookup"><span data-stu-id="17e3c-127">Encapsulated Unions</span></span>

<span data-ttu-id="17e3c-128">Una Unión encapsulada proviene de una sintaxis de Unión especial en IDL.</span><span class="sxs-lookup"><span data-stu-id="17e3c-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="17e3c-129">De hecho, una Unión encapsulada es una estructura de agrupación con un campo discriminante al principio de la estructura y la Unión como el único miembro.</span><span class="sxs-lookup"><span data-stu-id="17e3c-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="17e3c-130">El tipo de conmutador de una Unión encapsulada \_<1> campo tiene dos partes.</span><span class="sxs-lookup"><span data-stu-id="17e3c-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="17e3c-131">El recorte inferior proporciona el tipo de modificador real y el recorte superior proporciona el incremento de memoria para depurar, que es una cantidad que el puntero de memoria debe incrementarse para omitir el \_ campo, que incluye cualquier relleno entre el campo \_ () de la estructura construida por código auxiliar y el campo de unión real.</span><span class="sxs-lookup"><span data-stu-id="17e3c-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="17e3c-132">El \_ campo tamaño de memoria<2> es el tamaño de la Unión únicamente y es idéntico a las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="17e3c-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="17e3c-133">Para obtener el tamaño total de la estructura que contiene la Unión, agregue el \_ tamaño de memoria<2> al incremento de memoria que se va a depurar, es decir, al recorte superior del tipo de modificador \_<1> campo y, a continuación, alinearse mediante la alineación correspondiente al incremento.</span><span class="sxs-lookup"><span data-stu-id="17e3c-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="17e3c-134">Uniones no encapsuladas</span><span class="sxs-lookup"><span data-stu-id="17e3c-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="17e3c-135">Una Unión no encapsulada es una situación típica en la que una Unión es un argumento o un campo y el modificador es otro argumento o campo, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="17e3c-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="17e3c-136">Donde:</span><span class="sxs-lookup"><span data-stu-id="17e3c-136">Where:</span></span>

<span data-ttu-id="17e3c-137">El \_ tipo de modificador<1> campo es un carácter de formato para discriminante.</span><span class="sxs-lookup"><span data-stu-id="17e3c-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="17e3c-138">El modificador \_ es \_ un descriptor<> campo es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="17e3c-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="17e3c-139">Sin embargo, para el modificador \_ es \_ una descripción<>, si la Unión está incrustada en una estructura, el campo de desplazamiento del modificador \_ es \_ Description<> es el desplazamiento al modificador en el \_ campo de la posición de la Unión en la estructura (no desde el principio de la estructura).</span><span class="sxs-lookup"><span data-stu-id="17e3c-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="17e3c-140">El \_ campo desplazamiento a \_ tamaño \_ y descripción de \_ ARM \_<2> proporciona el desplazamiento al tamaño y la descripción de ARM de la Unión, que es idéntico al de las uniones encapsuladas y lo comparten todas las uniones no encapsuladas del mismo tipo:</span><span class="sxs-lookup"><span data-stu-id="17e3c-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 