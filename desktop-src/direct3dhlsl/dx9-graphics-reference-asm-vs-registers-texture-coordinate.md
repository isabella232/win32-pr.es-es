---
title: Registro de coordenadas de textura (HLSL VS Reference)
description: Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértices.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149576"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="31819-103">Registro de coordenadas de textura (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="31819-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="31819-104">Este registro de salida del sombreador de vértices contiene coordenadas de textura por vértices.</span><span class="sxs-lookup"><span data-stu-id="31819-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="31819-105">Un registro consta de propiedades que determinan el comportamiento de cada registro.</span><span class="sxs-lookup"><span data-stu-id="31819-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="31819-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31819-106">Property</span></span>        | <span data-ttu-id="31819-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="31819-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="31819-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="31819-108">Name</span></span>            | <span data-ttu-id="31819-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="31819-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="31819-110">Count</span><span class="sxs-lookup"><span data-stu-id="31819-110">Count</span></span>           | <span data-ttu-id="31819-111">Ocho vectores</span><span class="sxs-lookup"><span data-stu-id="31819-111">Eight vectors</span></span> |
| <span data-ttu-id="31819-112">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="31819-112">I/O permissions</span></span> | <span data-ttu-id="31819-113">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="31819-113">Write-only</span></span>    |



 

<span data-ttu-id="31819-114">Los registros de coordenadas de texturas de salida son una matriz de registros de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="31819-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="31819-115">Los datos de registro se iteran y se usan como coordenadas de textura en las fases de muestreo de textura para proporcionar datos al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="31819-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="31819-116">Al escribir en un registro de coordenadas de textura, se recomienda pasar solo tantos valores de punto flotante como la dimensión del mapa de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="31819-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="31819-117">Controlan los valores que se pasan con un modificador.</span><span class="sxs-lookup"><span data-stu-id="31819-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="31819-118">Por ejemplo, use. XY para un mapa de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="31819-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="31819-119">Las marcas de canalización de vértices de función fija, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), se deben establecer en cero si se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="31819-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="31819-120">Los datos de vértices de objeto proporcionan coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="31819-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="31819-121">Los objetos que no usan texturas en mosaico suelen tener coordenadas de textura en el intervalo de \[ 0 a 1 \] .</span><span class="sxs-lookup"><span data-stu-id="31819-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="31819-122">Los objetos que usan texturas en mosaico, como Terrain, normalmente tienen coordenadas de textura que van desde \[ -n, + n, \] donde n puede ser cualquier número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="31819-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="31819-123">La interpolación de coordenadas de textura se realiza en los datos de vértices para la rasterización.</span><span class="sxs-lookup"><span data-stu-id="31819-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="31819-124">Durante la rasterización, las coordenadas de textura se interpolan entre los vértices del objeto, se modifican mediante el ajuste de textura y se escalan según el tamaño de la textura (también teniendo en cuenta los modos de direccionamiento de textura) para generar un índice de entero.</span><span class="sxs-lookup"><span data-stu-id="31819-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="31819-125">A continuación, el índice se utiliza para realizar una búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="31819-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="31819-126">Use el valor MaxTextureRepeat de [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para determinar el número de veces que se puede poner en mosaico una textura.</span><span class="sxs-lookup"><span data-stu-id="31819-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="31819-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31819-127">Example</span></span>

<span data-ttu-id="31819-128">Declare el registro de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="31819-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="31819-129">Copie las coordenadas de textura por vértice en el registro de salida.</span><span class="sxs-lookup"><span data-stu-id="31819-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="31819-130">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="31819-130">Vertex shader versions</span></span>      | <span data-ttu-id="31819-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="31819-131">1\_1</span></span> | <span data-ttu-id="31819-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31819-132">2\_0</span></span> | <span data-ttu-id="31819-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31819-133">2\_sw</span></span> | <span data-ttu-id="31819-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31819-134">2\_x</span></span> | <span data-ttu-id="31819-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31819-135">3\_0</span></span> | <span data-ttu-id="31819-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31819-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="31819-137">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="31819-137">Texture Coordinate Register</span></span> | <span data-ttu-id="31819-138">x</span><span class="sxs-lookup"><span data-stu-id="31819-138">x</span></span>    | <span data-ttu-id="31819-139">x</span><span class="sxs-lookup"><span data-stu-id="31819-139">x</span></span>    | <span data-ttu-id="31819-140">x</span><span class="sxs-lookup"><span data-stu-id="31819-140">x</span></span>     | <span data-ttu-id="31819-141">x</span><span class="sxs-lookup"><span data-stu-id="31819-141">x</span></span>    | <span data-ttu-id="31819-142">x</span><span class="sxs-lookup"><span data-stu-id="31819-142">x</span></span>    | <span data-ttu-id="31819-143">x</span><span class="sxs-lookup"><span data-stu-id="31819-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="31819-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31819-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31819-145">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="31819-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 