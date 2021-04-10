---
description: En esta página se muestra cómo generar y usar un efecto.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Usar un efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152687"
---
# <a name="using-an-effect-direct3d-9"></a>Usar un efecto (Direct3D 9)

En esta página se muestra cómo generar y usar un efecto. Los temas tratados incluyen cómo:

-   [Crear un efecto](#create-an-effect)
-   [Representar un efecto](#render-an-effect)
-   [Usar la semántica para buscar parámetros de efectos](#use-semantics-to-find-effect-parameters)
-   [Usar los controladores para obtener y establecer los parámetros de forma eficaz](#use-handles-to-get-and-set-parameters-efficiently)
-   [Agregar información de parámetros con anotaciones](#add-parameter-information-with-annotations)
-   [Parámetros de efectos compartidos](#share-effect-parameters)
-   [Compilar un efecto sin conexión](#compile-an-effect-offline)
-   [Mejorar el rendimiento con los sombreadores](#improve-performance-with-preshaders)
-   [Usar bloques de parámetros para administrar parámetros de efectos](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Crear un efecto

Este es un ejemplo de la creación de un efecto tomado del [ejemplo BasicHLSL](../directx-sdk--august-2009-.md). El código de creación del efecto para crear un sombreador de depuración es desde **OnCreateDevice**:


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



Esta función toma estos argumentos:

-   Dispositivo.
-   Nombre del archivo de efecto.
-   Un puntero a una lista de definiciones terminada en NULL \# que se va a utilizar al analizar el sombreador.
-   Un puntero opcional a un controlador de inclusión escrito por el usuario. El procesador llama al controlador cada vez que necesita resolver un \# include.
-   Una marca de compilación del sombreador que proporciona sugerencias del compilador sobre cómo se utilizará el sombreador. Entre estas opciones se incluyen:
    -   Omitiendo la validación, si se están compilando sombreadores buenos conocidos.
    -   Omitiendo la optimización (a veces se usa cuando las optimizaciones dificultan la depuración).
    -   Solicitar la información de depuración que se va a incluir en el sombreador para que se pueda depurar.
-   Grupo de efectos. Si más de un efecto utiliza el mismo puntero de bloque de memoria, las variables globales de los efectos se comparten entre sí. Si no es necesario compartir las variables de efecto, el bloque de memoria se puede establecer en **null**.
-   Puntero al nuevo efecto.
-   Un puntero a un búfer al que se pueden enviar los errores de validación. En este ejemplo, el parámetro se ha establecido en **null** y no se ha usado.

> [!Note]  
> A partir del SDK de diciembre de 2006, el compilador de HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10. Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.

 

## <a name="render-an-effect"></a>Representar un efecto

La secuencia de llamadas para aplicar el estado de efectos a un dispositivo es:

-   [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) establece la técnica activa.
-   [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) establece el paso activo.
-   [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) actualiza los cambios en cualquier llamada establecida en el paso. Se debe llamar a este método antes de cualquier llamada a Draw.
-   [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) finaliza un paso.
-   [**ID3DXEffect:: end**](id3dxeffect--end.md) finaliza la técnica activa.

El código de representación del efecto también es más sencillo que el código de representación correspondiente sin ningún efecto. Este es el código de representación con un efecto:


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



El bucle de representación consiste en consultar el efecto para ver cuántas pasadas contiene y, a continuación, llamar a todas las pasadas para una técnica. El bucle de representación se puede expandir para llamar a varias técnicas, cada una con varias fases.

## <a name="use-semantics-to-find-effect-parameters"></a>Usar la semántica para buscar parámetros de efectos

Una semántica es un identificador que se adjunta a un parámetro de efecto para permitir que una aplicación busque el parámetro. Un parámetro puede tener como máximo una semántica. La semántica se encuentra después de dos puntos (:) después del nombre del parámetro. Por ejemplo:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Si ha declarado la variable global de efecto sin usar una semántica, tendría un aspecto similar al siguiente:


```
float4x4 matWorldViewProj;
```



La interfaz de efecto puede usar una semántica para obtener un identificador de un parámetro de efecto determinado. Por ejemplo, lo siguiente devuelve el identificador de la matriz:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Además de buscar por nombre semántico, la interfaz de efecto tiene muchos otros métodos para buscar parámetros.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Usar los controladores para obtener y establecer los parámetros de forma eficaz

Los identificadores proporcionan un medio eficaz para hacer referencia a parámetros de efectos, técnicas, pasadas y anotaciones con un efecto. Los identificadores (que son de tipo D3DXHANDLE) son punteros de cadena. Los identificadores que se pasan a funciones como GetParameterxxx o GetAnnotationxxx pueden tener una de las tres formas siguientes:

-   Identificador devuelto por una función como GetParameterxxx.
-   Cadena que contiene el nombre del parámetro, la técnica, la fase o la anotación.
-   Identificador establecido en **null**.

Este ejemplo devuelve un identificador al parámetro que tiene la semántica WORLDVIEWPROJ asociada:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Agregar información de parámetros con anotaciones

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Una anotación es una forma flexible de agregar información a parámetros individuales. La información se puede volver a leer y usar de cualquier manera que la aplicación elija. Una anotación puede ser de cualquier tipo de datos y se puede agregar dinámicamente. Las declaraciones de anotación se delimitan mediante corchetes angulares. Una anotación contiene:

-   Un tipo de datos.
-   Un nombre de variable.
-   Un signo igual (=).
-   Valor de datos.
-   Punto y coma final (;).

Por ejemplo, los dos ejemplos anteriores de este documento contienen esta anotación:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



La anotación se adjunta al objeto Texture y especifica el archivo de textura que se debe usar para inicializar el objeto Texture. La anotación no inicializa el objeto Texture, sino simplemente una parte de la información del usuario que se adjunta a la variable. Una aplicación puede leer la anotación con [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) o [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) para devolver la cadena. La aplicación también puede agregar anotaciones.

Cada anotación:

-   Debe ser un valor numérico o cadenas.
-   Siempre se debe inicializar con un valor predeterminado.
-   Se puede asociar a [técnicas y pases (Direct3D 9)](techniques-and-passes.md) y [parámetros de efecto](/previous-versions/windows/desktop/ee417539(v=vs.85))de nivel superior.
-   Se puede escribir y leer desde con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).
-   Se puede Agregar con [**ID3DXEffect**](id3dxeffect.md).
-   No se puede hacer referencia dentro del efecto.
-   No puede tener subexpresiones o subestados.

## <a name="share-effect-parameters"></a>Parámetros de efectos compartidos

Los parámetros de efecto son todas las variables no estáticas declaradas en un efecto. Esto puede incluir variables globales y anotaciones. Los parámetros de efecto se pueden compartir entre distintos efectos declarando parámetros con la palabra clave "Shared" y creando después el efecto con un grupo de efectos.

Un grupo de efectos contiene parámetros de efectos compartidos. El grupo se crea llamando a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), que devuelve una interfaz [**ID3DXEffectPool**](id3dxeffectpool.md) . La interfaz se puede proporcionar como entrada a cualquiera de las funciones de D3DXCreateEffectxxx cuando se crea un efecto. Para que un parámetro se comparta entre varios efectos, el parámetro debe tener el mismo nombre, tipo y semántica en cada uno de los efectos compartidos.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Los efectos que comparten parámetros deben usar el mismo dispositivo. Esto se aplica para impedir el uso compartido de parámetros dependientes del dispositivo (como sombreadores o texturas) en distintos dispositivos. Los parámetros se eliminan del grupo cada vez que se liberan los efectos que contienen los parámetros compartidos. Si los parámetros de uso compartido no son necesarios, proporcione **null** para el grupo de efectos cuando se cree un efecto.

Los efectos clonados usan el mismo grupo de efectos que el efecto desde el que se clonan. La clonación de un efecto realiza una copia exacta de un efecto, incluidas las variables globales, las técnicas, las pasadas y las anotaciones.

## <a name="compile-an-effect-offline"></a>Compilar un efecto sin conexión

Puede compilar un efecto en tiempo de ejecución con [**D3DXCreateEffect**](d3dxcreateeffect.md)o puede compilar un efecto sin conexión mediante la herramienta de compilador de línea de comandos fxc.exe. El efecto en el [ejemplo CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contiene un sombreador de vértices, un sombreador de píxeles y una técnica:


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



El uso de la [herramienta de compilador de efectos](../direct3dtools/fxc.md) para compilar el sombreador de vs \_ 1 \_ 1 generó las siguientes instrucciones del sombreador de ensamblado:


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a>Mejorar el rendimiento con los sombreadores

Un presombreador es una técnica para aumentar la eficacia del sombreador mediante el cálculo previo de expresiones de sombreador constantes. El compilador de efectos extrae automáticamente los cálculos del sombreador del cuerpo de un sombreador y los ejecuta en la CPU antes de que se ejecute el sombreador. Por consiguiente, los presombreadores solo funcionan con efectos. Por ejemplo, estas dos expresiones se pueden evaluar fuera del sombreador antes de ejecutarse.


```
mul(World,mul(View, Projection));
sin(time)
```



Los cálculos del sombreador que se pueden desplace son los asociados a los parámetros uniformes; es decir, los cálculos no cambian para cada vértice o píxel. Si usa efectos, el compilador de efectos genera y ejecuta automáticamente un sombreador. no hay marcas para habilitar. Los presombreadores pueden reducir el número de instrucciones por sombreador y también pueden reducir el número de registros constantes que utiliza un sombreador.

Piense en el compilador de efectos como una especie de compilador de varios procesadores porque compila código de sombreador para dos tipos de procesadores: una CPU y una GPU. Además, el compilador de efectos está diseñado para trasladar el código de la GPU a la CPU y, por tanto, mejorar el rendimiento del sombreador. Esto es muy similar a la extracción de una expresión estática fuera de un bucle. Sombreador que transforma la posición del espacio universal en el espacio de proyección y copia las coordenadas de textura con el siguiente aspecto en HLSL:


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



El uso de la [herramienta de compilador de efectos](../direct3dtools/fxc.md) para compilar el sombreador de vs \_ 1 \_ 1 genera las siguientes instrucciones de ensamblado:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Esto usa 14 ranuras aproximadamente y consume 9 registros constantes. Con un presombreador, el compilador mueve las expresiones estáticas fuera del sombreador y al sombreador. El mismo sombreador tendría un aspecto similar al siguiente con un sombreador:


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



Un efecto ejecuta un sombreador inmediatamente antes de ejecutar un sombreador. El resultado es la misma funcionalidad con mayor rendimiento del sombreador, ya que se ha reducido el número de instrucciones que es necesario ejecutar (para cada vértice o píxel según el tipo de sombreador). Además, el sombreador consume menos registros constantes como resultado de las expresiones estáticas que se mueven al presombreador. Esto significa que los sombreadores previamente limitados por el número de registros constantes que requieren ahora pueden compilarse porque requieren menos registros constantes. Es razonable esperar una mejora del rendimiento del 5 por ciento y del 20 por ciento de los sombreadores.

Tenga en cuenta que las constantes de entrada son diferentes de las constantes de salida en un sombreador. El resultado C1 no es el mismo que el registro C1 de entrada. La escritura en un registro constante en un sombreador escribe realmente en la ranura de entrada (constante) del sombreador correspondiente.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



La instrucción de CMP anterior leerá el valor C1 del presombreador, mientras que la instrucción mul escribirá en los registros del sombreador de hardware para que los use el sombreador de vértices.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Usar bloques de parámetros para administrar parámetros de efectos

Los bloques de parámetros son bloques de cambios de estado de efecto. Un bloque de parámetros puede registrar cambios de estado, de modo que se puedan aplicar más adelante con una sola llamada. Cree un bloque de parámetros mediante una llamada a [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



El bloque de parámetros guarda cuatro cambios aplicados por las llamadas a la API. La llamada a [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) inicia la grabación de los cambios de estado. [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) deja de agregar los cambios al bloque de parámetros y devuelve un identificador. El identificador se usará al llamar a [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).

En el [ejemplo EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), el bloque de parámetros se aplica en la secuencia de representación:


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



El bloque de parámetros establece el valor de los cuatro cambios de Estado justo antes de que se llame a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) . Los bloques de parámetros son una forma cómoda de establecer varios cambios de estado con una única llamada API.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](effects.md)
</dt> </dl>

 

 
