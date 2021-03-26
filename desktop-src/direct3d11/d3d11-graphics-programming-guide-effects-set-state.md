---
title: Establecer el estado del efecto (Direct3D 11)
description: Algunas constantes Effect solo deben inicializarse.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df65e164c2df01f78ae9ea9ab83a547b977335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531912"
---
# <a name="set-effect-state-direct3d-11"></a><span data-ttu-id="2ccea-103">Establecer el estado del efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2ccea-103">Set Effect State (Direct3D 11)</span></span>

<span data-ttu-id="2ccea-104">Algunas constantes Effect solo deben inicializarse.</span><span class="sxs-lookup"><span data-stu-id="2ccea-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="2ccea-105">Una vez inicializado, el estado del efecto se establece en el dispositivo para todo el bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="2ccea-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="2ccea-106">Es necesario actualizar otras variables cada vez que se llama al bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="2ccea-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="2ccea-107">A continuación se muestra el código básico para establecer las variables de efecto, para cada uno de los tipos de variables.</span><span class="sxs-lookup"><span data-stu-id="2ccea-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="2ccea-108">Un efecto encapsula todo el estado de representación necesario para realizar una fase de representación.</span><span class="sxs-lookup"><span data-stu-id="2ccea-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="2ccea-109">En lo que respecta a la API, hay tres tipos de estado encapsulados en un efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="2ccea-110">Estado constante</span><span class="sxs-lookup"><span data-stu-id="2ccea-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="2ccea-111">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="2ccea-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="2ccea-112">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="2ccea-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="2ccea-113">Estado constante</span><span class="sxs-lookup"><span data-stu-id="2ccea-113">Constant State</span></span>

<span data-ttu-id="2ccea-114">En primer lugar, declare las variables en un efecto mediante los tipos de datos de HLSL.</span><span class="sxs-lookup"><span data-stu-id="2ccea-114">First, declare variables in an effect using HLSL data types.</span></span>


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



<span data-ttu-id="2ccea-115">En segundo lugar, declare las variables de la aplicación que se pueden establecer en la aplicación y, a continuación, actualice las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D11CreateDevice()
{
  ...
    g_pLightDir = g_pEffect11->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect11->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect11->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect11->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect11->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect11->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect11->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect11->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



<span data-ttu-id="2ccea-116">En tercer lugar, use los métodos de actualización para establecer el valor de las variables de la aplicación en las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


```
           
OnD3D11FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="2ccea-117">Dos maneras de obtener el estado en una variable de efecto</span><span class="sxs-lookup"><span data-stu-id="2ccea-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="2ccea-118">Hay dos maneras de obtener el estado contenido en una variable de efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="2ccea-119">Dado un efecto que se ha cargado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2ccea-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="2ccea-120">Una manera es obtener el estado de la muestra de un [**ID3DX11EffectVariable**](id3dx11effectvariable.md) que se ha convertido en una interfaz de muestra.</span><span class="sxs-lookup"><span data-stu-id="2ccea-120">One way is to get the sampler state from an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) that has been cast as a sampler interface.</span></span>


```
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid() )
        hr = (l_pD3D11EffectVariable->GetBackingStore( 0, 
            &sampler_desc );
}
```



<span data-ttu-id="2ccea-121">La otra forma es obtener el estado de la muestra de un [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span><span class="sxs-lookup"><span data-stu-id="2ccea-121">The other way is to get the sampler state from an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).</span></span>


```
ID3D11SamplerState* l_ppSamplerState = NULL;
D3D11_SAMPLER_DESC sampler_desc;
ID3D11EffectSamplerVariable* l_pD3D11EffectVariable = NULL;
if( g_pEffect11 )
{
    l_pD3D11EffectVariable = g_pEffect11->GetVariableByName( "MeshTextureSampler" )->AsSampler();
    if( l_pD3D11EffectVariable->IsValid )
    {
        hr = l_pD3D11EffectVariable->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a><span data-ttu-id="2ccea-122">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="2ccea-122">Shader State</span></span>

<span data-ttu-id="2ccea-123">El estado del sombreador se declara y se asigna en una técnica de efecto, dentro de un paso.</span><span class="sxs-lookup"><span data-stu-id="2ccea-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


```
VertexShader vsRenderScene = CompileShader( vs_4_0, RenderSceneVS( 1, true, true );  
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( vsRenderScene );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



<span data-ttu-id="2ccea-124">Esto funciona igual que si no estuviera usando ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="2ccea-125">Hay tres llamadas, una para cada tipo de sombreador (vértice, geometría y píxel).</span><span class="sxs-lookup"><span data-stu-id="2ccea-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="2ccea-126">El primero, SetVertexShader, llama a [**ID3D11DeviceContext:: VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span><span class="sxs-lookup"><span data-stu-id="2ccea-126">The first one, SetVertexShader, calls [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader).</span></span> <span data-ttu-id="2ccea-127">CompileShader es una función especial de efecto que toma el perfil de sombreador (vs \_ 4 \_ 0) y el nombre de la función de sombreador de vértices (RenderVS).</span><span class="sxs-lookup"><span data-stu-id="2ccea-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="2ccea-128">En otras palabras, cada una de estas llamadas CompileShader compila su función de sombreador asociada y devuelve un puntero al sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="2ccea-128">In other words, each of these CompileShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

<span data-ttu-id="2ccea-129">Tenga en cuenta que no se debe establecer todo el estado del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ccea-129">Note that not all shader state must be set.</span></span> <span data-ttu-id="2ccea-130">Este paso no incluye ninguna llamada a SetHullShader o SetDomainShader, lo que significa que el casco y los sombreadores de dominio actualmente enlazados no se modificarán.</span><span class="sxs-lookup"><span data-stu-id="2ccea-130">This pass does not include any SetHullShader or SetDomainShader calls, meaning that the currently bound hull and domain shaders will be unchanged.</span></span>

## <a name="texture-state"></a><span data-ttu-id="2ccea-131">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="2ccea-131">Texture State</span></span>

<span data-ttu-id="2ccea-132">El estado de la textura es un poco más complejo que establecer una variable, ya que los datos de la textura no se leen simplemente como una variable, se muestra a partir de una textura.</span><span class="sxs-lookup"><span data-stu-id="2ccea-132">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="2ccea-133">Por lo tanto, debe definir la variable de textura (al igual que una variable normal, excepto que usa un tipo de textura) y debe definir las condiciones de muestreo.</span><span class="sxs-lookup"><span data-stu-id="2ccea-133">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="2ccea-134">A continuación se muestra un ejemplo de una declaración de variable de textura y la declaración de estado de muestreo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2ccea-134">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="2ccea-135">Este es un ejemplo de cómo establecer una textura desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ccea-135">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="2ccea-136">En este ejemplo, la textura se almacena en los datos de la malla, que se cargó al crear el efecto.</span><span class="sxs-lookup"><span data-stu-id="2ccea-136">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="2ccea-137">El primer paso es obtener un puntero a la textura del efecto (desde la malla).</span><span class="sxs-lookup"><span data-stu-id="2ccea-137">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="2ccea-138">El segundo paso consiste en especificar una vista para tener acceso a la textura.</span><span class="sxs-lookup"><span data-stu-id="2ccea-138">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="2ccea-139">La vista define una manera general de tener acceso a los datos del recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="2ccea-139">The view defines a general way to access the data from the texture resource.</span></span>


```
   
OnD3D11FrameRender()
{
  ID3D11ShaderResourceView* pDiffuseRV = NULL;

  ...
  pDiffuseRV = g_Mesh11.GetMaterial(pSubset->MaterialID)->pDiffuseRV11;
  g_ptxDiffuse->SetResource( pDiffuseRV );
  ...
}   
```



<span data-ttu-id="2ccea-140">Desde la perspectiva de la aplicación, las vistas de acceso desordenados se controlan de forma similar a las vistas de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="2ccea-140">From the application perspective, unordered access views are handled similarly to shader resource views.</span></span> <span data-ttu-id="2ccea-141">Sin embargo, en el efecto sombreador de píxeles y las funciones del sombreador de cálculo, los datos de vista de acceso desordenados se leen o se escriben directamente en.</span><span class="sxs-lookup"><span data-stu-id="2ccea-141">However, in the effect pixel shader and compute shader functions, unordered access view data is read from/written to directly.</span></span> <span data-ttu-id="2ccea-142">No se puede muestrear desde una vista de acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="2ccea-142">You cannot sample from an unordered access view.</span></span>

<span data-ttu-id="2ccea-143">Para obtener más información sobre cómo ver recursos, vea [recursos](overviews-direct3d-11-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2ccea-143">For more information about viewing resources, see [Resources](overviews-direct3d-11-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ccea-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ccea-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ccea-145">Representar un efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2ccea-145">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




