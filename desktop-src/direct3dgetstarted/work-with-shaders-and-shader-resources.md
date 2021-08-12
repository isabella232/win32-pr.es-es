---
title: Trabajar con sombreadores y recursos de sombreador
description: Es el momento de aprender a trabajar con sombreadores y recursos de sombreador para desarrollar el juego de Microsoft DirectX para Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0152ba74dcc8dd1c602b69d854634502c928a0deefe5521bcab8999954049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288555"
---
# <a name="work-with-shaders-and-shader-resources"></a>Trabajar con sombreadores y recursos de sombreador

Es el momento de aprender a trabajar con sombreadores y recursos de sombreador para desarrollar el juego de Microsoft DirectX para Windows 8. Hemos visto cómo configurar el dispositivo gráfico y los recursos, e incluso hemos empezado a modificar su canalización. Ahora echemos un vistazo a los sombreadores de píxeles y vértices.

Si no está familiarizado con los lenguajes de sombreador, hay una explicación rápida en orden. Los sombreadores son programas pequeños de bajo nivel que se compilan y ejecutan en fases específicas de la canalización de gráficos. Su especialización son operaciones matemáticas de punto flotante muy rápidas. Los programas de sombreador más comunes son:

-   **Sombreador de** vértices: se ejecuta para cada vértice de una escena. Este sombreador funciona en los elementos de búfer de vértices proporcionados por la aplicación que realiza la llamada y, como mínimo, da como resultado un vector de posición de 4 componentes que se rasterizará en una posición de píxel.
-   **Sombreador de** píxeles: se ejecuta para cada píxel de un destino de representación. Este sombreador recibe coordenadas rasterizadas de fases anteriores del sombreador (en las canalizaciones más sencillas, este sería el sombreador de vértices) y devuelve un color (u otro valor de 4 componentes) para esa posición de píxel, que luego se escribe en un destino de representación.

En este ejemplo se incluyen sombreadores de vértices y píxeles muy básicos que solo dibujan geometría, y sombreadores más complejos que agregan cálculos de iluminación básicos.

Los programas de sombreador se escriben en lenguaje de sombreador de alto nivel (HLSL) de Microsoft. La sintaxis HLSL se parece mucho a C, pero sin punteros. Los programas de sombreador deben ser muy compactos y eficaces. Si el sombreador se compila en demasiadas instrucciones, no se puede ejecutar y se devuelve un error. (Tenga en cuenta que el número exacto de instrucciones permitidas forma parte del nivel [de característica de Direct3D).](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)

En Direct3D, los sombreadores no se compilan en tiempo de ejecución; se compilan cuando se compila el resto del programa. Al compilar la aplicación con Microsoft Visual Studio 2013, los archivos HLSL se compilan en archivos CSO (.cso) que la aplicación debe cargar y colocar en la memoria de GPU antes de dibujar. Asegúrese de incluir estos archivos CSO con la aplicación al empaquetar; son recursos como mallas y texturas.

## <a name="understand-hlsl-semantics"></a>Comprender la semántica hlsl

Es importante tardar un momento en analizar la semántica hlsl antes de continuar, ya que a menudo son un punto de confusión para los nuevos desarrolladores de Direct3D. La semántica hlsl son cadenas que identifican un valor pasado entre la aplicación y un programa de sombreador. Aunque pueden ser cualquiera de las cadenas posibles, el procedimiento recomendado es usar una cadena como o que `POSITION` `COLOR` indique el uso. Esta semántica se asigna al construir un búfer constante o un diseño de entrada. Puedes anexar un número entre 0 y 7 a la semántica para usar registros distintos para valores similares. Por ejemplo: COLOR0, COLOR1, COLOR2...

La semántica que tiene como prefijo "SV" son semánticas de valores del sistema escritas en el programa de sombreador; el propio juego (que se ejecuta en la CPU) no puede \_ modificarlos.  Normalmente, esta semántica contiene valores que son entradas o salidas de otra fase del sombreador en la canalización de gráficos o que la GPU genera completamente.

Además, la semántica tiene comportamientos diferentes cuando se usan para especificar la entrada o `SV_` la salida de una fase del sombreador. Por ejemplo, (salida) contiene los datos de vértice transformados durante la fase del sombreador de vértices y (entrada ) contiene los valores de posición de píxeles interpolados por la GPU durante la fase de `SV_POSITION` `SV_POSITION` rasterización.

Estas son algunas semánticas de HLSL comunes:

-   `POSITION`(*n*) para los datos del búfer de vértices. `SV_POSITION` proporciona una posición de píxel al sombreador de píxeles y el juego no puede escribirlo.
-   `NORMAL`(*n*) para los datos normales proporcionados por el búfer de vértices.
-   `TEXCOORD`(*n*) para los datos de coordenadas UV de textura proporcionados a un sombreador.
-   `COLOR`(n) para los datos de color RGBA proporcionados a un sombreador. Tenga en cuenta que se trata de forma idéntica para coordinar los datos, incluida la interpolación del valor durante la rasterización; la semántica simplemente le ayuda a identificar que son datos de color.
-   `SV_Target`\[n \] para escribir desde un sombreador de píxeles a una textura de destino u otro búfer de píxeles.

Veremos algunos ejemplos de semántica hlsl a medida que se revisa el ejemplo.

## <a name="read-from-the-constant-buffers"></a>Lectura de los búferes constantes

Cualquier sombreador puede leer desde un búfer constante si ese búfer está asociado a su fase como un recurso. En este ejemplo, solo se asigna un búfer constante al sombreador de vértices.

El búfer constante se declara en dos lugares: en el código de C++ y en los archivos HLSL correspondientes que tendrán acceso a él.

Aquí se muestra cómo se declara la estructura de búfer constante en el código de C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Al declarar la estructura del búfer constante en el código de C++, asegúrese de que todos los datos están alineados correctamente a lo largo de los límites de 16 bytes. La manera más fácil de hacerlo es usar tipos [DirectXMath,](/windows/desktop/dxmath/directxmath-portal) como **XMFLOAT4** o **XMFLOAT4X4,** como se muestra en el código de ejemplo. También puede protegerse contra búferes mal alineados declarando una aserción estática:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Esta línea de código producirá un error en tiempo de compilación si **ConstantBufferStruct** no está alineado en 16 bytes. Para obtener más información sobre la alineación y el empaquetado constantes del búfer, vea [Reglas de empaquetado para variables constantes.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)

Ahora, aquí se muestra cómo se declara el búfer constante en el sombreador de vértices HLSL.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Todos los búferes (constante, textura, muestreador u otros) deben tener un registro definido para que la GPU pueda acceder a ellos. Cada fase del sombreador permite hasta 15 búferes constantes y cada búfer puede contener hasta 4096 variables constantes. La sintaxis de declaración de uso de registros es la siguiente:

-   **b:** _\#_ un registro para un búfer constante (**cbuffer**).
-   **t:** _\#_ un registro para un búfer de textura (**tbuffer**).
-   **s** _\#_ : un registro para un muestreador. (Un muestreador define el comportamiento de búsqueda de los elementos de textura en el recurso de textura).

Por ejemplo, hlsl para un sombreador de píxeles podría tomar una textura y un muestreador como entrada con una declaración como esta.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

Es su función asignar búferes constantes a los registros: al configurar la canalización, se asocia un búfer constante a la misma ranura a la que se le asignó en el archivo HLSL. Por ejemplo, en el tema anterior, la llamada a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica "0" para el primer parámetro. Esto indica a Direct3D que adjunte el recurso de búfer constante para registrar 0, lo que coincide con la asignación del búfer a **register(b0)** en el archivo HLSL.

## <a name="read-from-the-vertex-buffers"></a>Lectura de los búferes de vértices

El búfer de vértices proporciona los datos del triángulo para los objetos de escena a los sombreadores de vértices. Al igual que con el búfer constante, la estructura del búfer de vértices se declara en el código de C++, mediante reglas de empaquetado similares.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



No hay ningún formato estándar para los datos de vértices en Direct3D 11. En su lugar, definimos nuestro propio diseño de datos de vértice mediante un descriptor; los campos de datos se definen mediante una matriz de [**estructuras \_ \_ \_ DESC INPUT ELEMENT de D3D11.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) Aquí se muestra un diseño de entrada simple que describe el mismo formato de vértice que la estructura anterior:


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



Si agrega datos al formato de vértice al modificar el código de ejemplo, asegúrese de actualizar también el diseño de entrada o el sombreador no podrá interpretarlo. Puede modificar el diseño de vértices de la siguiente forma:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



En ese caso, modificaría la definición de diseño de entrada como se muestra a continuación.


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

Al igual que con el búfer constante, el sombreador de vértices tiene una definición de búfer correspondiente para los elementos de vértice entrantes. (Por eso hemos proporcionado una referencia al recurso del sombreador de vértices al crear el diseño de entrada: Direct3D valida el diseño de datos por vértice con la estructura de entrada del sombreador). Observe cómo la semántica coincide entre la definición de diseño de entrada y esta declaración de búfer HLSL. Sin embargo, `COLOR` tiene un "0" anexado a él. No es necesario agregar el 0 si solo tiene un elemento declarado en el diseño, pero es una buena práctica anexarlo en caso de que decida agregar más elementos de color en `COLOR` el futuro.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Pasar datos entre sombreadores

Los sombreadores toman tipos de entrada y devuelven tipos de salida de sus funciones principales tras la ejecución. Para el sombreador de vértices definido en la sección anterior, el tipo de entrada era la estructura VS INPUT y definimos un diseño de entrada y una estructura \_ de C++ correspondientes. Una matriz de esta estructura se usa para crear un búfer de vértices en el **método CreateCube.**

El sombreador de vértices devuelve una estructura PS INPUT, que debe contener como mínimo la posición final del vértice de \_ 4 componentes (float4). Este valor de posición debe tener el valor del sistema semántico, , declarado para que la GPU tenga los datos que necesita para `SV_POSITION` realizar el siguiente paso de dibujo. Observe que no hay una correspondencia 1:1 entre la salida del sombreador de vértices y la entrada del sombreador de píxeles; El sombreador de vértices devuelve una estructura para cada vértice que se le da, pero el sombreador de píxeles se ejecuta una vez para cada píxel. Esto se debe a que los datos por vértice pasan primero a través de la fase de rasterización. Esta fase decide qué píxeles "cubren" la geometría que está dibujando, calcula los datos interpolados por vértice para cada píxel y, a continuación, llama al sombreador de píxeles una vez para cada uno de esos píxeles. La interpolación es el comportamiento predeterminado al rasterizar los valores de salida y es esencial en particular para el procesamiento correcto de los datos vectoriales de salida (vectores claros, normales y tangentes por vértice, etc.).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Revisión del sombreador de vértices

El sombreador de vértices de ejemplo es muy sencillo: toma un vértice (posición y color), transforma la posición de las coordenadas del modelo en coordenadas proyectadas de perspectiva y la devuelve (junto con el color) al rasterizador. Observe que el valor de color se interpola junto con los datos de posición, lo que proporciona un valor diferente para cada píxel, aunque el sombreador de vértices no haya hecho ningún cálculo sobre el valor de color.


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



Un sombreador de vértices más complejo, como uno que configura los vértices de un objeto para el sombreado de Phong, podría ser más parecido a este. En este caso, aprovechamos el hecho de que los vectores y las normales se interpolan para aproximar una superficie de aspecto suave.

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

## <a name="review-the-pixel-shader"></a>Revisión del sombreador de píxeles

Este sombreador de píxeles de este ejemplo es posiblemente la cantidad mínima absoluta de código que puede tener en un sombreador de píxeles. Toma los datos de color de píxel interpolado generados durante la rasterización y los devuelve como salida, donde se escribirán en un destino de representación. ¡Qué pesado!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



La parte importante es la `SV_TARGET` semántica del valor del sistema en el valor devuelto. Indica que la salida se va a escribir en el destino de representación principal, que es el búfer de textura proporcionado a la cadena de intercambio para su presentación. Esto es necesario para los sombreadores de píxeles: sin los datos de color del sombreador de píxeles, Direct3D no tendría nada que mostrar.

Un ejemplo de un sombreador de píxeles más complejo para realizar el sombreado de Pong podría tener este aspecto. Puesto que los vectores y las normales se interpolaron, no es necesario calcularlos por píxel. Sin embargo, tenemos que volver a normalizarlos debido a cómo funciona la interpolación. Conceptualmente, es necesario "girar" gradualmente el vector desde la dirección del vértice A hasta la dirección en el vértice B, manteniendo su longitud; en su lugar, la interpolación de silbidos se corta a través de una línea recta entre los dos puntos de conexión vectoriales.

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

En otro ejemplo, el sombreador de píxeles toma sus propios búferes constantes que contienen información de luz y material. El diseño de entrada del sombreador de vértices se expandiría para incluir datos normales y se espera que la salida de ese sombreador de vértices incluya vectores transformados para el vértice, la luz y el vértice normal en el sistema de coordenadas de vista.

Si tiene búferes de textura y muestreadores con registros asignados **(t** y **s**, respectivamente), también puede acceder a ellos en el sombreador de píxeles.

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

Los sombreadores son herramientas muy eficaces que se pueden usar para generar recursos de procedimientos, como mapas de sombra o texturas de ruido. De hecho, las técnicas avanzadas requieren que piense en texturas de forma más abstracta, no como elementos visuales, sino como búferes. Contiene datos como información de alto u otros datos que se pueden muestrear en el paso final del sombreador de píxeles o en ese fotograma determinado como parte de un paso de efectos de varias fases. El muestreo múltiple es una herramienta eficaz y la red troncal de muchos efectos visuales modernos.

## <a name="next-steps"></a>Pasos siguientes

Esperamos que esté cómodo con DirectX 11 en este punto y esté listo para empezar a trabajar en el proyecto. Estos son algunos vínculos para ayudar a responder a otras preguntas que puede tener sobre el desarrollo con DirectX y C++:

-   [Desarrollar juegos](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Uso de Visual Studio para la programación de juegos de DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Tutoriales de ejemplo y desarrollo de juegos de DirectX](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Recursos de programación de juegos adicionales](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con recursos de dispositivo DirectX](work-with-dxgi.md)
</dt> <dt>

[Información sobre la canalización de representación de Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 