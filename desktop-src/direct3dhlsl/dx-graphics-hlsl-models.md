---
title: Modelos de sombreador frente a perfiles de sombreador
description: Modelos de sombreador frente a perfiles de sombreador
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119620"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="dd5d0-103">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="dd5d0-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="dd5d0-104">El lenguaje de sombreado de alto nivel para DirectX implementa una serie de modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="dd5d0-105">Con HLSL, puede crear sombreadores programables de tipo C para la canalización de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="dd5d0-106">Cada modelo de sombreador se basa en las funcionalidades del modelo anterior, implementando más funcionalidad con menos restricciones.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="dd5d0-107">El modelo de sombreador 1 se inició con DirectX 8 e incluyó instrucciones de nivel de ensamblado y de tipo C.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="dd5d0-108">Este modelo tiene muchas limitaciones causadas por hardware de sombreador programable temprano.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="dd5d0-109">El modelo de sombreador 2 y 3 se expandió en gran parte en el número de instrucciones, y los sombreadores de constantes podrían usar.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="dd5d0-110">Son mucho más eficaces que el modelo de sombreador 1, pero siguen teniendo algunas de las limitaciones existentes del primer modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="dd5d0-111">A partir de Windows Vista, el modelo 4 del sombreador es un rediseño completo.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="dd5d0-112">Permite instrucciones y constantes ilimitadas (dentro de las restricciones de hardware de la máquina), tiene objetos con plantilla para que el muestreo de textura sea más limpio y eficaz, y tiene las restricciones más mínimas de cualquier modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="dd5d0-113">Sin embargo, requiere la Modelo de controlador de Windows que solo está disponible en el sistema operativo Windows Vista (o posterior).</span><span class="sxs-lookup"><span data-stu-id="dd5d0-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="dd5d0-114">Perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="dd5d0-114">Shader Profiles</span></span>

<span data-ttu-id="dd5d0-115">Un perfil de sombreador es el destino para compilar un sombreador; En esta tabla se enumeran los perfiles de sombreador admitidos por cada modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="dd5d0-116">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dd5d0-116">Shader model</span></span>                                                   | <span data-ttu-id="dd5d0-117">Perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="dd5d0-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd5d0-118">Shader Model 1</span><span class="sxs-lookup"><span data-stu-id="dd5d0-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="dd5d0-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd5d0-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="dd5d0-120">Shader Model 2</span><span class="sxs-lookup"><span data-stu-id="dd5d0-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="dd5d0-121">ps \_ 2 \_ 0, ps \_ \_ 2 x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ \_ \_ 0 level 9 \_ 0, vs \_ 4 \_ 0 level \_ \_ 9 \_ 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 level \_ \_ 9 \_ 1, lib \_ 4 \_ 0 level \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dd5d0-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="dd5d0-122">Shader Model 3</span><span class="sxs-lookup"><span data-stu-id="dd5d0-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="dd5d0-123">ps \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd5d0-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="dd5d0-124">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="dd5d0-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="dd5d0-125">cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, \_ vs 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd5d0-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="dd5d0-126">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="dd5d0-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="dd5d0-127">cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (Aunque gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps \_ 4 \_ 1, vs 4 0 y vs 4 1 \_ \_ \_ \_ se introdujeron en el modelo de sombreador 4.0, el modelo de sombreador 5 agrega compatibilidad a estos perfiles de sombreador para búferes estructurados y búferes de direcciones de bytes).</span><span class="sxs-lookup"><span data-stu-id="dd5d0-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="dd5d0-128">Shader Model 6</span><span class="sxs-lookup"><span data-stu-id="dd5d0-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="dd5d0-129">cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dd5d0-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="dd5d0-130">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="dd5d0-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="dd5d0-131">Direct3D 9 introdujo los modelos de sombreador 1, 2 y 3.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="dd5d0-132">Direct3D 10 introdujo el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="dd5d0-133">Direct3D 10.1 introdujo el modelo de sombreador 4.1.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="dd5d0-134">Perfiles de efecto</span><span class="sxs-lookup"><span data-stu-id="dd5d0-134">Effect Profiles</span></span>

<span data-ttu-id="dd5d0-135">Un perfil de efecto es el destino para compilar un efecto o sombreador; En esta tabla se enumeran los perfiles de efecto admitidos por cada versión de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="dd5d0-136">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="dd5d0-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="dd5d0-137">Direct3D 9 introdujo los perfiles effect-framework fx \_ 1 \_ 0 y fx \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="dd5d0-138">Direct3D 10 introdujo effect-framework profile fx \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="dd5d0-139">Direct3D 10.1 introdujo effect-framework profile fx \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="dd5d0-140">Direct3D 11 introdujo effect-framework profile fx \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="dd5d0-141">Estos perfiles de efectos heredados están en desuso.</span><span class="sxs-lookup"><span data-stu-id="dd5d0-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dd5d0-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd5d0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd5d0-143">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="dd5d0-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





