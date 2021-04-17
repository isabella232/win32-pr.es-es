---
description: Una variable de efecto se declara con la sintaxis siguiente.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxis de las variables de efectos (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423368"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="7c9c8-103">Sintaxis de las variables de efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7c9c8-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="7c9c8-104">Una variable de efecto se declara con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c9c8-105">Syntax</span></span>

<span data-ttu-id="7c9c8-106">*DataType* *VariableName* \[ : *SemanticName* \]  <  *Annotations* >;</span><span class="sxs-lookup"><span data-stu-id="7c9c8-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="7c9c8-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c9c8-107">Name</span></span>         | <span data-ttu-id="7c9c8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c9c8-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9c8-109">DataType</span><span class="sxs-lookup"><span data-stu-id="7c9c8-109">DataType</span></span>     | <span data-ttu-id="7c9c8-110">Cualquier tipo [básico](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) o de [textura](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9c8-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="7c9c8-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="7c9c8-111">VariableName</span></span> | <span data-ttu-id="7c9c8-112">Cadena ASCII que identifica de forma única el nombre de la variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="7c9c8-113">SemanticName</span><span class="sxs-lookup"><span data-stu-id="7c9c8-113">SemanticName</span></span> | <span data-ttu-id="7c9c8-114">Cadena ASCII que denota información adicional sobre cómo se debe usar una variable.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="7c9c8-115">Una semántica es una cadena ASCII que puede ser un valor de sistema predefinido o una cadena de usuario personalizado.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="7c9c8-116">Anotaciones</span><span class="sxs-lookup"><span data-stu-id="7c9c8-116">Annotations</span></span>  | <span data-ttu-id="7c9c8-117">Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="7c9c8-118">Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7c9c8-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="7c9c8-119">Una variable de efecto que se declara fuera de todas las funciones, se considera global en el ámbito; las variables declaradas dentro de una función son locales para esa función.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="7c9c8-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c9c8-120">Example</span></span>

<span data-ttu-id="7c9c8-121">El [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variables globales sin semántica para los colores de materiales, las propiedades de luz y las matrices de transformación.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="7c9c8-122">En este ejemplo se muestran las variables de efectos globales.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="7c9c8-123">En este ejemplo se muestran las variables de efecto que son locales para una función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="7c9c8-124">En este ejemplo se muestran los parámetros de función que tienen semántica.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="7c9c8-125">En este ejemplo se muestra cómo declarar una variable de textura.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="7c9c8-126">El muestreo de una textura se realiza con una muestra de textura.</span><span class="sxs-lookup"><span data-stu-id="7c9c8-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="7c9c8-127">Para configurar una muestra en un efecto, vea el [tipo de muestra](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7c9c8-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c9c8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c9c8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c9c8-129">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="7c9c8-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
