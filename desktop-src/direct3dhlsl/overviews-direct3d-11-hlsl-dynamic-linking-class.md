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
# <a name="interfaces-and-classes"></a><span data-ttu-id="6a789-103">Interfaces y clases</span><span class="sxs-lookup"><span data-stu-id="6a789-103">Interfaces and classes</span></span>

<span data-ttu-id="6a789-104">La vinculación dinámica del sombreador usa las interfaces y las clases del lenguaje de sombreador de alto nivel (HLSL) que son sintácticamente similares a sus homólogos de C++.</span><span class="sxs-lookup"><span data-stu-id="6a789-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="6a789-105">Esto permite a los sombreadores hacer referencia a instancias de la interfaz abstracta en tiempo de compilación y dejar la resolución de esas instancias en clases concretas para la aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6a789-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="6a789-106">En las secciones siguientes se detalla cómo configurar un sombreador para utilizar interfaces y clases y cómo inicializar instancias de interfaz en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a789-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="6a789-107">Declarar interfaces</span><span class="sxs-lookup"><span data-stu-id="6a789-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="6a789-108">Declarar clases</span><span class="sxs-lookup"><span data-stu-id="6a789-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="6a789-109">Declaraciones de instancia de interfaz en un sombreador</span><span class="sxs-lookup"><span data-stu-id="6a789-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="6a789-110">Declaraciones de instancia de clase en un sombreador</span><span class="sxs-lookup"><span data-stu-id="6a789-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="6a789-111">Inicializar instancias de interfaz en una aplicación</span><span class="sxs-lookup"><span data-stu-id="6a789-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="6a789-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a789-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="6a789-113">Declarar interfaces</span><span class="sxs-lookup"><span data-stu-id="6a789-113">Declaring interfaces</span></span>

<span data-ttu-id="6a789-114">Una interfaz funciona de forma similar a una clase base abstracta en C++.</span><span class="sxs-lookup"><span data-stu-id="6a789-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="6a789-115">Una interfaz se declara en un sombreador mediante la palabra clave interface y solo contiene declaraciones de método.</span><span class="sxs-lookup"><span data-stu-id="6a789-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="6a789-116">Todos los métodos declarados en una interfaz serán métodos virtuales en cualquier clase derivada de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a789-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="6a789-117">Las clases derivadas deben implementar todos los métodos declarados en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a789-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="6a789-118">Tenga en cuenta que las interfaces son la única manera de declarar métodos virtuales, no hay ninguna palabra clave virtual como en C++ y las clases connot declaran métodos virtuales.</span><span class="sxs-lookup"><span data-stu-id="6a789-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="6a789-119">En el siguiente código de sombreador de ejemplo se declaran dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="6a789-119">The following example shader code declares two interfaces.</span></span>


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



## <a name="declaring-classes"></a><span data-ttu-id="6a789-120">Declarar clases</span><span class="sxs-lookup"><span data-stu-id="6a789-120">Declaring Classes</span></span>

<span data-ttu-id="6a789-121">Una clase se comporta de forma similar a las clases de C++.</span><span class="sxs-lookup"><span data-stu-id="6a789-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="6a789-122">Una clase se declara con la palabra clave Class y puede contener variables y métodos de miembro.</span><span class="sxs-lookup"><span data-stu-id="6a789-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="6a789-123">Una clase puede heredar de cero o de una clase y cero o más interfaces.</span><span class="sxs-lookup"><span data-stu-id="6a789-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="6a789-124">Las clases deben implementar o heredar implementaciones para todas las interfaces en su cadena de herencia o no se pueden crear instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="6a789-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="6a789-125">En el siguiente código de sombreador de ejemplo se muestra cómo derivar una clase de una interfaz y de otra clase.</span><span class="sxs-lookup"><span data-stu-id="6a789-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


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



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="6a789-126">Declaraciones de instancia de interfaz en un sombreador</span><span class="sxs-lookup"><span data-stu-id="6a789-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="6a789-127">Una instancia de interfaz actúa como marcador de posición para las instancias de clase que proporcionan una implementación de los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6a789-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="6a789-128">El uso de una instancia de una interfaz permite que el código del sombreador llame a un método sin conocer qué implementación de ese método se invocará.</span><span class="sxs-lookup"><span data-stu-id="6a789-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="6a789-129">El código del sombreador declara una o más instancias para cada interfaz que define.</span><span class="sxs-lookup"><span data-stu-id="6a789-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="6a789-130">Estas instancias se usan en el código del sombreador de una manera similar a los punteros de clase base de C++.</span><span class="sxs-lookup"><span data-stu-id="6a789-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="6a789-131">En el siguiente código de sombreador de ejemplo se muestra la declaración de varias instancias de interfaz y su uso en el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a789-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


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



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="6a789-132">Declaraciones de instancia de clase en un sombreador</span><span class="sxs-lookup"><span data-stu-id="6a789-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="6a789-133">Cada clase que se utilizará en lugar de una instancia de interfaz debe declararse como una variable en un búfer de constantes o ser creada por la aplicación en tiempo de ejecución mediante el método [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) .</span><span class="sxs-lookup"><span data-stu-id="6a789-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="6a789-134">Las instancias de la interfaz se apuntarán a instancias de clase en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a789-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="6a789-135">Se puede hacer referencia a las instancias de clase en el código del sombreador como cualquier otra variable, pero una clase que se deriva de una interfaz normalmente solo se usará con una instancia de interfaz y no se hará referencia a ella mediante el código del sombreador directamente.</span><span class="sxs-lookup"><span data-stu-id="6a789-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="6a789-136">En el siguiente código de sombreador de ejemplo se muestra la declaración de varias instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="6a789-136">The following example shader code illustrates declaring several class instances.</span></span>


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



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="6a789-137">Inicializar instancias de interfaz en una aplicación</span><span class="sxs-lookup"><span data-stu-id="6a789-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="6a789-138">Las instancias de interfaz se inicializan en el código de aplicación pasando una matriz de vinculación dinámica que contiene las asignaciones de interfaz a uno de los métodos SetShader de [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="6a789-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="6a789-139">Para crear una matriz de vinculación dinámica, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6a789-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="6a789-140">Cree un objeto de vinculación de clase mediante [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span><span class="sxs-lookup"><span data-stu-id="6a789-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="6a789-141">Cree el sombreador que va a usar la vinculación de clases dinámicas, pasando el objeto de vinculación de clase como parámetro a la función de creación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a789-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="6a789-142">Cree un objeto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) mediante la función [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="6a789-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="6a789-143">Use el objeto de reflexión del sombreador para obtener el número de instancias de interfaz en el sombreador mediante el método [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .</span><span class="sxs-lookup"><span data-stu-id="6a789-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="6a789-144">Cree una matriz lo suficientemente grande como para contener el número de instancias de interfaz en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a789-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="6a789-145">Determine el índice de la matriz que corresponde a cada instancia de interfaz mediante [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) y [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="6a789-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="6a789-146">Obtenga una instancia de clase para cada objeto de clase derivado de una interfaz en el sombreador mediante [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span><span class="sxs-lookup"><span data-stu-id="6a789-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="6a789-147">Establezca instancias de la interfaz en instancias de clase estableciendo la entrada correspondiente en la matriz de vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="6a789-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="6a789-148">Pase la matriz de vinculación dinámica como un parámetro a una llamada a SetShader.</span><span class="sxs-lookup"><span data-stu-id="6a789-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="6a789-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a789-149">Related topics</span></span>

[<span data-ttu-id="6a789-150">Vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="6a789-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)