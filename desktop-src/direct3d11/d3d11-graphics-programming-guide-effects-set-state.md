---
title: Establecer el estado del efecto (Direct3D 11)
description: Solo es necesario inicializar algunas constantes de efecto. Consulte el código básico para establecer variables de efecto en Direct3D 12.
ms.assetid: f94ba82e-fc67-4e4d-a49d-20e1163bdff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa27e817299df9398bd6fa1752e636162d9b97f7b886a372b71c5d0845dff41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953085"
---
# <a name="set-effect-state-direct3d-11"></a>Establecer el estado del efecto (Direct3D 11)

Solo es necesario inicializar algunas constantes de efecto. Una vez inicializado, el estado del efecto se establece en el dispositivo para todo el bucle de representación. Es necesario actualizar otras variables cada vez que se llama al bucle de representación. A continuación se muestra el código básico para establecer variables de efecto para cada uno de los tipos de variables.

Un efecto encapsula todo el estado de representación necesario para realizar un paso de representación. En cuanto a la API, hay tres tipos de estado encapsulados en un efecto.

-   [Estado constante](#constant-state)
-   [Estado del sombreador](#shader-state)
-   [Estado de textura](#texture-state)

## <a name="constant-state"></a>Estado constante

En primer lugar, declare variables en un efecto mediante tipos de datos HLSL.


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



En segundo lugar, declare variables en la aplicación que la aplicación pueda establecer y, a continuación, actualizará las variables de efecto.


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



En tercer lugar, use los métodos de actualización para establecer el valor de las variables de la aplicación en las variables de efecto.


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>Dos maneras de obtener el estado en una variable de efecto

Hay dos maneras de obtener el estado contenido en una variable de efecto. Dado un efecto que se ha cargado en la memoria.

Una manera es obtener el estado del sampler de [**un ID3DX11EffectVariable**](id3dx11effectvariable.md) que se ha convertido como una interfaz sampler.


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



La otra manera es obtener el estado del muestreador de [**un id3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate).


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



## <a name="shader-state"></a>Estado del sombreador

El estado del sombreador se declara y asigna en una técnica de efecto, dentro de un paso.


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



Esto funciona igual que lo haría si no usara ningún efecto. Hay tres llamadas, una para cada tipo de sombreador (vértice, geometría y píxel). El primero, SetVertexShader, llama a [**ID3D11DeviceContext::VSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader). CompileShader es una función de efecto especial que toma el perfil del sombreador (frente a 4 0) y el nombre de la función de sombreador de vértices \_ \_ (RenderVS). En otras palabras, cada una de estas llamadas a CompileShader compila su función de sombreador asociada y devuelve un puntero al sombreador compilado.

Tenga en cuenta que no se debe establecer todo el estado del sombreador. Este paso no incluye ninguna llamada a SetHullShader o SetDomainShader, lo que significa que los sombreadores de casco y dominio enlazados actualmente no se modificarán.

## <a name="texture-state"></a>Estado de textura

El estado de textura es un poco más complejo que establecer una variable, ya que los datos de textura no se leen simplemente como una variable, sino que se muestrea a partir de una textura. Por lo tanto, debe definir la variable de textura (al igual que una variable normal excepto que usa un tipo de textura) y debe definir las condiciones de muestreo. Este es un ejemplo de una declaración de variable de textura y la declaración de estado de muestreo correspondiente.


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



Este es un ejemplo de cómo establecer una textura desde una aplicación. En este ejemplo, la textura se almacena en los datos de malla que se cargaron cuando se creó el efecto.

El primer paso es obtener un puntero a la textura desde el efecto (desde la malla).


```
ID3D11EffectShaderResourceVariable* g_ptxDiffuse = NULL;

// Obtain variables
g_ptxDiffuse = g_pEffect11->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



El segundo paso es especificar una vista para acceder a la textura. La vista define una manera general de acceder a los datos desde el recurso de textura.


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



Desde la perspectiva de la aplicación, las vistas de acceso desordenado se controlan de forma similar a las vistas de recursos de sombreador. Sin embargo, en las funciones de sombreador de píxeles de efecto y sombreador de cálculo, los datos de la vista de acceso desordenado se leen o escriben directamente en ellos. No se puede muestrear desde una vista de acceso desordenado.

Para obtener más información sobre cómo ver recursos, vea [Recursos](overviews-direct3d-11-resources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un efecto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




