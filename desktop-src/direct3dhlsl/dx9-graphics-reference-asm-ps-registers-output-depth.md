---
title: Registro de profundidad de salida
description: El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo \ 0.. 1 \ que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357754"
---
# <a name="output-depth-register"></a><span data-ttu-id="b1ecc-103">Registro de profundidad de salida</span><span class="sxs-lookup"><span data-stu-id="b1ecc-103">Output Depth Register</span></span>

<span data-ttu-id="b1ecc-104">El registro de profundidad de salida del sombreador de píxeles (oDepth) es un registro escalar de solo escritura con el intervalo \[ 0.. 1 \] que devuelve un nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="b1ecc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1ecc-105">Syntax</span></span>



| <span data-ttu-id="b1ecc-106">oDepth</span><span class="sxs-lookup"><span data-stu-id="b1ecc-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="b1ecc-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="b1ecc-107">Where:</span></span>



| <span data-ttu-id="b1ecc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1ecc-108">Name</span></span>   | <span data-ttu-id="b1ecc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1ecc-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="b1ecc-110">oDepth</span><span class="sxs-lookup"><span data-stu-id="b1ecc-110">oDepth</span></span> | <span data-ttu-id="b1ecc-111">Nuevo valor de profundidad para una prueba de profundidad en el búfer de estarcido de profundidad</span><span class="sxs-lookup"><span data-stu-id="b1ecc-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="b1ecc-112">Es importante tener en cuenta que la escritura en oDepth provoca la pérdida de los algoritmos de optimización de búfer de profundidad específicos del hardware (es decir, la jerarquía Z) que aceleran el rendimiento de las pruebas de profundidad.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="b1ecc-113">La replicación de origen swizzle (. x. \| y \| . z \| . w) es necesaria cuando se escribe en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="b1ecc-114">No se permiten las máscaras de escritura explícitas.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="b1ecc-115">La escritura en el registro oDepth reemplaza el valor de profundidad interpolada (y omite cualquier sesgo de profundidad/renderstates slopescale).</span><span class="sxs-lookup"><span data-stu-id="b1ecc-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="b1ecc-116">Si no se ha creado o conectado ningún búfer de profundidad al dispositivo, se omite la escritura en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="b1ecc-117">Si va a realizar el muestreo múltiple y escribe en oDepth, dado que el sombreador de píxeles solo se ejecuta una vez por píxel, el valor de profundidad se replica para todas las ubicaciones de submuestras tratadas.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="b1ecc-118">La prueba de profundidad sigue ocurriendo por ejemplo, pero no tiene un valor de profundidad por muestra en la comparación desde el sombreador de píxeles como si no hubiera escrito oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="b1ecc-119">Si una aplicación tiene un búfer de w establecido como su búfer de profundidad, debe tener en cuenta al escribir en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="b1ecc-120">Es posible que necesite enviar información del rango de w al sombreador de píxeles y calcular el rango de w para escalar los valores w escritos en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="b1ecc-121">\_ \_ restricciones de PS 2 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1ecc-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="b1ecc-122">oDepth solo se puede escribir con la instrucción [MOV-PS](mov---ps.md) y solo puede realizarse una vez.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="b1ecc-123">No se permite ningún modificador de origen al escribir en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="b1ecc-124">No se permite ningún modificador de instrucción cuando se escribe en oDepth.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="b1ecc-125">No se escribe en oDepth desde una construcción de control de flujo o cuando se usa predication.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="b1ecc-126">Restricciones de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1ecc-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="b1ecc-127">En el caso de PS \_ 3 \_ 0, los registros de salida \# se pueden escribir en cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="b1ecc-128">La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="b1ecc-129">Si no se produce una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador no lo escribió, el destino de representación correspondiente tampoco se actualiza.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="b1ecc-130">Si se escribe un subconjunto de los canales en un registro de salida, los valores no definidos se escribirán en los canales restantes.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="b1ecc-131">Puede escribir en oDepth dentro de control de flujo o predication, siempre y cuando todas las rutas de acceso posibles escriban en el registro.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="b1ecc-132">No puede realizar ningún cálculo de degradado (u operaciones que invoquen implícitamente los cálculos de degradado como [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían en función de la primitiva (por ejemplo: instrucciones de control de flujo dinámico).</span><span class="sxs-lookup"><span data-stu-id="b1ecc-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="b1ecc-133">La instrucción predication no se considera el control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="b1ecc-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1ecc-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1ecc-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1ecc-135">Registra</span><span class="sxs-lookup"><span data-stu-id="b1ecc-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




