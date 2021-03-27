---
title: Sintaxis de la función Effect (Direct3D 11)
description: Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791685"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="c8e21-103">Sintaxis de la función Effect (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c8e21-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="c8e21-104">Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="c8e21-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e21-105">Syntax</span></span>

<span data-ttu-id="c8e21-106">*ReturnType* *nombrefunción* ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="c8e21-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="c8e21-107">{</span><span class="sxs-lookup"><span data-stu-id="c8e21-107">{</span></span>

<dl> <span data-ttu-id="c8e21-108">\[ *Instrucciones* \]</span><span class="sxs-lookup"><span data-stu-id="c8e21-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="c8e21-109">};</span><span class="sxs-lookup"><span data-stu-id="c8e21-109">};</span></span>



| <span data-ttu-id="c8e21-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="c8e21-110">Name</span></span>         | <span data-ttu-id="c8e21-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8e21-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e21-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="c8e21-112">ReturnType</span></span>   | <span data-ttu-id="c8e21-113">Cualquier [tipo HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="c8e21-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="c8e21-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="c8e21-114">FunctionName</span></span> | <span data-ttu-id="c8e21-115">Cadena ASCII que identifica de forma única el nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8e21-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="c8e21-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="c8e21-116">ArgumentList</span></span> | <span data-ttu-id="c8e21-117">Uno o más argumentos, separados por comas (vea [argumentos de función (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="c8e21-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="c8e21-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c8e21-118">Statements</span></span>   | <span data-ttu-id="c8e21-119">Una o más instrucciones (vea [instrucciones (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que componen el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="c8e21-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="c8e21-120">Si una función se define sin cuerpo, se considera que es un prototipo. y deben redefinirse con un cuerpo antes del uso.</span><span class="sxs-lookup"><span data-stu-id="c8e21-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="c8e21-121">Una función de efecto puede ser un sombreador o simplemente puede ser una función llamada por un sombreador.</span><span class="sxs-lookup"><span data-stu-id="c8e21-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="c8e21-122">Una función se identifica de forma exclusiva por su nombre, los tipos de sus parámetros y la plataforma de destino; por lo tanto, las funciones se pueden sobrecargar.</span><span class="sxs-lookup"><span data-stu-id="c8e21-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="c8e21-123">Cualquier función HLSL válida debe ajustarse a este formato; para obtener una lista más detallada de la sintaxis de las funciones de HLSL, consulte [funciones (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="c8e21-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="c8e21-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8e21-124">Example</span></span>

<span data-ttu-id="c8e21-125">El siguiente es un ejemplo de una función de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c8e21-125">The following is an example of a pixel shader function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c8e21-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8e21-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8e21-127">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="c8e21-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 