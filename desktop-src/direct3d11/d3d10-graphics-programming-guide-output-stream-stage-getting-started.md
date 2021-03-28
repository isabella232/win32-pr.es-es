---
title: Introducción con la fase de Stream-Output
description: En esta sección se describe cómo usar un sombreador de geometría con la fase de salida de la secuencia.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984030"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Introducción con la fase de Stream-Output

En esta sección se describe cómo usar un sombreador de geometría con la fase de salida de la secuencia.

## <a name="compile-a-geometry-shader"></a>Compilar un sombreador de geometría

Este sombreador de geometría (GS) calcula una cara normal para cada triángulo y genera datos de coordenadas normal y de textura.


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



Teniendo en cuenta ese código, tenga en cuenta que un sombreador de geometría se parece mucho a un sombreador de vértices o de píxeles, pero con las siguientes excepciones: el tipo devuelto por la función, las declaraciones de parámetros de entrada y la función intrínseca.



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
<td>El tipo de valor devuelto de función realiza una acción, declara el número máximo de vértices que puede generar el sombreador. En este caso, <span data-codelanguage=""></span>
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

define la salida para que tenga un máximo de 12 vértices.</td>
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
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>El primer parámetro es una matriz de vértices (3 en este caso) definida por una estructura de GSPS_INPUT (que define los datos por vértice como una posición, una coordenada normal y de textura). El primer parámetro también usa la palabra clave triangular, lo que significa que la etapa del ensamblador de entrada debe generar los datos en el sombreador de geometría como uno de los tipos primitivos triangulares (lista de triángulos o franja de triángulo).</p>
<p>El segundo parámetro es una secuencia de triángulo definida por el tipo TriangleStream <GSPS_INPUT> . Esto significa que el parámetro es una matriz de triángulos, cada uno de los cuales se compone de tres vértices (que contienen los datos de los miembros de GSPS_INPUT).</p>
<p>Use las palabras clave Triangle y trianglestream para identificar triángulos individuales o un flujo de triángulos en un GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Función intrínseca</p></td>
<td><p>Las líneas de código de la función de sombreador usan funciones intrínsecas de HLSL Common-Shader-Core, excepto las dos últimas líneas, que llaman a Append y RestartStrip. Estas funciones solo están disponibles para un sombreador de geometría. Append informa al sombreador de geometría para que anexe la salida a la franja actual; RestartStrip crea una nueva franja primitiva. Se crea una nueva banda implícitamente en cada invocación de la fase GS.</p></td>
</tr>
</tbody>
</table>



 

El resto del sombreador es muy similar a un sombreador de vértices o de píxeles. El sombreador de geometría utiliza una estructura para declarar los parámetros de entrada y marca el miembro de posición con la semántica de posición de la VP \_ para indicar al hardware que se trata de datos posicionales. La estructura de entrada identifica los otros dos parámetros de entrada como coordenadas de textura (aunque uno de ellos contendrá una cara normal). Podría usar su propia semántica personalizada para la cara normal si lo prefiere.

Una vez diseñado el sombreador de geometría, llame a [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) para compilar como se muestra en el ejemplo de código siguiente.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Al igual que los sombreadores de píxeles y vértices, se necesita una marca de sombreador para indicar al compilador cómo desea que se compile el sombreador (para la depuración, optimizada para velocidad, etc.), la función de punto de entrada y el modelo de sombreador con el que realizar la validación. En este ejemplo se crea un sombreador de geometría generado a partir del archivo Tutorial13. FX mediante la función GS. El sombreador se compila para el modelo de sombreador 4,0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Creación de un objeto de Geometry-Shader con salida de flujo

Una vez que sepa que va a transmitir los datos de la geometría y que ha compilado correctamente el sombreador, el paso siguiente consiste en llamar a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) para crear el objeto de sombreador de geometría.

Pero en primer lugar, debe declarar la firma de entrada de la etapa de salida de la secuencia. Esta firma coincide o valida las salidas GS y las entradas de SO en el momento de la creación del objeto. El código siguiente es un ejemplo de la declaración de SO.


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

-   Puntero al sombreador de geometría compilado (o sombreador de vértices si no hay ningún sombreador de geometría presente y los datos se transmitirán directamente desde el sombreador de vértices). Para obtener información sobre cómo obtener este puntero, vea [obtener un puntero a un sombreador compilado](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Puntero a una matriz de declaraciones que describen los datos de entrada para la fase de salida de la secuencia. (Consulte [**D3D11 \_ para obtener la \_ \_ entrada de declaración**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)). Puede proporcionar hasta 64 declaraciones, una para cada tipo de elemento diferente que se va a mostrar desde la fase de. La matriz de entradas de declaración describe el diseño de los datos, independientemente de si solo se van a enlazar un único búfer o varios búferes para la salida de la secuencia.
-   Número de elementos que se escriben en la fase de.
-   Un puntero al objeto de sombreador de geometría que se crea (vea [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

En esta situación, el intervalo del búfer es NULL, el índice de la secuencia que se va a enviar al rasterizador es 0 y la interfaz de vinculación de clases es NULL.

La declaración de salida de flujo define la forma en que los datos se escriben en un recurso de búfer. Puede agregar tantos componentes como desee a la declaración de salida. Utilice la fase for para escribir en un único recurso de búfer o en muchos recursos de búfer. En el caso de un solo búfer, la fase for puede escribir muchos elementos diferentes por vértice. En el caso de varios búferes, la fase for solo puede escribir un único elemento de datos por vértice en cada búfer.

Para usar la fase for sin usar un sombreador de geometría, llame a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) y pase un puntero a un sombreador de vértices al parámetro *pShaderBytecode* .

## <a name="set-the-output-targets"></a>Establecimiento de los destinos de salida

El último paso es establecer los búferes de este modo. Los datos se pueden transmitir en uno o varios búferes de la memoria para su uso posterior. En el código siguiente se muestra cómo crear un búfer único que se puede usar para los datos de vértices, así como para la fase de creación de datos en streaming.


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



Cree un búfer mediante una llamada a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). En este ejemplo se muestra el uso predeterminado, que es habitual para un recurso de búfer que se espera que se actualice con bastante frecuencia por la CPU. La marca de enlace identifica la fase de canalización a la que se puede enlazar el recurso. Cualquier recurso usado por la fase SO también se debe crear con la salida de flujo de enlace D3D10 de la \_ secuencia de enlace \_ \_ .

Una vez que el búfer se crea correctamente, establézcalo en el dispositivo actual llamando a [**ID3D11DeviceContext:: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Esta llamada toma el número de búferes, un puntero a los búferes y una matriz de desplazamientos (un desplazamiento en cada uno de los búferes que indica dónde comenzar a escribir datos). Los datos se escribirán en estos búferes de salida de streaming cuando se llama a una función Draw. Una variable interna realiza un seguimiento de la posición en la que se comienza a escribir datos en los búferes de salida de streaming y que las variables continuarán aumentando hasta que se vuelva a llamar a [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) y se especifique un nuevo valor de desplazamiento.

Todos los datos que se escriben en los búferes de destino serán valores de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia: fase de salida](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

