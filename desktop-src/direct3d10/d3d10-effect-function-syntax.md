---
description: Una función Effect se escribe en HLSL y se declara con la sintaxis siguiente.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintaxis de la función Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496151"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="9fbac-103">Sintaxis de la función Effect (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="9fbac-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="9fbac-104">Una función Effect se escribe en HLSL y se declara con la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="9fbac-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fbac-105">Syntax</span></span>

<span data-ttu-id="9fbac-106">*ReturnType* *nombrefunción* ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="9fbac-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="9fbac-107">{</span><span class="sxs-lookup"><span data-stu-id="9fbac-107">{</span></span>

<dl> <span data-ttu-id="9fbac-108">\[ *Instrucciones* \]</span><span class="sxs-lookup"><span data-stu-id="9fbac-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="9fbac-109">};</span><span class="sxs-lookup"><span data-stu-id="9fbac-109">};</span></span>



| <span data-ttu-id="9fbac-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fbac-110">Name</span></span>         | <span data-ttu-id="9fbac-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fbac-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbac-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="9fbac-112">ReturnType</span></span>   | <span data-ttu-id="9fbac-113">Cualquier [tipo HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="9fbac-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="9fbac-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="9fbac-114">FunctionName</span></span> | <span data-ttu-id="9fbac-115">Cadena ASCII que identifica de forma única el nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9fbac-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="9fbac-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="9fbac-116">ArgumentList</span></span> | <span data-ttu-id="9fbac-117">Uno o más argumentos, separados por comas (vea [argumentos de función (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="9fbac-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="9fbac-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="9fbac-118">Statements</span></span>   | <span data-ttu-id="9fbac-119">Una o más instrucciones (vea [instrucciones (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) que componen el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="9fbac-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="9fbac-120">Si una función se define sin cuerpo, se considera que es un prototipo. y deben redefinirse con un cuerpo antes del uso.</span><span class="sxs-lookup"><span data-stu-id="9fbac-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="9fbac-121">Una función de efecto puede ser un sombreador o simplemente puede ser una función llamada por un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9fbac-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="9fbac-122">Una función se identifica de forma exclusiva por su nombre, los tipos de sus parámetros y la plataforma de destino; por lo tanto, las funciones se pueden sobrecargar.</span><span class="sxs-lookup"><span data-stu-id="9fbac-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="9fbac-123">Cualquier función HLSL válida debe ajustarse a este formato; para obtener una lista más detallada de la sintaxis de las funciones de HLSL, consulte [funciones (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9fbac-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="9fbac-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fbac-124">Example</span></span>

<span data-ttu-id="9fbac-125">El [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa un sombreador de píxeles y un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="9fbac-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="9fbac-126">La función de sombreador de píxeles se denomina RenderScenePS y se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="9fbac-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="9fbac-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fbac-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbac-128">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="9fbac-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
