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
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903740"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="4f1fd-103">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f1fd-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="4f1fd-104">El lenguaje de sombreado de alto nivel para DirectX implementa una serie de modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="4f1fd-105">Con HLSL, puede crear sombreadores programables similares a C para la canalización de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="4f1fd-106">Cada modelo de sombreador se basa en las capacidades del modelo antes de hacerlo, implementando más funcionalidad con menos restricciones.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-106">Each shader model builds on the capabilites of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="4f1fd-107">El modelo de sombreador 1 comenzó con DirectX 8 e incluye instrucciones de nivel de ensamblado y de tipo C.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="4f1fd-108">Este modelo tiene muchas limitaciones causadas por el hardware del sombreador programable inicial.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="4f1fd-109">El modelo de sombreador 2 y 3 se expande en gran medida en el número de instrucciones y los sombreadores de constantes podrían usar.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="4f1fd-110">Son mucho más eficaces que el modelo de sombreador 1, pero siguen teniendo algunas de las limitaciones existentes del primer modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="4f1fd-111">A partir de Windows Vista, el modelo de sombreador 4 es un rediseño completo.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="4f1fd-112">Permite instrucciones y constantes ilimitadas (dentro de las restricciones de hardware de la máquina), tiene objetos con plantilla para hacer que el muestreo de textura sea más limpio y más eficaz, y tiene el menor número de restricciones de cualquier modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="4f1fd-113">Sin embargo, requiere el Modelo de controlador de Windows que solo está disponible en el sistema operativo Windows Vista (o posterior).</span><span class="sxs-lookup"><span data-stu-id="4f1fd-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="4f1fd-114">Perfiles del sombreador</span><span class="sxs-lookup"><span data-stu-id="4f1fd-114">Shader Profiles</span></span>

<span data-ttu-id="4f1fd-115">Un perfil de sombreador es el destino para compilar un sombreador; en esta tabla se enumeran los perfiles del sombreador que son compatibles con cada modelo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1fd-116">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f1fd-116">Shader Model</span></span>                                       | <span data-ttu-id="4f1fd-117">Perfiles del sombreador</span><span class="sxs-lookup"><span data-stu-id="4f1fd-117">Shader Profiles</span></span>                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4f1fd-118">Modelo de sombreador 1</span><span class="sxs-lookup"><span data-stu-id="4f1fd-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="4f1fd-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4f1fd-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4f1fd-120">Modelo de sombreador 2</span><span class="sxs-lookup"><span data-stu-id="4f1fd-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="4f1fd-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 0, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1, PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 3, vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 0, vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1, vs \_ 4 \_ 0 nivel 9 3, \_ \_ \_ lib \_ 4 0 nivel 9 1, \_ \_ \_ \_ lib \_ 4 \_ \_ \_ \_ 0 nivel 9 3</span><span class="sxs-lookup"><span data-stu-id="4f1fd-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="4f1fd-122">Modelo de sombreador 3</span><span class="sxs-lookup"><span data-stu-id="4f1fd-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="4f1fd-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f1fd-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4f1fd-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4f1fd-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="4f1fd-125">CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 1, \_ vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4f1fd-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="4f1fd-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4f1fd-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="4f1fd-127">CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 0 \_ , vs \_ 5 \_ 0, lib \_ 5 \_ 0 (aunque GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 y vs \_ 4 \_ 1 se introdujeron en el modelo de sombreador 4,0, el modelo de sombreador 5 agrega compatibilidad con estos perfiles de sombreador para búferes estructurados y búferes de direcciones</span><span class="sxs-lookup"><span data-stu-id="4f1fd-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="4f1fd-128">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="4f1fd-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="4f1fd-129">CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4f1fd-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1fd-130">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="4f1fd-130">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="4f1fd-131">Direct3D 9 incorporó los modelos de sombreador 1, 2 y 3.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span><br/> <span data-ttu-id="4f1fd-132">Direct3D 10 presentó el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-132">Direct3D 10 introduced shader model 4.</span></span><br/> <span data-ttu-id="4f1fd-133">Direct3D 10,1 presentó el modelo de sombreador 4,1.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-133">Direct3D 10.1 introduced shader model 4.1.</span></span><br/> |



 

## <a name="effect-profiles"></a><span data-ttu-id="4f1fd-134">Perfiles de efectos</span><span class="sxs-lookup"><span data-stu-id="4f1fd-134">Effect Profiles</span></span>

<span data-ttu-id="4f1fd-135">Un perfil de efecto es el destino para compilar un efecto o sombreador; en esta tabla se enumeran los perfiles de efecto que son compatibles con cada versión de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1fd-136">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="4f1fd-136">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="4f1fd-137">Direct3D 9 incorporó los perfiles de marco de efecto FX \_ 1 \_ 0 y FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span><br/> <span data-ttu-id="4f1fd-138">Direct3D 10 presentó Effect-Framework Profile FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span><br/> <span data-ttu-id="4f1fd-139">Direct3D 10,1 incorporó Effect-Framework Profile FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span><br/> <span data-ttu-id="4f1fd-140">En Direct3D 11 se incorporó Effect-Framework Profile FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="4f1fd-141">Estos perfiles de efectos heredados están desusados.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4f1fd-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f1fd-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f1fd-143">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="4f1fd-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





