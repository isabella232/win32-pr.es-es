---
title: Tareas iniciales con la fase Stream-Output datos
description: En esta sección se describe cómo usar un sombreador de geometría con la fase de salida del flujo.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480fb75c126d89cc8db5ae79950e437ff411fcc60f3e9bf006662d0ecc2e3d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099618"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Tareas iniciales con la fase Stream-Output datos

En esta sección se describe cómo usar un sombreador de geometría con la fase de salida del flujo.

## <a name="compile-a-geometry-shader"></a>Compilar un sombreador de geometría

Este sombreador de geometría (GS) calcula una cara normal para cada triángulo y genera datos de coordenadas de posición, normales y de textura.


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



Teniendo en cuenta ese código, tenga en cuenta que un sombreador de geometría se parece mucho a un sombreador de vértices o píxeles, pero con las siguientes excepciones: el tipo devuelto por la función, las declaraciones de parámetros de entrada y la función intrínseca.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo de valor devuelto de función<br/></td>
<td>El tipo de valor devuelto de función hace una cosa, declara el número máximo de vértices que puede generar el sombreador. En este caso, <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

define la salida para que sea un máximo de 12 vértices.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Declaraciones de parámetros de entrada</p></td>
<td><p>Esta función toma dos parámetros de entrada:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>El primer parámetro es una matriz de vértices (3 en este caso) definida por una estructura GSPS_INPUT (que define los datos por vértice como una posición, una coordenada normal y una coordenada de textura). El primer parámetro también usa la palabra clave triangle, lo que significa que la fase del ensamblador de entrada debe generar datos al sombreador de geometría como uno de los tipos primitivos de triángulo (lista de triángulos o franja de triángulo).</p>
<p>El segundo parámetro es una secuencia de triángulo definida por el tipo TriangleStream &lt; GSPS_INPUTT &gt; . Esto significa que el parámetro es una matriz de triángulos, cada uno de los cuales se forma con tres vértices (que contienen los datos de los miembros de GSPS_INPUT).</p>
<p>Use las palabras clave triangle y trianglestream para identificar triángulos individuales o una secuencia de triángulos en un GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Función intrínseca</p></td>
<td><p>Las líneas de código de la función de sombreador usan funciones intrínsecas HLSL common-shader-core, excepto las dos últimas líneas, que llaman a Append y RestartStrip. Estas funciones solo están disponibles para un sombreador de geometría. Anexar informa al sombreador de geometría para anexar la salida a la franja actual; RestartStrip crea una nueva franja primitiva. Se crea implícitamente una nueva franja en cada invocación de la fase GS.</p></td>
</tr>
</tbody>
</table>



 

El resto del sombreador es muy similar a un sombreador de vértices o píxeles. El sombreador de geometría usa una estructura para declarar parámetros de entrada y marca el miembro de posición con la semántica SV POSITION para decir al hardware que se trata de \_ datos posicionales. La estructura de entrada identifica los otros dos parámetros de entrada como coordenadas de textura (aunque uno de ellos contendrá una cara normal). Si lo prefiere, puede usar su propia semántica personalizada para la cara normal.

Después de diseñar el sombreador de geometría, llame [**a D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) para compilar, como se muestra en el ejemplo de código siguiente.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Al igual que los sombreadores de vértices y píxeles, necesita una marca de sombreador para decir al compilador cómo desea que se compile el sombreador (para la depuración, optimizado para velocidad, entre otros), la función de punto de entrada y el modelo de sombreador con el que se va a validar. En este ejemplo se crea un sombreador de geometría creado a partir del archivo Tutorial13.fx, mediante la función GS. El sombreador se compila para el modelo de sombreador 4.0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Crear un objeto Geometry-Shader con salida de flujo

Una vez que sepa que va a transmitir los datos desde la geometría y que ha compilado correctamente el sombreador, el siguiente paso es llamar a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) para crear el objeto de sombreador geometry.

Pero en primer lugar, debe declarar la firma de entrada de fase de salida de aire (SO). Esta firma coincide o valida las salidas de GS y las entradas SO en el momento de la creación del objeto. El código siguiente es un ejemplo de la declaración SO.


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



Esta función toma varios parámetros, entre los que se incluyen:

-   Puntero al sombreador de geometría compilado (o sombreador de vértices si no habrá ningún sombreador de geometría y los datos se transmitirán directamente desde el sombreador de vértices). Para obtener información sobre cómo obtener este puntero, vea [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Puntero a una matriz de declaraciones que describen los datos de entrada de la fase de salida del flujo. (Vea [**D3D11 \_ SO DECLARATION \_ \_ ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)).) Puede proporcionar hasta 64 declaraciones, una para cada tipo diferente de elemento que se va a generar desde la fase SO. La matriz de entradas de declaración describe el diseño de datos independientemente de si solo se va a enlazar un búfer único o varios búferes para la salida del flujo.
-   Número de elementos escritos por la fase SO.
-   Puntero al objeto de sombreador de geometría que se crea (vea [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

En esta situación, el paso del búfer es NULL, el índice de la secuencia que se va a enviar al rasterizador es 0 y la interfaz de vinculación de clase es NULL.

La declaración de salida de flujo define la forma en que se escriben los datos en un recurso de búfer. Puede agregar tantos componentes como desee a la declaración de salida. Use la fase SO para escribir en un único recurso de búfer o en muchos recursos de búfer. Para un solo búfer, la fase SO puede escribir muchos elementos diferentes por vértice. Para varios búferes, la fase SO solo puede escribir un único elemento de datos por vértice en cada búfer.

Para usar la fase SO sin usar un sombreador de geometría, llame a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) y pase un puntero a un sombreador de vértices al *parámetro pShaderBytecode.*

## <a name="set-the-output-targets"></a>Establecer los destinos de salida

El último paso es establecer los búferes de la fase SO. Los datos se pueden transmitir a uno o varios búferes en memoria para usarlos más adelante. En el código siguiente se muestra cómo crear un búfer único que se puede usar para los datos de vértice, así como para la fase SO en la que se transmitirán datos.


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



Cree un búfer mediante una llamada [**a ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). En este ejemplo se muestra el uso predeterminado, que es típico para un recurso de búfer que se espera que la CPU actualice con bastante frecuencia. La marca de enlace identifica la fase de canalización a la que se puede enlazar el recurso. Cualquier recurso utilizado por la fase SO también debe crearse con la marca de enlace D3D10 \_ BIND \_ STREAM \_ OUTPUT.

Una vez que el búfer se haya creado correctamente, estaléctelo en el dispositivo actual mediante una llamada a [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Esta llamada toma el número de búferes, un puntero a los búferes y una matriz de desplazamientos (un desplazamiento en cada uno de los búferes que indica dónde empezar a escribir datos). Los datos se escribirán en estos búferes de salida de streaming cuando se llame a una función draw. Una variable interna realiza un seguimiento de la posición de dónde empezar a escribir datos en los búferes de salida de streaming, y las variables seguirán incrementando hasta que se vuelva a llamar a [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) y se especifique un nuevo valor de desplazamiento.

Todos los datos escritos en los búferes de destino serán valores de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase stream-output](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

