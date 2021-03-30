---
title: Registro de entero constante (referencia de PS de HLSL)
description: Los registros de enteros constantes solo se usan en loop-PS y REP-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984038"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="034a9-103">Registro de entero constante (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="034a9-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="034a9-104">Los registros de enteros constantes solo se usan en [Loop-PS](loop---ps.md) y [REP-PS](rep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="034a9-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="034a9-105">Se pueden establecer mediante [defi-PS](defi---ps.md) o [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="034a9-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="034a9-106">Cuando se usa como argumento para la instrucción [de bucle-PS](loop---ps.md) :</span><span class="sxs-lookup"><span data-stu-id="034a9-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="034a9-107">. x es el recuento de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="034a9-107">.x is the iteration count.</span></span> <span data-ttu-id="034a9-108">([REP-PS](rep---ps.md) usa solo este componente).</span><span class="sxs-lookup"><span data-stu-id="034a9-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="034a9-109">. y es el valor inicial del contador de bucle.</span><span class="sxs-lookup"><span data-stu-id="034a9-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="034a9-110">. z es el paso de incremento para el contador de bucles.</span><span class="sxs-lookup"><span data-stu-id="034a9-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="034a9-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="034a9-111">Pixel shader versions</span></span>     | <span data-ttu-id="034a9-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="034a9-112">1\_1</span></span> | <span data-ttu-id="034a9-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="034a9-113">1\_2</span></span> | <span data-ttu-id="034a9-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="034a9-114">1\_3</span></span> | <span data-ttu-id="034a9-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="034a9-115">1\_4</span></span> | <span data-ttu-id="034a9-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="034a9-116">2\_0</span></span> | <span data-ttu-id="034a9-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="034a9-117">2\_sw</span></span> | <span data-ttu-id="034a9-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="034a9-118">2\_x</span></span> | <span data-ttu-id="034a9-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="034a9-119">3\_0</span></span> | <span data-ttu-id="034a9-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="034a9-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="034a9-121">Registro de entero constante</span><span class="sxs-lookup"><span data-stu-id="034a9-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="034a9-122">x</span><span class="sxs-lookup"><span data-stu-id="034a9-122">x</span></span>    | <span data-ttu-id="034a9-123">x</span><span class="sxs-lookup"><span data-stu-id="034a9-123">x</span></span>    | <span data-ttu-id="034a9-124">x</span><span class="sxs-lookup"><span data-stu-id="034a9-124">x</span></span>     |



 

<span data-ttu-id="034a9-125">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="034a9-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="034a9-126">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="034a9-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="034a9-127">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="034a9-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="034a9-128">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="034a9-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="034a9-129">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="034a9-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="034a9-130">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="034a9-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="034a9-131">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="034a9-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="034a9-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="034a9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="034a9-133">Registra</span><span class="sxs-lookup"><span data-stu-id="034a9-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 