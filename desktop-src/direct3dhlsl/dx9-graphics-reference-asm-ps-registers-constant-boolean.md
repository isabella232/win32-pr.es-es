---
title: Registro booleano constante (referencia de PS de HLSL)
description: Este registro es una colección de bits que se usa en las instrucciones de control de flujo estático (por ejemplo, si es bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793012"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="8c4bb-103">Registro booleano constante (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c4bb-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="8c4bb-104">Este registro es una colección de bits utilizada en las instrucciones de control de flujo estático (por ejemplo, [si es bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="8c4bb-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="8c4bb-105">Hay 16 de ellos, por lo tanto, un sombreador puede tener 16 condiciones de rama independientes.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="8c4bb-106">Se pueden establecer mediante [defb-PS](defb---ps.md) o [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="8c4bb-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="8c4bb-107">El comportamiento de las constantes del sombreador ha cambiado entre Direct3D 8 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="8c4bb-108">En Direct3D 9, las constantes establecidas con defx asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="8c4bb-109">La duración de una constante declarada con defx se limita solo a la ejecución de ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="8c4bb-110">Por el contrario, las constantes que se establecen mediante las SetXXXShaderConstantX de las API inicializan constantes en el espacio global.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="8c4bb-111">Las constantes en el espacio global no se copian en el espacio local (visible para el sombreador) hasta que se llama a SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="8c4bb-112">En Direct3D 8, las constantes establecidas con defx o las API asignan valores al espacio constante del sombreador.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="8c4bb-113">Cada vez que se ejecuta el sombreador, el sombreador actual usa las constantes independientemente de la técnica utilizada para establecerlas.</span><span class="sxs-lookup"><span data-stu-id="8c4bb-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="8c4bb-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8c4bb-114">Pixel shader versions</span></span>     | <span data-ttu-id="8c4bb-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="8c4bb-115">1\_1</span></span> | <span data-ttu-id="8c4bb-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="8c4bb-116">1\_2</span></span> | <span data-ttu-id="8c4bb-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8c4bb-117">1\_3</span></span> | <span data-ttu-id="8c4bb-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="8c4bb-118">1\_4</span></span> | <span data-ttu-id="8c4bb-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c4bb-119">2\_0</span></span> | <span data-ttu-id="8c4bb-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c4bb-120">2\_sw</span></span> | <span data-ttu-id="8c4bb-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8c4bb-121">2\_x</span></span> | <span data-ttu-id="8c4bb-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8c4bb-122">3\_0</span></span> | <span data-ttu-id="8c4bb-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8c4bb-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="8c4bb-124">Registro booleano constante</span><span class="sxs-lookup"><span data-stu-id="8c4bb-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="8c4bb-125">x</span><span class="sxs-lookup"><span data-stu-id="8c4bb-125">x</span></span>    | <span data-ttu-id="8c4bb-126">x</span><span class="sxs-lookup"><span data-stu-id="8c4bb-126">x</span></span>    | <span data-ttu-id="8c4bb-127">x</span><span class="sxs-lookup"><span data-stu-id="8c4bb-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="8c4bb-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c4bb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c4bb-129">Registra</span><span class="sxs-lookup"><span data-stu-id="8c4bb-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 