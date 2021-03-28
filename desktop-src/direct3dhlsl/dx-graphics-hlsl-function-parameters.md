---
title: Argumentos de la función
description: Una función toma uno o más argumentos de entrada; Use la siguiente sintaxis para declarar cada argumento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420190"
---
# <a name="function-arguments"></a><span data-ttu-id="110d4-103">Argumentos de la función</span><span class="sxs-lookup"><span data-stu-id="110d4-103">Function Arguments</span></span>

<span data-ttu-id="110d4-104">Una función toma uno o más argumentos de entrada; Use la siguiente sintaxis para declarar cada argumento.</span><span class="sxs-lookup"><span data-stu-id="110d4-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="110d4-105">**\[InputModifier \] nombre de tipo \[ : semántico \] \[ InterpolationModifier \] \[ = inicializadores\]**</span><span class="sxs-lookup"><span data-stu-id="110d4-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="110d4-106">\[Nombre de tipo de modificador \] \[ : semántico \] \[ : modificador de interpolación \] \[ = inicializadores\]</span><span class="sxs-lookup"><span data-stu-id="110d4-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="110d4-107">Si hay varios argumentos de función, se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="110d4-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="110d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="110d4-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="110d4-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="110d4-109">Item</span></span></th>
<th><span data-ttu-id="110d4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="110d4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="110d4-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="110d4-112">Término opcional que identifica un argumento como una entrada, una salida o ambas cosas.</span><span class="sxs-lookup"><span data-stu-id="110d4-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="110d4-113">Value</span><span class="sxs-lookup"><span data-stu-id="110d4-113">Value</span></span></td>
<td><span data-ttu-id="110d4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="110d4-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="110d4-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="110d4-116">Solo entrada</span><span class="sxs-lookup"><span data-stu-id="110d4-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="110d4-117"><strong>Inout</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="110d4-118">Entrada y salida</span><span class="sxs-lookup"><span data-stu-id="110d4-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="110d4-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="110d4-120">Solo salida</span><span class="sxs-lookup"><span data-stu-id="110d4-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="110d4-121"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="110d4-122">Datos constantes de solo entrada</span><span class="sxs-lookup"><span data-stu-id="110d4-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="110d4-123">Los parámetros siempre se pasan por valor.</span><span class="sxs-lookup"><span data-stu-id="110d4-123">Parameters are always passed by value.</span></span> <span data-ttu-id="110d4-124">en indica que el valor del parámetro se debe copiar en desde la aplicación que realiza la llamada antes de que comience la función.</span><span class="sxs-lookup"><span data-stu-id="110d4-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="110d4-125">out indica que el último valor del parámetro debe copiarse y devolverse a la aplicación que realiza la llamada cuando la función devuelve.</span><span class="sxs-lookup"><span data-stu-id="110d4-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="110d4-126">Inout es una abreviatura para especificar ambos.</span><span class="sxs-lookup"><span data-stu-id="110d4-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="110d4-127">Un valor uniforme procede de un registro constante; cada sombreador de vértices o invocación del sombreador de píxeles verá el mismo valor inicial para una variable uniforme.</span><span class="sxs-lookup"><span data-stu-id="110d4-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="110d4-128">Las variables globales se tratan como si se declararan uniformes.</span><span class="sxs-lookup"><span data-stu-id="110d4-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="110d4-129">En el caso de las funciones que no son de nivel superior, Uniform es sinónimo de <strong>en</strong>.</span><span class="sxs-lookup"><span data-stu-id="110d4-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="110d4-130">Si no se especifica ningún uso de parámetro, se supone que el uso del parámetro está <strong>en</strong>.</span><span class="sxs-lookup"><span data-stu-id="110d4-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="110d4-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Automáticamente</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="110d4-132">El tipo de argumento; puede ser cualquier <a href="dx-graphics-hlsl-data-types.md">tipo</a>HLSL válido.</span><span class="sxs-lookup"><span data-stu-id="110d4-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="110d4-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="110d4-134">Cadena ASCII que identifica de forma única el nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="110d4-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="110d4-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semántica</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="110d4-136">Cadena opcional que identifica el uso previsto de los datos (vea <a href="dx-graphics-hlsl-semantics.md">semántica (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="110d4-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="110d4-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="110d4-138"><a href="dx-graphics-hlsl-struct.md">Modificador de interpolación</a> opcional que permite a un sombreador determinar el método de interpolación.</span><span class="sxs-lookup"><span data-stu-id="110d4-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="110d4-139">Un modificador de interpolación en un argumento de función solo se aplica a un argumento que se usa como entrada para una función de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="110d4-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="110d4-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inicializadores</strong></span><span class="sxs-lookup"><span data-stu-id="110d4-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="110d4-141">Valores opcionales para la inicialización; se requieren varios valores para inicializar los tipos de datos de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="110d4-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="110d4-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="110d4-142">Remarks</span></span>

<span data-ttu-id="110d4-143">Los argumentos de función se enumeran en una lista de argumentos separados por comas en una declaración de función.</span><span class="sxs-lookup"><span data-stu-id="110d4-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="110d4-144">Como en las funciones de C, cada argumento debe tener un nombre de parámetro y un tipo declarados; un argumento para una función HLSL puede incluir opcionalmente una semántica, un valor inicial y una entrada de sombreador de píxeles puede incluir un tipo de interpolación.</span><span class="sxs-lookup"><span data-stu-id="110d4-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="110d4-145">El *tipo* de un argumento de función puede ser una estructura, que podría incluir un modificador de interpolación por miembro.</span><span class="sxs-lookup"><span data-stu-id="110d4-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="110d4-146">Si el argumento de función también tiene un modificador de interpolación, el modificador de argumento de función reemplaza los modificadores de interpolación declarados en el tipo.</span><span class="sxs-lookup"><span data-stu-id="110d4-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="110d4-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="110d4-147">Examples</span></span>

<span data-ttu-id="110d4-148">En este ejemplo (del [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) se muestran entradas uniformes y no uniformes para una función de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="110d4-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="110d4-149">Este ejemplo (del [ejemplo ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) utiliza una estructura de entrada para pasar argumentos a una función de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="110d4-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="110d4-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="110d4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="110d4-151">Funciones (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="110d4-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





