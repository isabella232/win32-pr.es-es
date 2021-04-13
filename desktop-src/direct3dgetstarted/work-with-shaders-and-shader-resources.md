---
title: Trabajar con sombreadores y recursos del sombreador
description: Es el momento de aprender a trabajar con sombreadores y recursos del sombreador en el desarrollo de un juego de Microsoft DirectX para Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420912"
---
# <a name="work-with-shaders-and-shader-resources"></a>Trabajar con sombreadores y recursos del sombreador

Es el momento de aprender a trabajar con sombreadores y recursos del sombreador en el desarrollo de un juego de Microsoft DirectX para Windows 8. Hemos visto cómo configurar el dispositivo de gráficos y los recursos, y es posible que incluso haya empezado a modificar su canalización. Ahora vamos a echar un vistazo a los sombreadores de píxeles y vértices.

Si no está familiarizado con los idiomas del sombreador, una explicación rápida está en orden. Los sombreadores son programas pequeños y de bajo nivel que se compilan y ejecutan en fases específicas de la canalización de gráficos. Su especialidad es una operación matemática de punto flotante muy rápida. Los programas de sombreador más comunes son:

-   **Sombreador de vértices**: se ejecuta para cada vértice de una escena. Este sombreador opera en los elementos de búfer de vértices proporcionados por la aplicación que realiza la llamada y, como mínimo, da como resultado un vector de posición de cuatro componentes que se rasterizará en una posición en píxeles.
-   **Sombreador de píxeles**: se ejecuta para cada píxel de un destino de representación. Este sombreador recibe coordenadas rasterizadas de las fases del sombreador anterior (en las canalizaciones más simples, esto sería el sombreador de vértices) y devuelve un color (u otro valor de 4 componentes) para esa posición en píxeles, que se escribe en un destino de representación.

En este ejemplo se incluyen sombreadores de vértices y píxeles muy básicos que solo dibujan geometría y sombreadores más complejos que agregan cálculos de iluminación básicos.

Los programas del sombreador están escritos en el lenguaje HLSL (Microsoft High Level Shader Language). La sintaxis de HLSL tiene un aspecto muy similar a C, pero sin los punteros. Los programas del sombreador deben ser muy compactos y eficaces. Si el sombreador se compila con demasiadas instrucciones, no se puede ejecutar y se devuelve un error. (Tenga en cuenta que el número exacto de instrucciones permitidas forma parte del [nivel de características de Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)).

En Direct3D, los sombreadores no se compilan en tiempo de ejecución; se compilan cuando se compila el resto del programa. Al compilar la aplicación con Microsoft Visual Studio 2013, los archivos HLSL se compilan en archivos CSO (. CSO) que la aplicación debe cargar y colocar en la memoria de GPU antes del dibujo. Asegúrese de incluir estos archivos CSO en la aplicación al empaquetarla. se trata de recursos como mallas y texturas.

## <a name="understand-hlsl-semantics"></a>Descripción de la semántica de HLSL

Es importante dedicar un momento a analizar la semántica de HLSL antes de continuar, ya que a menudo son un punto de confusión para los nuevos desarrolladores de Direct3D. La semántica de HLSL son cadenas que identifican un valor pasado entre la aplicación y un programa de sombreador. Aunque pueden ser cualquiera de las diversas cadenas posibles, el procedimiento recomendado es usar una cadena como `POSITION` o `COLOR` que indique el uso. Esta semántica se asigna cuando se crea un búfer de constantes o un diseño de entrada. Puedes anexar un número entre 0 y 7 a la semántica para usar registros distintos para valores similares. Por ejemplo: COLOR0, COLOR1, COLOR2...

La semántica que tiene el prefijo "SV \_ " es la semántica *del valor del sistema* que escribe el programa del sombreador; el propio juego (que se ejecuta en la CPU) no puede modificarla. Normalmente, esta semántica contiene valores que son entradas o salidas de otra fase del sombreador en la canalización de gráficos, o que la GPU genera completamente.

Además, `SV_` la semántica tiene comportamientos diferentes cuando se usan para especificar la entrada o la salida de una fase del sombreador. Por ejemplo, `SV_POSITION` (salida) contiene los datos de vértice transformados durante la fase del sombreador de vértices y `SV_POSITION` (*entrada*) contiene los valores de posición en píxeles interpolados por la GPU durante la fase de rasterización.

A continuación se muestran algunas semánticas de HLSL comunes:

-   `POSITION`(*n*) para los datos de búfer de vértices. `SV_POSITION` proporciona una posición en píxeles para el sombreador de píxeles y no se puede escribir en el juego.
-   `NORMAL`(*n*) para los datos normales proporcionados por el búfer de vértices.
-   `TEXCOORD`(*n*) para los datos de coordenadas UV de textura que se proporcionan a un sombreador.
-   `COLOR`(n) para los datos de color RGBA proporcionados a un sombreador. Tenga en cuenta que se trata de forma idéntica para coordinar los datos, incluida la interpolación del valor durante la rasterización; la semántica simplemente le ayuda a identificar que se trata de datos de color.
-   `SV_Target`\[n \] para escribir de un sombreador de píxeles en una textura de destino u otro búfer de píxeles.

Veremos algunos ejemplos de la semántica de HLSL mientras revisamos el ejemplo.

## <a name="read-from-the-constant-buffers"></a>Leer de los búferes de constantes

Cualquier sombreador puede leer desde un búfer de constantes si ese búfer se adjunta a su fase como un recurso. En este ejemplo, solo se asigna un búfer de constantes al sombreador de vértices.

El búfer de constantes se declara en dos lugares: en el código de C++ y en los archivos HLSL correspondientes que tendrán acceso a él.

Aquí se muestra cómo se declara el struct de búfer de constantes en el código de C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Al declarar la estructura para el búfer de constantes en el código de C++, asegúrese de que todos los datos se alineen correctamente a lo largo de los límites de 16 bytes. La forma más fácil de hacerlo es usar tipos de [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , como **XMFLOAT4** o **XMFLOAT4X4**, tal como se ha detectado en el código de ejemplo. También puede protegerse frente a búferes desalineados mediante la declaración de una aserción estática:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Esta línea de código producirá un error en tiempo de compilación si **ConstantBufferStruct** no tiene una alineación de 16 bytes. Para obtener más información sobre la alineación y el empaquetado de búferes constantes, consulte [reglas de empaquetado para variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

Ahora, aquí se muestra cómo se declara el búfer de constantes en el HLSL del sombreador de vértices.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Todos los búferes (constantes, texturas, muestreador u otros) deben tener un registro definido para que la GPU pueda acceder a ellos. Cada fase del sombreador permite hasta 15 búferes de constantes y cada búfer puede contener hasta 4.096 variables constantes. La sintaxis de la declaración de uso de registro es la siguiente:

-   **b * * *\#* : un registro para un búfer de constantes (** CBuffer * *).
-   **t * * *\#* : un registro para un búfer de textura (** tbuffer * *).
-   **s * \#** *: registro de una muestra. (Una muestra define el comportamiento de búsqueda de textura en el recurso de textura).

Por ejemplo, el HLSL de un sombreador de píxeles podría tomar una textura y una muestra como entrada con una declaración como esta.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

Depende de usted asignar búferes de constantes a los registros; al configurar la canalización, debe adjuntar un búfer de constantes a la misma ranura a la que se asignó en el archivo HLSL. Por ejemplo, en el tema anterior, la llamada a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica "0" para el primer parámetro. Esto indica a Direct3D que debe adjuntar el recurso de búfer de constante al registro 0, que coincide con la asignación del búfer para **registrar (b0)** en el archivo HLSL.

## <a name="read-from-the-vertex-buffers"></a>Leer de los búferes de vértices

El búfer de vértices proporciona los datos de triángulo para los objetos de escena a los sombreadores de vértices. Al igual que con el búfer de constantes, el struct de búfer de vértices se declara en el código de C++, mediante reglas de empaquetado similares.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



No hay ningún formato estándar para los datos de vértices en Direct3D 11. En su lugar, se define nuestro propio diseño de datos de vértices con un descriptor. los campos de datos se definen mediante una matriz de estructuras [**\_ DESC del \_ elemento \_ de entrada D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) . Aquí se muestra un diseño de entrada simple que describe el mismo formato de vértice que el struct anterior:


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



Si agrega datos al formato de vértice al modificar el código de ejemplo, asegúrese de actualizar también el diseño de entrada o el sombreador no podrá interpretarlo. Puede modificar el diseño de vértices de la siguiente manera:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



En ese caso, debe modificar la definición de diseño de entrada como se indica a continuación.


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



Cada una de las definiciones de elementos de diseño de entrada tiene como prefijo una cadena, como "POSITION" o "NORMAL", que es la semántica que se explicó anteriormente en este tema. Es como un identificador que ayuda a la GPU a identificar ese elemento al procesar el vértice. Elija nombres comunes y significativos para los elementos de vértice.

Al igual que con el búfer de constantes, el sombreador de vértices tiene una definición de búfer correspondiente para los elementos de vértices entrantes. (Este es el motivo por el que se proporciona una referencia al recurso de sombreador de vértices al crear el diseño de entrada: Direct3D valida el diseño de datos por vértice con la estructura de entrada del sombreador). Observe cómo la semántica coincide entre la definición de diseño de entrada y esta declaración de búfer de HLSL. Sin embargo, `COLOR` tiene un "0" anexado. No es necesario agregar 0 si solo tiene un `COLOR` elemento declarado en el diseño, pero es aconsejable anexarlo en caso de que decida agregar más elementos de color en el futuro.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Pasar datos entre sombreadores

Los sombreadores toman tipos de entrada y devuelven los tipos de salida de sus funciones principales tras su ejecución. Para el sombreador de vértices definido en la sección anterior, el tipo de entrada era la estructura de entrada de VS \_ y hemos definido un diseño de entrada y una estructura de C++ coincidentes. Una matriz de este struct se usa para crear un búfer de vértices en el método **CreateCube** .

El sombreador de vértices devuelve una estructura de entrada de PS \_ , que debe contener mínimamente la posición del vértice final de 4 componentes (FLOAT4). Este valor de posición debe tener la semántica del valor del sistema, `SV_POSITION` , que se declara para que la GPU tenga los datos que necesita para realizar el siguiente paso del dibujo. Observe que no hay una correspondencia 1:1 entre la salida del sombreador de vértices y la entrada del sombreador de píxeles; el sombreador de vértices devuelve una estructura para cada vértice, pero el sombreador de píxeles se ejecuta una vez para cada píxel. Esto se debe a que los datos por vértice primero pasan a través de la fase de rasterización. En esta fase se decide qué píxeles "cubren" la geometría que se está dibujando, se calculan los datos interpolados por vértice para cada píxel y, a continuación, se llama al sombreador de píxeles una vez para cada uno de esos píxeles. La interpolación es el comportamiento predeterminado cuando se rasterizan los valores de salida y es esencial en concreto para el procesamiento correcto de los datos de vectores de salida (vectores ligeros, normalización por vértice y tangentes y otros).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Revisar el sombreador de vértices

El sombreador de vértices de ejemplo es muy sencillo: tomar un vértice (posición y color), transformar la posición de las coordenadas del modelo en coordenadas proyectadas de perspectiva y devolverla (junto con el color) al rasterizador. Observe que el valor de color se interpola a la derecha junto con los datos de la posición, lo que proporciona un valor diferente para cada píxel aunque el sombreador de vértices no haya realizado ningún cálculo en el valor de color.


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



Un sombreador de vértices más complejo, como uno que configura los vértices de un objeto para el sombreado de Phong, podría ser más parecido a esto. En este caso, estamos aprovechando el hecho de que los vectores y las normales se interpolan para aproximarse a una superficie de aspecto suave.

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a>Revisar el sombreador de píxeles

Este sombreador de píxeles en este ejemplo es probablemente la cantidad mínima absoluta de código que puede tener en un sombreador de píxeles. Toma los datos de color de los píxeles interpolados generados durante la rasterización y los devuelve como salida, donde se escribirá en un destino de representación. ¿Cómo aburri!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



La parte importante es la `SV_TARGET` semántica del valor del sistema en el valor devuelto. Indica que la salida se va a escribir en el destino de representación principal, que es el búfer de textura proporcionado a la cadena de intercambio para su presentación. Esto es necesario para los sombreadores de píxeles: sin los datos de color del sombreador de píxeles, Direct3D no tendría nada que mostrar.

Un ejemplo de un sombreador de píxeles más complejo para realizar el sombreado de Phong podría ser similar al siguiente. Dado que los vectores y las normales se interpolaron, no tenemos que calcularlos por píxel. Sin embargo, es necesario volver a normalizarlas debido a cómo funciona la interpolación; conceptualmente, es necesario "girar" gradualmente el vector de la dirección en el vértice a hasta la dirección del vértice B, manteniendo su longitud: la interpolación wheras se corta en lugar de una línea recta entre los dos extremos de vector.

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

En otro ejemplo, el sombreador de píxeles toma sus propios búferes de constantes que contienen información de luz y material. El diseño de entrada en el sombreador de vértices se expandirá para incluir datos normales y se espera que la salida de ese sombreador de vértices incluya vectores transformados para el vértice, la luz y el vértice normal en el sistema de coordenadas de la vista.

Si tiene búferes de textura y muestreadores con registros asignados (**t** y **s**, respectivamente), puede tener acceso a ellos también en el sombreador de píxeles.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

Los sombreadores son herramientas muy eficaces que se pueden usar para generar recursos de procedimientos como mapas de sombras o texturas de ruido. De hecho, las técnicas avanzadas requieren que se creen texturas más abstractas, no como elementos visuales, sino como búferes. Contienen datos como la información de alto u otros datos que se pueden muestrear en el paso final del sombreador de píxeles o en ese fotograma determinado como parte de un paso de efectos de varias fases. El muestreo múltiple es una herramienta eficaz y la red troncal de muchos efectos visuales modernos.

## <a name="next-steps"></a>Pasos siguientes

Espero que esté familiarizado con DirectX 11at este punto y esté listo para empezar a trabajar en el proyecto. Estos son algunos vínculos que le ayudarán a responder a otras preguntas que puede tener sobre el desarrollo con DirectX y C++:

-   [Desarrollar juegos](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Usar Visual Studio Tools para la programación de juegos de DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Tutoriales de ejemplo y desarrollo de juegos de DirectX](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Recursos adicionales de programación de juegos](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con recursos de dispositivos DirectX](work-with-dxgi.md)
</dt> <dt>

[Descripción de la canalización de representación de Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 