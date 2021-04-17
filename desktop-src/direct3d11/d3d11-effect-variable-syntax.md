---
title: Sintaxis de las variables de efectos (Direct3D 11)
description: Una variable de efecto se declara con la sintaxis descrita en esta sección.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487754"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="736a5-103">Sintaxis de las variables de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="736a5-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="736a5-104">Una variable de efecto se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="736a5-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="736a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="736a5-105">Syntax</span></span>

<span data-ttu-id="736a5-106">Sintaxis básica:</span><span class="sxs-lookup"><span data-stu-id="736a5-106">Basic syntax:</span></span>

<span data-ttu-id="736a5-107">*DataType* *VariableName* \[ *: SemanticName* \]  <  *Annotations*  >  \[ = InitialValue \] ;</span><span class="sxs-lookup"><span data-stu-id="736a5-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="736a5-108">Consulte [Sintaxis de variables (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) para ver la sintaxis completa.</span><span class="sxs-lookup"><span data-stu-id="736a5-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="736a5-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="736a5-109">Name</span></span>         | <span data-ttu-id="736a5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="736a5-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="736a5-111">DataType</span><span class="sxs-lookup"><span data-stu-id="736a5-111">DataType</span></span>     | <span data-ttu-id="736a5-112">Cualquier vista de acceso [básica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [textura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), sin ordenar, sombreador o tipo de bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="736a5-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="736a5-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="736a5-113">VariableName</span></span> | <span data-ttu-id="736a5-114">Cadena ASCII que identifica de forma única el nombre de la variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="736a5-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="736a5-115">SemanticName</span><span class="sxs-lookup"><span data-stu-id="736a5-115">SemanticName</span></span> | <span data-ttu-id="736a5-116">Cadena ASCII que denota información adicional sobre cómo se debe usar una variable.</span><span class="sxs-lookup"><span data-stu-id="736a5-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="736a5-117">Una semántica es una cadena ASCII que puede ser un valor de sistema predefinido o una cadena de usuario personalizado.</span><span class="sxs-lookup"><span data-stu-id="736a5-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="736a5-118">Anotaciones</span><span class="sxs-lookup"><span data-stu-id="736a5-118">Annotations</span></span>  | <span data-ttu-id="736a5-119">Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite.</span><span class="sxs-lookup"><span data-stu-id="736a5-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="736a5-120">Para ver la sintaxis, vea [Sintaxis de anotación (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="736a5-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="736a5-121">InitialValue</span><span class="sxs-lookup"><span data-stu-id="736a5-121">InitialValue</span></span> | <span data-ttu-id="736a5-122">Valor predeterminado de la variable.</span><span class="sxs-lookup"><span data-stu-id="736a5-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="736a5-123">Una variable de efecto que se declara fuera de todas las funciones, se considera global en el ámbito; las variables declaradas dentro de una función son locales para esa función.</span><span class="sxs-lookup"><span data-stu-id="736a5-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="736a5-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="736a5-124">Example</span></span>

<span data-ttu-id="736a5-125">En este ejemplo se muestran variables numéricas de efectos globales.</span><span class="sxs-lookup"><span data-stu-id="736a5-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="736a5-126">En este ejemplo se muestran las variables de efecto que son locales para una función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="736a5-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="736a5-127">En este ejemplo se muestran los parámetros de función que tienen semántica.</span><span class="sxs-lookup"><span data-stu-id="736a5-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="736a5-128">En este ejemplo se muestra la declaración de una variable de textura global.</span><span class="sxs-lookup"><span data-stu-id="736a5-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="736a5-129">El muestreo de una textura se realiza con una muestra de textura.</span><span class="sxs-lookup"><span data-stu-id="736a5-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="736a5-130">Para configurar una muestra en un efecto, vea el [tipo de muestra](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="736a5-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="736a5-131">En este ejemplo se muestra la declaración de variables de vista de acceso no ordenada global.</span><span class="sxs-lookup"><span data-stu-id="736a5-131">This example illustrates declaring global unordered access view variables.</span></span>


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a><span data-ttu-id="736a5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="736a5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="736a5-133">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="736a5-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 