---
title: Tareas iniciales con la Stream-Output fase
description: En esta sección se describe cómo usar un sombreador de geometría con la fase de salida del flujo.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2e72d25177926c948f43996b6c57d42a7c557b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587882"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="3c8d5-103">Tareas iniciales con la Stream-Output fase</span><span class="sxs-lookup"><span data-stu-id="3c8d5-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="3c8d5-104">En esta sección se describe cómo usar un sombreador de geometría con la fase de salida del flujo.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="3c8d5-105">Compilar un sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="3c8d5-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="3c8d5-106">Este sombreador de geometría (GS) calcula una cara normal para cada triángulo y genera datos de coordenadas de posición, normales y de textura.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


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



<span data-ttu-id="3c8d5-107">Teniendo en cuenta ese código, tenga en cuenta que un sombreador de geometría se parece mucho a un sombreador de vértices o píxeles, pero con las siguientes excepciones: el tipo devuelto por la función, las declaraciones de parámetros de entrada y la función intrínseca.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c8d5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c8d5-108">Item</span></span></th>
<th><span data-ttu-id="3c8d5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c8d5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c8d5-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo de valor devuelto de función</span><span class="sxs-lookup"><span data-stu-id="3c8d5-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="3c8d5-111">El tipo de valor devuelto de función hace una cosa, declara el número máximo de vértices que puede generar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="3c8d5-112">En este caso, <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="3c8d5-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c8d5-113">define la salida para que sea un máximo de 12 vértices.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c8d5-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Declaraciones de parámetros de entrada</span><span class="sxs-lookup"><span data-stu-id="3c8d5-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="3c8d5-115">Esta función toma dos parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="3c8d5-115">This function takes two input parameters:</span></span></p>
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
<p><span data-ttu-id="3c8d5-116">El primer parámetro es una matriz de vértices (3 en este caso) definida por una estructura GSPS_INPUT (que define los datos por vértice como una posición, una coordenada normal y una coordenada de textura).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="3c8d5-117">El primer parámetro también usa la palabra clave triangle, lo que significa que la fase del ensamblador de entrada debe generar datos al sombreador de geometría como uno de los tipos primitivos de triángulo (lista de triángulos o franja de triángulo).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="3c8d5-118">El segundo parámetro es una secuencia de triángulo definida por el tipo TriangleStream &lt; GSPS_INPUTT &gt; .</span><span class="sxs-lookup"><span data-stu-id="3c8d5-118">The second parameter is a triangle stream defined by the type TriangleStream&lt;GSPS_INPUTT&gt;.</span></span> <span data-ttu-id="3c8d5-119">Esto significa que el parámetro es una matriz de triángulos, cada uno de los cuales se forma de tres vértices (que contienen los datos de los miembros de GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="3c8d5-120">Use las palabras clave triangle y trianglestream para identificar triángulos individuales o una secuencia de triángulos en un GS.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c8d5-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Función intrínseca</span><span class="sxs-lookup"><span data-stu-id="3c8d5-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="3c8d5-122">Las líneas de código de la función de sombreador usan funciones intrínsecas HLSL common-shader-core, excepto las dos últimas líneas, que llaman a Append y RestartStrip.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="3c8d5-123">Estas funciones solo están disponibles para un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="3c8d5-124">Anexar informa al sombreador de geometría para anexar la salida a la franja actual; RestartStrip crea una nueva franja primitiva.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="3c8d5-125">Se crea implícitamente una nueva franja en cada invocación de la fase GS.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3c8d5-126">El resto del sombreador es muy similar a un sombreador de vértices o píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="3c8d5-127">El sombreador de geometría usa una estructura para declarar parámetros de entrada y marca el miembro de posición con la semántica POSITION de SV para decir al hardware que se trata de \_ datos posicionales.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="3c8d5-128">La estructura de entrada identifica los otros dos parámetros de entrada como coordenadas de textura (aunque uno de ellos contendrá una cara normal).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="3c8d5-129">Si lo prefiere, puede usar su propia semántica personalizada para la cara normal.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="3c8d5-130">Después de diseñar el sombreador de geometría, llame [**a D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) para compilar, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="3c8d5-131">Al igual que los sombreadores de vértices y píxeles, necesita una marca de sombreador para decir al compilador cómo desea que se compile el sombreador (para la depuración, optimizado para velocidad, entre otros), la función de punto de entrada y el modelo de sombreador con el que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="3c8d5-132">En este ejemplo se crea un sombreador de geometría creado a partir del archivo Tutorial13.fx, mediante la función GS.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="3c8d5-133">El sombreador se compila para el modelo de sombreador 4.0.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="3c8d5-134">Crear un objeto Geometry-Shader con salida de flujo</span><span class="sxs-lookup"><span data-stu-id="3c8d5-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="3c8d5-135">Una vez que sepa que va a transmitir los datos desde la geometría y que ha compilado correctamente el sombreador, el siguiente paso es llamar a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) para crear el objeto de sombreador geometry.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="3c8d5-136">Pero en primer lugar, debe declarar la firma de entrada de la fase de salida de aire (SO).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="3c8d5-137">Esta firma coincide o valida las salidas de GS y las entradas SO en el momento de la creación del objeto.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="3c8d5-138">El código siguiente es un ejemplo de la declaración SO.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-138">The following code is an example of the SO declaration.</span></span>


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



<span data-ttu-id="3c8d5-139">Esta función toma varios parámetros, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="3c8d5-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="3c8d5-140">Puntero al sombreador de geometría compilado (o sombreador de vértices si no habrá ningún sombreador de geometría y los datos se transmitirán directamente desde el sombreador de vértices).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="3c8d5-141">Para obtener información sobre cómo obtener este puntero, vea [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="3c8d5-142">Puntero a una matriz de declaraciones que describen los datos de entrada de la fase de salida del flujo.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="3c8d5-143">(Vea [**D3D11 \_ SO DECLARATION \_ \_ ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)).) Puede proporcionar hasta 64 declaraciones, una para cada tipo diferente de elemento que se va a generar desde la fase SO.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="3c8d5-144">La matriz de entradas de declaración describe el diseño de datos independientemente de si solo se va a enlazar un búfer único o varios búferes para la salida del flujo.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="3c8d5-145">Número de elementos escritos por la fase SO.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="3c8d5-146">Puntero al objeto de sombreador de geometría que se crea (vea [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="3c8d5-147">En esta situación, el paso del búfer es NULL, el índice de la secuencia que se va a enviar al rasterizador es 0 y la interfaz de vinculación de clase es NULL.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="3c8d5-148">La declaración de salida de flujo define la forma en que se escriben los datos en un recurso de búfer.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="3c8d5-149">Puede agregar tantos componentes como desee a la declaración de salida.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="3c8d5-150">Use la fase SO para escribir en un único recurso de búfer o en muchos recursos de búfer.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="3c8d5-151">Para un solo búfer, la fase SO puede escribir muchos elementos diferentes por vértice.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="3c8d5-152">Para varios búferes, la fase SO solo puede escribir un único elemento de datos por vértice en cada búfer.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="3c8d5-153">Para usar la fase SO sin usar un sombreador de geometría, llame a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) y pase un puntero a un sombreador de vértices al *parámetro pShaderBytecode.*</span><span class="sxs-lookup"><span data-stu-id="3c8d5-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="3c8d5-154">Establecer los destinos de salida</span><span class="sxs-lookup"><span data-stu-id="3c8d5-154">Set the Output Targets</span></span>

<span data-ttu-id="3c8d5-155">El último paso es establecer los búferes de la fase SO.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="3c8d5-156">Los datos se pueden transmitir a uno o varios búferes en memoria para usarlos más adelante.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="3c8d5-157">En el código siguiente se muestra cómo crear un búfer único que se puede usar para los datos de vértice, así como para la fase SO en la que se transmitirán datos.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


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



<span data-ttu-id="3c8d5-158">Cree un búfer mediante una llamada [**a ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="3c8d5-159">En este ejemplo se muestra el uso predeterminado, que es típico para un recurso de búfer que se espera que la CPU actualice con bastante frecuencia.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="3c8d5-160">La marca de enlace identifica la fase de canalización a la que se puede enlazar el recurso.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="3c8d5-161">Cualquier recurso utilizado por la fase SO también debe crearse con la marca de enlace D3D10 \_ BIND \_ STREAM \_ OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="3c8d5-162">Una vez creado correctamente el búfer, estaléctelo en el dispositivo actual mediante una llamada a [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="3c8d5-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="3c8d5-163">Esta llamada toma el número de búferes, un puntero a los búferes y una matriz de desplazamientos (un desplazamiento en cada uno de los búferes que indica dónde empezar a escribir datos).</span><span class="sxs-lookup"><span data-stu-id="3c8d5-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="3c8d5-164">Los datos se escribirán en estos búferes de salida de streaming cuando se llame a una función draw.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="3c8d5-165">Una variable interna realiza un seguimiento de la posición de dónde empezar a escribir datos en los búferes de salida de streaming, y las variables seguirán incrementando hasta que se vuelva a llamar a [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) y se especifique un nuevo valor de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="3c8d5-166">Todos los datos escritos en los búferes de destino serán valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3c8d5-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c8d5-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c8d5-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8d5-168">Fase stream-output</span><span class="sxs-lookup"><span data-stu-id="3c8d5-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

