---
title: Interfaces y clases
description: La vinculación dinámica del sombreador usa las interfaces y las clases del lenguaje de sombreador de alto nivel (HLSL) que son sintácticamente similares a sus homólogos de C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421149"
---
# <a name="interfaces-and-classes"></a>Interfaces y clases

La vinculación dinámica del sombreador usa las interfaces y las clases del lenguaje de sombreador de alto nivel (HLSL) que son sintácticamente similares a sus homólogos de C++. Esto permite a los sombreadores hacer referencia a instancias de la interfaz abstracta en tiempo de compilación y dejar la resolución de esas instancias en clases concretas para la aplicación en tiempo de ejecución.

En las secciones siguientes se detalla cómo configurar un sombreador para utilizar interfaces y clases y cómo inicializar instancias de interfaz en el código de la aplicación.

-   [Declarar interfaces](#declaring-interfaces)
-   [Declarar clases](#declaring-classes)
-   [Declaraciones de instancia de interfaz en un sombreador](#interface-instance-declarations-in-a-shader)
-   [Declaraciones de instancia de clase en un sombreador](#class-instance-declarations-in-a-shader)
-   [Inicializar instancias de interfaz en una aplicación](#initializing-interface-instances-in-an-application)
-   [Temas relacionados](#related-topics)

## <a name="declaring-interfaces"></a>Declarar interfaces

Una interfaz funciona de forma similar a una clase base abstracta en C++. Una interfaz se declara en un sombreador mediante la palabra clave interface y solo contiene declaraciones de método. Todos los métodos declarados en una interfaz serán métodos virtuales en cualquier clase derivada de la interfaz. Las clases derivadas deben implementar todos los métodos declarados en una interfaz. Tenga en cuenta que las interfaces son la única manera de declarar métodos virtuales, no hay ninguna palabra clave virtual como en C++ y las clases connot declaran métodos virtuales.

En el siguiente código de sombreador de ejemplo se declaran dos interfaces.


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a>Declarar clases

Una clase se comporta de forma similar a las clases de C++. Una clase se declara con la palabra clave Class y puede contener variables y métodos de miembro. Una clase puede heredar de cero o de una clase y cero o más interfaces. Las clases deben implementar o heredar implementaciones para todas las interfaces en su cadena de herencia o no se pueden crear instancias de la clase.

En el siguiente código de sombreador de ejemplo se muestra cómo derivar una clase de una interfaz y de otra clase.


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a>Declaraciones de instancia de interfaz en un sombreador

Una instancia de interfaz actúa como marcador de posición para las instancias de clase que proporcionan una implementación de los métodos de la interfaz. El uso de una instancia de una interfaz permite que el código del sombreador llame a un método sin conocer qué implementación de ese método se invocará. El código del sombreador declara una o más instancias para cada interfaz que define. Estas instancias se usan en el código del sombreador de una manera similar a los punteros de clase base de C++.

En el siguiente código de sombreador de ejemplo se muestra la declaración de varias instancias de interfaz y su uso en el código del sombreador.


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a>Declaraciones de instancia de clase en un sombreador

Cada clase que se utilizará en lugar de una instancia de interfaz debe declararse como una variable en un búfer de constantes o ser creada por la aplicación en tiempo de ejecución mediante el método [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) . Las instancias de la interfaz se apuntarán a instancias de clase en el código de la aplicación. Se puede hacer referencia a las instancias de clase en el código del sombreador como cualquier otra variable, pero una clase que se deriva de una interfaz normalmente solo se usará con una instancia de interfaz y no se hará referencia a ella mediante el código del sombreador directamente.

En el siguiente código de sombreador de ejemplo se muestra la declaración de varias instancias de clase.


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a>Inicializar instancias de interfaz en una aplicación

Las instancias de interfaz se inicializan en el código de aplicación pasando una matriz de vinculación dinámica que contiene las asignaciones de interfaz a uno de los métodos SetShader de [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) .

Para crear una matriz de vinculación dinámica, siga estos pasos:

1.  Cree un objeto de vinculación de clase mediante [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Cree el sombreador que va a usar la vinculación de clases dinámicas, pasando el objeto de vinculación de clase como parámetro a la función de creación del sombreador.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Cree un objeto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) mediante la función [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Use el objeto de reflexión del sombreador para obtener el número de instancias de interfaz en el sombreador mediante el método [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Cree una matriz lo suficientemente grande como para contener el número de instancias de interfaz en el sombreador.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Determine el índice de la matriz que corresponde a cada instancia de interfaz mediante [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) y [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Obtenga una instancia de clase para cada objeto de clase derivado de una interfaz en el sombreador mediante [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Establezca instancias de la interfaz en instancias de clase estableciendo la entrada correspondiente en la matriz de vinculación dinámica.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Pase la matriz de vinculación dinámica como un parámetro a una llamada a SetShader.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>Temas relacionados

[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)