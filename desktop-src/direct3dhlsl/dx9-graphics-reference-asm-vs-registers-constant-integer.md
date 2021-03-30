---
title: Registro de entero constante (referencia de HLSL VS)
description: Los registros de enteros constantes solo se usan en bucle-vs y REP-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984047"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="694fb-103">Registro de entero constante (referencia de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="694fb-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="694fb-104">Los registros de enteros constantes solo se usan en [bucle-vs](loop---vs.md) y [REP-vs](rep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="694fb-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="694fb-105">Se pueden establecer mediante [defi-vs](defi---vs.md) o [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="694fb-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="694fb-106">Cuando se usa como argumento para la instrucción [de bucle vs](loop---vs.md) :</span><span class="sxs-lookup"><span data-stu-id="694fb-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="694fb-107">. x es el recuento de iteraciones.</span><span class="sxs-lookup"><span data-stu-id="694fb-107">.x is the iteration count.</span></span> <span data-ttu-id="694fb-108">([REP-vs](rep---vs.md) solo usa este componente).</span><span class="sxs-lookup"><span data-stu-id="694fb-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="694fb-109">. y es el valor inicial del contador de bucle.</span><span class="sxs-lookup"><span data-stu-id="694fb-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="694fb-110">. z es el paso de incremento para el contador de bucles.</span><span class="sxs-lookup"><span data-stu-id="694fb-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="694fb-111">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="694fb-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="694fb-112">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="694fb-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="694fb-113">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="694fb-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="694fb-114">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="694fb-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="694fb-115">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="694fb-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="694fb-116">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="694fb-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="694fb-117">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="694fb-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="694fb-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="694fb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="694fb-119">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="694fb-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 