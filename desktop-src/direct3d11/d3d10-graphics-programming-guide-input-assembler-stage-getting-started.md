---
title: Introducción con la fase de Input-Assembler
description: Hay algunos pasos necesarios para inicializar la fase del ensamblador de entrada (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420956"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="bee4a-103">Introducción con la fase de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="bee4a-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="bee4a-104">Hay algunos pasos necesarios para inicializar la fase del ensamblador de entrada (IA).</span><span class="sxs-lookup"><span data-stu-id="bee4a-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="bee4a-105">Por ejemplo, debe crear recursos de búfer con los datos de vértice que necesita la canalización, indicar a la fase de IA dónde están los búferes y qué tipo de datos contienen, y especificar el tipo de primitivas que se van a ensamblar a partir de los datos.</span><span class="sxs-lookup"><span data-stu-id="bee4a-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="bee4a-106">En este tema se describen los pasos básicos implicados en la configuración de la fase IA, que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bee4a-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="bee4a-107">Paso</span><span class="sxs-lookup"><span data-stu-id="bee4a-107">Step</span></span>                                                                                    | <span data-ttu-id="bee4a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee4a-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee4a-109">Crear búferes de entrada</span><span class="sxs-lookup"><span data-stu-id="bee4a-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="bee4a-110">Crear e inicializar búferes de entrada con datos de vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="bee4a-111">Crear el objeto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="bee4a-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="bee4a-112">Defina cómo se transmitirán los datos del búfer de vértices a la fase del IA mediante un objeto de diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="bee4a-113">Enlazar objetos a la fase Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="bee4a-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="bee4a-114">Enlazar los objetos creados (búferes de entrada y el objeto de diseño de entrada) a la fase de IA.</span><span class="sxs-lookup"><span data-stu-id="bee4a-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="bee4a-115">Especificar el tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="bee4a-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="bee4a-116">Identifique cómo se ensamblarán los vértices en primitivos.</span><span class="sxs-lookup"><span data-stu-id="bee4a-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="bee4a-117">Llamar a métodos de Draw</span><span class="sxs-lookup"><span data-stu-id="bee4a-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="bee4a-118">Enviar los datos enlazados a la fase del IA a través de la canalización.</span><span class="sxs-lookup"><span data-stu-id="bee4a-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="bee4a-119">Una vez que comprenda estos pasos, continúe con el [uso de System-Generated valores](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span><span class="sxs-lookup"><span data-stu-id="bee4a-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="bee4a-120">Crear búferes de entrada</span><span class="sxs-lookup"><span data-stu-id="bee4a-120">Create Input Buffers</span></span>

<span data-ttu-id="bee4a-121">Hay dos tipos de búferes de entrada: [búferes de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y búferes de índice.</span><span class="sxs-lookup"><span data-stu-id="bee4a-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="bee4a-122">Los búferes de vértices proporcionan datos de vértices a la fase de IA.</span><span class="sxs-lookup"><span data-stu-id="bee4a-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="bee4a-123">Los búferes de índice son opcionales; proporcionan índices a los vértices del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="bee4a-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="bee4a-124">Puede crear uno o más búferes de vértices y, opcionalmente, un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="bee4a-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="bee4a-125">Después de crear los recursos de búfer, debe crear un objeto de diseño de entrada para describir el diseño de los datos en la fase del IA y, a continuación, debe enlazar los recursos de búfer a la fase de IA.</span><span class="sxs-lookup"><span data-stu-id="bee4a-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="bee4a-126">No es necesario crear y enlazar búferes si los sombreadores no utilizan búferes.</span><span class="sxs-lookup"><span data-stu-id="bee4a-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="bee4a-127">Para obtener un ejemplo de un sombreador de píxeles y vértices sencillo que dibuja un triángulo único, vea [usar la fase Input-Assembler sin búferes](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="bee4a-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="bee4a-128">Para obtener ayuda con la creación de un búfer de vértices, vea [crear un búfer de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="bee4a-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="bee4a-129">Para obtener ayuda con la creación de un búfer de índice, vea crear un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="bee4a-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="bee4a-130">Crear el objeto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="bee4a-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="bee4a-131">El objeto de diseño de entrada encapsula el estado de entrada de la fase de IA.</span><span class="sxs-lookup"><span data-stu-id="bee4a-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="bee4a-132">Esto incluye una descripción de los datos de entrada que se enlazan a la fase de IA.</span><span class="sxs-lookup"><span data-stu-id="bee4a-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="bee4a-133">Los datos se transmiten a la fase del IA desde la memoria, desde uno o más búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="bee4a-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="bee4a-134">La descripción identifica los datos de entrada que están enlazados desde uno o más búferes de vértices y proporciona al tiempo de ejecución la capacidad de comprobar los tipos de datos de entrada con respecto a los tipos de parámetro de entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bee4a-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="bee4a-135">Esta comprobación de tipos no solo comprueba si los tipos son compatibles, sino también que cada uno de los elementos que el sombreador requiere está disponible en los recursos de búfer.</span><span class="sxs-lookup"><span data-stu-id="bee4a-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="bee4a-136">Un objeto de diseño de entrada se crea a partir de una matriz de descripciones de elementos de entrada y un puntero al sombreador compilado (vea [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span><span class="sxs-lookup"><span data-stu-id="bee4a-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="bee4a-137">La matriz contiene uno o varios elementos de entrada; cada elemento de entrada describe un elemento de datos de vértice único desde un búfer de vértice único.</span><span class="sxs-lookup"><span data-stu-id="bee4a-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="bee4a-138">El conjunto completo de descripciones de elementos de entrada describe todos los elementos de datos de vértice de todos los búferes de vértices que se vincularán a la fase del ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="bee4a-139">La descripción de diseño siguiente describe un búfer de vértice único que contiene tres elementos de datos de vértice:</span><span class="sxs-lookup"><span data-stu-id="bee4a-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="bee4a-140">Una descripción del elemento de entrada describe cada elemento incluido en un solo vértice en un búfer de vértices, incluidos el tamaño, el tipo, la ubicación y el propósito.</span><span class="sxs-lookup"><span data-stu-id="bee4a-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="bee4a-141">Cada fila identifica el tipo de datos mediante la semántica, el índice semántico y el formato de datos.</span><span class="sxs-lookup"><span data-stu-id="bee4a-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="bee4a-142">Una [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) es una cadena de texto que identifica cómo se utilizarán los datos.</span><span class="sxs-lookup"><span data-stu-id="bee4a-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="bee4a-143">En este ejemplo, la primera fila identifica los datos de posición de 3 componentes (*XYZ*, por ejemplo); la segunda fila identifica los datos de textura de dos componentes (*UV*, por ejemplo); y la tercera fila identifica los datos normales.</span><span class="sxs-lookup"><span data-stu-id="bee4a-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="bee4a-144">En este ejemplo de una descripción del elemento de entrada, el índice semántico (que es el segundo parámetro) se establece en cero para las tres filas.</span><span class="sxs-lookup"><span data-stu-id="bee4a-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="bee4a-145">El índice semántico ayuda a distinguir entre dos filas que usan la misma semántica.</span><span class="sxs-lookup"><span data-stu-id="bee4a-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="bee4a-146">Dado que no hay ninguna semántica similar en este ejemplo, el índice semántico se puede establecer en su valor predeterminado, cero.</span><span class="sxs-lookup"><span data-stu-id="bee4a-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="bee4a-147">El tercer parámetro es el *formato*.</span><span class="sxs-lookup"><span data-stu-id="bee4a-147">The third parameter is the *format*.</span></span> <span data-ttu-id="bee4a-148">El formato (vea [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) especifica el número de componentes por elemento y el tipo de datos, que define el tamaño de los datos de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="bee4a-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="bee4a-149">El formato se puede escribir totalmente en el momento de la creación de recursos o se puede crear un recurso con un **\_ formato de DXGI**, que identifica el número de componentes de un elemento, pero deja el tipo de datos sin definir.</span><span class="sxs-lookup"><span data-stu-id="bee4a-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="bee4a-150">Ranuras de entrada</span><span class="sxs-lookup"><span data-stu-id="bee4a-150">Input Slots</span></span>

<span data-ttu-id="bee4a-151">Los datos entran en la fase del IA a través de entradas llamadas *ranuras de entrada*, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="bee4a-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="bee4a-152">La fase IA tiene *n* ranuras de entrada, que están diseñadas para admitir hasta *n* búferes de vértices que proporcionan datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="bee4a-153">Cada búfer de vértices debe estar asignado a una ranura diferente; Esta información se almacena en la declaración de diseño de entrada cuando se crea el objeto de diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="bee4a-154">También puede especificar un desplazamiento desde el inicio de cada búfer hasta el primer elemento del búfer que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="bee4a-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![Ilustración de los espacios de entrada para la fase IA](images/d3d10-ia-slots.png)

<span data-ttu-id="bee4a-156">Los dos parámetros siguientes son la *ranura de entrada* y el *desplazamiento de entrada*.</span><span class="sxs-lookup"><span data-stu-id="bee4a-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="bee4a-157">Cuando se usan varios búferes, se pueden enlazar a uno o más espacios de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="bee4a-158">El desplazamiento de entrada es el número de bytes entre el inicio del búfer y el principio de los datos.</span><span class="sxs-lookup"><span data-stu-id="bee4a-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="bee4a-159">Reutilizar objetos Input-Layout</span><span class="sxs-lookup"><span data-stu-id="bee4a-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="bee4a-160">Cada objeto de diseño de entrada se crea en función de una firma de sombreador; Esto permite que la API valide los elementos de objeto de diseño de entrada con la firma del sombreador de entrada para asegurarse de que hay una coincidencia exacta de los tipos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="bee4a-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="bee4a-161">Puede crear un único objeto de diseño de entrada para muchos sombreadores, siempre y cuando todas las firmas de entrada de sombreador coincidan exactamente.</span><span class="sxs-lookup"><span data-stu-id="bee4a-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="bee4a-162">Enlazar objetos a la fase Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="bee4a-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="bee4a-163">Después de crear los recursos de búfer de vértices y un objeto de diseño de entrada, puede enlazarlos a la fase de IA llamando a [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) y [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span><span class="sxs-lookup"><span data-stu-id="bee4a-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="bee4a-164">En el ejemplo siguiente se muestra el enlace de un búfer de vértice único y un objeto de diseño de entrada a la fase del IA:</span><span class="sxs-lookup"><span data-stu-id="bee4a-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="bee4a-165">El enlace del objeto de diseño de entrada solo requiere un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="bee4a-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="bee4a-166">En el ejemplo anterior, se enlaza un solo búfer de vértices; sin embargo, varios búferes de vértices se pueden enlazar mediante una única llamada a [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)y el código siguiente muestra este tipo de llamada para enlazar tres búferes de vértice:</span><span class="sxs-lookup"><span data-stu-id="bee4a-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="bee4a-167">Un búfer de índice se enlaza a la fase del IA llamando a [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="bee4a-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="bee4a-168">Especificar el tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="bee4a-168">Specify the Primitive Type</span></span>

<span data-ttu-id="bee4a-169">Después de enlazar los búferes de entrada, se debe indicar a la fase del IA Cómo ensamblar los vértices en primitivas.</span><span class="sxs-lookup"><span data-stu-id="bee4a-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="bee4a-170">Esto se hace especificando el [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) llamando a [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); el código siguiente llama a esta función para definir los datos como una lista de triángulos sin adyacencias:</span><span class="sxs-lookup"><span data-stu-id="bee4a-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="bee4a-171">El resto de los tipos primitivos se enumeran en la [**topología de D3D \_ Primitive \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span><span class="sxs-lookup"><span data-stu-id="bee4a-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="bee4a-172">Llamar a métodos de Draw</span><span class="sxs-lookup"><span data-stu-id="bee4a-172">Call Draw Methods</span></span>

<span data-ttu-id="bee4a-173">Una vez que los recursos de entrada se han enlazado a la canalización, una aplicación llama a un método draw para representar primitivas.</span><span class="sxs-lookup"><span data-stu-id="bee4a-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="bee4a-174">Hay varios métodos Draw, que se muestran en la tabla siguiente: Algunos utilizan búferes de índice, algunos datos de instancia de uso y algunos datos de reutilización de la fase de transmisión por secuencias como entrada para la fase del ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="bee4a-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="bee4a-175">Dibujar métodos</span><span class="sxs-lookup"><span data-stu-id="bee4a-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="bee4a-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee4a-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bee4a-177">**ID3D11DeviceContext::D RAW**</span><span class="sxs-lookup"><span data-stu-id="bee4a-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="bee4a-178">Dibuje primitivos no indizados sin instancia.</span><span class="sxs-lookup"><span data-stu-id="bee4a-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="bee4a-179">**ID3D11DeviceContext::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="bee4a-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="bee4a-180">Dibuje primitivos con instancias no indizadas.</span><span class="sxs-lookup"><span data-stu-id="bee4a-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="bee4a-181">**ID3D11DeviceContext::D rawIndexed**</span><span class="sxs-lookup"><span data-stu-id="bee4a-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="bee4a-182">Dibuje primitivos indizados sin instancia.</span><span class="sxs-lookup"><span data-stu-id="bee4a-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="bee4a-183">**ID3D11DeviceContext::D rawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="bee4a-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="bee4a-184">Dibuje primitivos con instancias indizadas.</span><span class="sxs-lookup"><span data-stu-id="bee4a-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="bee4a-185">**ID3D11DeviceContext::D rawAuto**</span><span class="sxs-lookup"><span data-stu-id="bee4a-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="bee4a-186">Dibuje primitivos no indexados sin instancia de los datos de entrada que provienen de la fase de streaming-output.</span><span class="sxs-lookup"><span data-stu-id="bee4a-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="bee4a-187">Cada método draw representa un tipo de topología única.</span><span class="sxs-lookup"><span data-stu-id="bee4a-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="bee4a-188">Durante la representación, se descartan los primitivos incompletos (aquellos que no tienen suficientes vértices, faltan índices, primitivas parciales, etc.).</span><span class="sxs-lookup"><span data-stu-id="bee4a-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bee4a-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bee4a-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee4a-190">Fase del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="bee4a-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 