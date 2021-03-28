---
title: Enmascaramiento del registro de destino
description: Enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción. Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418913"
---
# <a name="destination-register-masking"></a><span data-ttu-id="a584c-104">Enmascaramiento del registro de destino</span><span class="sxs-lookup"><span data-stu-id="a584c-104">Destination Register Masking</span></span>

<span data-ttu-id="a584c-105">Enmascaramiento especifica qué componentes del registro de destino se actualizarán con el resultado de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="a584c-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="a584c-106">Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="a584c-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="a584c-107">DX9 \_ Graphics \_ referencia \_ ASM \_ vs \_ registros \_ modificadores \_ masking: esta sección contiene reglas para aplicar máscaras a los registros de destino.</span><span class="sxs-lookup"><span data-stu-id="a584c-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="a584c-108">\_ \_ Máscaras de registro de textura: los registros de textura tienen algunas reglas únicas.</span><span class="sxs-lookup"><span data-stu-id="a584c-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="a584c-109">Enmascaramiento del registro de destino</span><span class="sxs-lookup"><span data-stu-id="a584c-109">Destination Register Masking</span></span>

<span data-ttu-id="a584c-110">Como se muestra en la tabla siguiente, el enmascaramiento (donde es uno de los [registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)válidos del sombreador de vértices) se puede aplicar a los componentes individuales de los datos vectoriales.</span><span class="sxs-lookup"><span data-stu-id="a584c-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="a584c-111">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="a584c-111">Component modifier</span></span> | <span data-ttu-id="a584c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a584c-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="a584c-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="a584c-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="a584c-114">Máscara de destino</span><span class="sxs-lookup"><span data-stu-id="a584c-114">Destination mask</span></span> |



 

-   <span data-ttu-id="a584c-115">En general, la especificación de las máscaras de escritura del registro de destino es un buen estilo de codificación.</span><span class="sxs-lookup"><span data-stu-id="a584c-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="a584c-116">Facilita la lectura y el mantenimiento del código.</span><span class="sxs-lookup"><span data-stu-id="a584c-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="a584c-117">Se puede especificar cualquier combinación de componentes (incluido ninguno) siempre y cuando x preceda a y, y preceda a z, y z preceda a w.</span><span class="sxs-lookup"><span data-stu-id="a584c-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="a584c-118">Los registros de salida OPC y oFog deben usar solo una máscara.</span><span class="sxs-lookup"><span data-stu-id="a584c-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="a584c-119">Algunas instrucciones requieren que el registro de destino use una sola máscara de escritura: EXP, EXPP, log, logP, pow, RCP y RSQ.</span><span class="sxs-lookup"><span data-stu-id="a584c-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="a584c-120">En la versión 1,0, la instrucción FRC requería una de las siguientes combinaciones de máscara:. x o. y o. XY.</span><span class="sxs-lookup"><span data-stu-id="a584c-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="a584c-121">La versión 2,0 no tiene ninguna restricción de máscara.</span><span class="sxs-lookup"><span data-stu-id="a584c-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="a584c-122">sincos (requiere una de las siguientes combinaciones de máscara:. x o. y o. XYZ.</span><span class="sxs-lookup"><span data-stu-id="a584c-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="a584c-123">m3x2 requiere la máscara de escritura. XY.</span><span class="sxs-lookup"><span data-stu-id="a584c-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="a584c-124">M3x3 y m4x3 requieren la máscara de escritura. XYZ.</span><span class="sxs-lookup"><span data-stu-id="a584c-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="a584c-125">M3x4 y M4x4 requieren la máscara de escritura. XYZ o la máscara de escritura predeterminada (xyzw).</span><span class="sxs-lookup"><span data-stu-id="a584c-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="a584c-126">Máscaras de registro de textura</span><span class="sxs-lookup"><span data-stu-id="a584c-126">Texture Register Masks</span></span>

<span data-ttu-id="a584c-127">Las reglas de validación para usar modificadores en los registros de coordenadas de textura son más estrictas que las reglas de validación para otros registros.</span><span class="sxs-lookup"><span data-stu-id="a584c-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="a584c-128">Si se escribe oTn, también se deben escribir todos los registros anteriores (oTn-1 ~ oT0).</span><span class="sxs-lookup"><span data-stu-id="a584c-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="a584c-129">La máscara de escritura "combinada" para cualquier \# registro de OT debe ser exactamente una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a584c-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="a584c-130">.x</span><span class="sxs-lookup"><span data-stu-id="a584c-130">.x</span></span>
    -   <span data-ttu-id="a584c-131">. XY</span><span class="sxs-lookup"><span data-stu-id="a584c-131">.xy</span></span>
    -   <span data-ttu-id="a584c-132">. XYZ</span><span class="sxs-lookup"><span data-stu-id="a584c-132">.xyz</span></span>
    -   <span data-ttu-id="a584c-133">. xyzw (que equivale a no usar modificadores de componente)</span><span class="sxs-lookup"><span data-stu-id="a584c-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="a584c-134">Por ejemplo, un sombreador de vértices puede generar los registros de textura en instrucciones independientes.</span><span class="sxs-lookup"><span data-stu-id="a584c-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="a584c-135">O bien, se pueden combinar las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="a584c-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="a584c-136">Estas restricciones solo se aplican a los registros de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a584c-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a584c-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a584c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a584c-138">Modificadores de registro del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a584c-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




