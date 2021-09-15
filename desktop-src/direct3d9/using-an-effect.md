---
description: En esta página se muestra cómo generar y usar un efecto.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Usar un efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473241"
---
# <a name="using-an-effect-direct3d-9"></a>Usar un efecto (Direct3D 9)

En esta página se muestra cómo generar y usar un efecto. Los temas tratados incluyen cómo:

-   [Crear un efecto](#create-an-effect)
-   [Representar un efecto](#render-an-effect)
-   [Usar semántica para buscar parámetros de efecto](#use-semantics-to-find-effect-parameters)
-   [Uso de identificadores para obtener y establecer parámetros de forma eficaz](#use-handles-to-get-and-set-parameters-efficiently)
-   [Agregar información de parámetros con anotaciones](#add-parameter-information-with-annotations)
-   [Parámetros de efecto de recurso compartido](#share-effect-parameters)
-   [Compilar un efecto sin conexión](#compile-an-effect-offline)
-   [Mejora del rendimiento con preshaders](#improve-performance-with-preshaders)
-   [Usar bloques de parámetros para administrar parámetros de efecto](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a>Crear un efecto

Este es un ejemplo de creación de un efecto tomado del [ejemplo basicHLSL](../directx-sdk--august-2009-.md). El código de creación del efecto para crear un sombreador de depuración es **de OnCreateDevice**:


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
-   Nombre de archivo del archivo de efecto.
-   Puntero a una lista de define terminada en NULL \# que se usará al analizar el sombreador.
-   Puntero opcional a un controlador de incluir escrito por el usuario. El procesador llama al controlador siempre que necesite resolver un \# include.
-   Marca de compilación de sombreador que proporciona sugerencias del compilador sobre cómo se usará el sombreador. Entre estas opciones se incluyen:
    -   Omitir la validación, si se compilan sombreadores buenos conocidos.
    -   Omitir la optimización (a veces se usa cuando las optimizaciones dificultan la depuración).
    -   Solicitud de información de depuración que se va a incluir en el sombreador para que se pueda depurar.
-   Grupo de efectos. Si más de un efecto usa el mismo puntero de grupo de memoria, las variables globales de los efectos se comparten entre sí. Si no es necesario compartir variables de efecto, el grupo de memoria se puede establecer en **NULL.**
-   Puntero al nuevo efecto.
-   Puntero a un búfer al que se pueden enviar errores de validación. En este ejemplo, el parámetro se estableció en **NULL** y no se usó.

> [!Note]  
> A partir del SDK de diciembre de 2006, el compilador HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10. Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.

 

## <a name="render-an-effect"></a>Representar un efecto

La secuencia de llamadas para aplicar el estado de efecto a un dispositivo es:

-   [**ID3DXEffect::Begin**](id3dxeffect--begin.md) establece la técnica activa.
-   [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) establece el paso activo.
-   [**ID3DXEffect::CommitChanges actualiza**](id3dxeffect--commitchanges.md) los cambios en las llamadas de conjunto en el paso. Se debe llamar a este método antes de cualquier llamada a draw.
-   [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) finaliza un paso.
-   [**ID3DXEffect::End finaliza**](id3dxeffect--end.md) la técnica activa.

El código de representación de efecto también es más sencillo que el código de representación correspondiente sin ningún efecto. Este es el código de representación con un efecto:


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



El bucle de representación consiste en consultar el efecto para ver cuántos pases contiene y, a continuación, llamar a todos los pases para una técnica. El bucle de representación se podría expandir para llamar a varias técnicas, cada una con varios pases.

## <a name="use-semantics-to-find-effect-parameters"></a>Usar semántica para buscar parámetros de efecto

Una semántica es un identificador asociado a un parámetro de efecto para permitir que una aplicación busque el parámetro. Un parámetro puede tener como máximo una semántica. La semántica se encuentra después de dos puntos (:) después del nombre del parámetro. Por ejemplo:


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



Si declaró la variable global de efecto sin usar una semántica, tendría este aspecto en su lugar:


```
float4x4 matWorldViewProj;
```



La interfaz de efecto puede usar una semántica para obtener un identificador para un parámetro de efecto determinado. Por ejemplo, lo siguiente devuelve el identificador de la matriz:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



Además de buscar por nombre semántico, la interfaz de efecto tiene muchos otros métodos para buscar parámetros.

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a>Uso de identificadores para obtener y establecer parámetros de forma eficaz

Los identificadores proporcionan un medio eficaz para hacer referencia a parámetros de efecto, técnicas, pases y anotaciones con un efecto. Los identificadores (que son de tipo D3DXHANDLE) son punteros de cadena. Los identificadores que se pasan a funciones como GetParameterxxx o GetAnnotationxxx pueden tener una de estas tres formas:

-   Identificador devuelto por una función como GetParameterxxx.
-   Cadena que contiene el nombre del parámetro, la técnica, el paso o la anotación.
-   Identificador establecido en **NULL.**

En este ejemplo se devuelve un identificador al parámetro que tiene asociada la semántica WORLDVIEWPROJ:


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a>Agregar información de parámetros con anotaciones

Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro. Una anotación es una manera flexible de agregar información a parámetros individuales. La información se puede volver a leer y usar de la manera que elija la aplicación. Una anotación puede ser de cualquier tipo de datos y se puede agregar dinámicamente. Las declaraciones de anotación están delimitadas por corchetes angulares. Una anotación contiene:

-   Tipo de datos.
-   Nombre de variable.
-   Signo igual (=).
-   Valor de datos.
-   Punto y coma final (;).

Por ejemplo, los dos ejemplos anteriores de este documento contienen esta anotación:


```
texture Tex0 < string name = "tiger.bmp"; >;
```



La anotación se adjunta al objeto de textura y especifica el archivo de textura que se debe usar para inicializar el objeto de textura. La anotación no inicializa el objeto de textura, simplemente es un fragmento de información del usuario que está asociado a la variable. Una aplicación puede leer la anotación con [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) o [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) para devolver la cadena. La aplicación también puede agregar anotaciones.

Cada anotación:

-   Debe ser numérico o cadenas.
-   Siempre se debe inicializar con un valor predeterminado.
-   Se puede asociar con [técnicas y pases (Direct3D 9)](techniques-and-passes.md) y parámetros de [efecto de nivel superior.](/previous-versions/windows/desktop/ee417539(v=vs.85))
-   Se puede escribir y leer con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler.**](id3dxeffectcompiler.md)
-   Se puede agregar con [**ID3DXEffect.**](id3dxeffect.md)
-   No se puede hacer referencia a dentro del efecto.
-   No puede tener submánticos ni subta anotaciones.

## <a name="share-effect-parameters"></a>Parámetros de efecto de recurso compartido

Los parámetros de efecto son todas las variables no estáticas declaradas en un efecto. Esto puede incluir variables globales y anotaciones. Los parámetros de efecto se pueden compartir entre distintos efectos declarando parámetros con la palabra clave "shared" y, a continuación, creando el efecto con un grupo de efectos.

Un grupo de efectos contiene parámetros de efecto compartido. El grupo se crea mediante una llamada a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), que devuelve una [**interfaz ID3DXEffectPool.**](id3dxeffectpool.md) La interfaz se puede proporcionar como entrada a cualquiera de las funciones D3DXCreateEffectxxx cuando se crea un efecto. Para que un parámetro se comparta entre varios efectos, el parámetro debe tener el mismo nombre, tipo y semántica en cada uno de los efectos compartidos.


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



Los efectos que comparten parámetros deben usar el mismo dispositivo. Esto se aplica para evitar el uso compartido de parámetros dependientes del dispositivo (como sombreadores o texturas) entre distintos dispositivos. Los parámetros se eliminan del grupo cada vez que se liberan los efectos que contienen los parámetros compartidos. Si no es necesario compartir parámetros, proporcione **NULL para** el grupo de efectos cuando se cree un efecto.

Los efectos clonados usan el mismo grupo de efectos que el efecto desde el que se clonan. La clonación de un efecto realiza una copia exacta de un efecto, incluidas variables globales, técnicas, pases y anotaciones.

## <a name="compile-an-effect-offline"></a>Compilar un efecto sin conexión

Puede compilar un efecto en tiempo de ejecución con [**D3DXCreateEffect**](d3dxcreateeffect.md)o puede compilar un efecto sin conexión mediante la herramienta de compilador de línea de comandos fxc.exe. El efecto del ejemplo [CompiledEffect contiene](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) un sombreador de vértices, un sombreador de píxeles y una técnica:


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



El [uso de la herramienta Effect-Compiler para](../direct3dtools/fxc.md) compilar el sombreador para vs \_ \_ 1 1 generó las siguientes instrucciones de sombreador de ensamblado:


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



## <a name="improve-performance-with-preshaders"></a>Mejora del rendimiento con preshaders

Un preshader es una técnica para aumentar la eficacia del sombreador mediante el cálculo previo de expresiones de sombreador constante. El compilador de efectos extrae automáticamente los cálculos del sombreador del cuerpo de un sombreador y los ejecuta en la CPU antes de que se ejecute el sombreador. Por lo tanto, los preshaders solo funcionan con efectos. Por ejemplo, estas dos expresiones se pueden evaluar fuera del sombreador antes de que se ejecute.


```
mul(World,mul(View, Projection));
sin(time)
```



Los cálculos de sombreador que se pueden mover son los asociados a parámetros uniformes; Es decir, los cálculos no cambian para cada vértice o píxel. Si usa efectos, el compilador de efectos genera y ejecuta automáticamente un preconfigurador. no hay marcas que habilitar. Los sombreadores previos pueden reducir el número de instrucciones por sombreador y también pueden reducir el número de registros constantes que consume un sombreador.

Piense en el compilador de efectos como una clase de compilador de varios procesadores porque compila el código del sombreador para dos tipos de procesadores: una CPU y una GPU. Además, el compilador de efectos está diseñado para mover código de la GPU a la CPU y, por tanto, mejorar el rendimiento del sombreador. Esto es muy similar a extraer una expresión estática de un bucle. Un sombreador que transforma la posición del espacio mundial al espacio de proyección y copia las coordenadas de textura tendría este aspecto en HLSL:


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



El [uso de la herramienta Effect-Compiler para](../direct3dtools/fxc.md) compilar el sombreador para vs \_ \_ 1 1 genera las siguientes instrucciones de ensamblado:


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



Esto usa aproximadamente 14 ranuras y consume 9 registros constantes. Con un preshader, el compilador mueve las expresiones estáticas fuera del sombreador y al preshader. El mismo sombreador tendría este aspecto con un preshader:


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



Un efecto ejecuta un preshader justo antes de ejecutar un sombreador. El resultado es la misma funcionalidad con un mayor rendimiento del sombreador porque se ha reducido el número de instrucciones que deben ejecutarse (para cada vértice o píxel según el tipo de sombreador). Además, el sombreador consume menos registros constantes como resultado de que las expresiones estáticas se mueven al objeto anterior. Esto significa que los sombreadores anteriormente limitados por el número de registros constantes que requerían ahora se pueden compilar porque requieren menos registros constantes. Es razonable esperar un 5 % y una mejora del rendimiento del 20 % de los preshaders.

Tenga en cuenta que las constantes de entrada son diferentes de las constantes de salida de un preconfigurador. La salida c1 no es la misma que el registro c1 de entrada. La escritura en un registro constante en un preconfigurador escribe realmente en la ranura de entrada (constante) del sombreador correspondiente.


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



La instrucción cmp anterior leerá el valor c1 del preshader, mientras que la instrucción mul escribirá en los registros del sombreador de hardware que usará el sombreador de vértices.

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a>Usar bloques de parámetros para administrar parámetros de efecto

Los bloques de parámetros son bloques de cambios de estado de efecto. Un bloque de parámetros puede registrar los cambios de estado, de modo que se puedan aplicar más adelante con una sola llamada. Cree un bloque de parámetros mediante una [**llamada a ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):


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



El bloque de parámetros guarda cuatro cambios aplicados por las llamadas API. La [**llamada a ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) comienza a registrar los cambios de estado. [**ID3DXEffect::EndParameterBlock deja**](id3dxeffect--endparameterblock.md) de agregar los cambios al bloque de parámetros y devuelve un identificador. El identificador se usará al llamar a [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).

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



El bloque de parámetros establece el valor de los cuatro cambios de estado justo antes de [**llamar a ID3DXEffect::Begin.**](id3dxeffect--begin.md) Los bloques de parámetros son una manera práctica de establecer varios cambios de estado con una sola llamada API.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](effects.md)
</dt> </dl>

 

 
