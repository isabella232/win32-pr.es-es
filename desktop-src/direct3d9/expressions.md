---
description: Las expresiones son instrucciones matemáticas o lógicas que se usan en el lado derecho de un signo igual. Hay muchos tipos de expresiones.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expresiones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677039"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="d4dd3-104">Expresiones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d4dd3-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="d4dd3-105">Las expresiones son instrucciones matemáticas o lógicas que se usan en el lado derecho de un signo igual.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="d4dd3-106">Hay muchos tipos de expresiones.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="d4dd3-107">Expresiones</span><span class="sxs-lookup"><span data-stu-id="d4dd3-107">Expressions</span></span>

1.  <span data-ttu-id="d4dd3-108">Referencia de variables</span><span class="sxs-lookup"><span data-stu-id="d4dd3-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="d4dd3-109">Escalar numérico</span><span class="sxs-lookup"><span data-stu-id="d4dd3-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="d4dd3-110">Expresión numérica</span><span class="sxs-lookup"><span data-stu-id="d4dd3-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="d4dd3-111">Aquí se admiten todas las expresiones HLL numéricas estándar.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="d4dd3-112">Constructor</span><span class="sxs-lookup"><span data-stu-id="d4dd3-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="d4dd3-113">Lista de inicializadores</span><span class="sxs-lookup"><span data-stu-id="d4dd3-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="d4dd3-114">Los valores escalares deben ser valores escalares literales.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="d4dd3-115">El número de inicializadores debe ser compatible con la variable (State) en el lado izquierdo del signo igual.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="d4dd3-116">Expresión OR</span><span class="sxs-lookup"><span data-stu-id="d4dd3-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="d4dd3-117">Los tokens deben ser compatibles con la variable (State) en el lado izquierdo del signo igual.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="d4dd3-118">Los tokens no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="d4dd3-119">NULL</span><span class="sxs-lookup"><span data-stu-id="d4dd3-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="d4dd3-120">NULL solo se puede asignar a un sombreador, un muestreador o un objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="d4dd3-121">Bloque de ensamblado</span><span class="sxs-lookup"><span data-stu-id="d4dd3-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="d4dd3-122">Los bloques de ensamblado de PS deben asignarse al estado u.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="d4dd3-123">Los bloques de ensamblado de VS deben asignarse al estado VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="d4dd3-124">Bloque de estado de muestra</span><span class="sxs-lookup"><span data-stu-id="d4dd3-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="d4dd3-125">Los bloques de estado de muestra son secuencias de estado de la fase de muestra sin indexar o asignaciones de textura.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="d4dd3-126">Los bloques de estado de muestra se deben asignar al estado de efecto de la muestra.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="d4dd3-127">Bloque de estado de estado de efecto</span><span class="sxs-lookup"><span data-stu-id="d4dd3-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="d4dd3-128">Los bloques de estado son secuencias de estado general.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="d4dd3-129">Los bloques de estado pueden estar anidados, pero no pueden contener referencias circulares.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="d4dd3-130">Los bloques de estado deben estar asignados al estado de efecto de STATEBLOCK.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="d4dd3-131">Compilación de HLSL</span><span class="sxs-lookup"><span data-stu-id="d4dd3-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="d4dd3-132">El destino de sombreador de vértices + \_ m n indica la versión de \_ D3DVS \_ (m, n) versión del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="d4dd3-133">El destino del sombreador de píxeles PS \_ m \_ n indica la versión \_ del sombreador de píxeles de la versión de D3DPS (m, n).</span><span class="sxs-lookup"><span data-stu-id="d4dd3-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="d4dd3-134">Las expresiones de compilación del lenguaje de alto nivel del sombreador de vértices solo se pueden asignar al estado del efecto VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="d4dd3-135">Las expresiones de compilación del lenguaje de alto nivel del sombreador de píxeles solo se pueden asignar al estado del efecto u.</span><span class="sxs-lookup"><span data-stu-id="d4dd3-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4dd3-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4dd3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4dd3-137">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="d4dd3-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



