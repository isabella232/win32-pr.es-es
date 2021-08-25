---
title: Tareas iniciales con la fase Input-Assembler de trabajo
description: Hay algunos pasos necesarios para inicializar la fase de ensamblador de entrada (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513e7452eebf157a80d4239127bf1d04a014375f7bbaf06e4f5814199d7ba053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858215"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Tareas iniciales con la fase Input-Assembler de trabajo

Hay algunos pasos necesarios para inicializar la fase de ensamblador de entrada (IA). Por ejemplo, debe crear recursos de búfer con los datos de vértices que necesita la canalización, indicar a la fase de IA dónde están los búferes y qué tipo de datos contienen, y especificar el tipo de primitivos que se ensamblan a partir de los datos.

Los pasos básicos implicados en la configuración de la fase de IA, que se muestran en la tabla siguiente, se tratan en este tema.



| Paso                                                                                    | Descripción                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Crear búferes de entrada](#create-input-buffers)                                           | Cree e inicialice búferes de entrada con datos de vértices de entrada.                                           |
| [Crear el objeto Input-Layout](#create-the-input-layout-object)                       | Defina cómo se transmitirán los datos del búfer de vértices a la fase IA mediante un objeto de diseño de entrada. |
| [Enlazar objetos a la fase Input-Assembler datos](#bind-objects-to-the-input-assembler-stage) | Enlace los objetos creados (búferes de entrada y el objeto de diseño de entrada) a la fase IA.                 |
| [Especificar el tipo primitivo](#specify-the-primitive-type)                               | Identifique cómo se ensamblarán los vértices en primitivos.                                          |
| [Llamar a métodos draw](#call-draw-methods)                                                 | Envíe los datos enlazados a la fase de IA a través de la canalización.                                             |



 

Después de comprender estos pasos, pase a Using System-Generated Values (Usar [System-Generated valores ).](d3d10-graphics-programming-guide-input-assembler-stage-using.md)

## <a name="create-input-buffers"></a>Crear búferes de entrada

Hay dos tipos de búferes de entrada: búferes [de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e búferes de índice. Los búferes de vértices suministran datos de vértices a la fase IA. Los búferes de índice son opcionales; proporcionan índices a los vértices del búfer de vértices. Puede crear uno o varios búferes de vértices y, opcionalmente, un búfer de índice.

Después de crear los recursos de búfer, debe crear un objeto de diseño de entrada para describir el diseño de datos en la fase IA y, a continuación, debe enlazar los recursos de búfer a la fase de IA. No es necesario crear y enlazar búferes si los sombreadores no usan búferes. Para obtener un ejemplo de un sombreador de vértices y píxeles simple que dibuja un triángulo único, vea Using the Input-Assembler Stage without Buffers (Uso de la fase de Input-Assembler [sin búferes).](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)

Para obtener ayuda con la creación de un búfer de vértices, vea [Crear un búfer de vértices.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating) Para obtener ayuda con la creación de un búfer de índice, consulte Creación de un búfer de índice.

## <a name="create-the-input-layout-object"></a>Crear el objeto Input-Layout

El objeto de diseño de entrada encapsula el estado de entrada de la fase IA. Esto incluye una descripción de los datos de entrada enlazados a la fase IA. Los datos se transmiten a la fase IA desde la memoria, desde uno o varios búferes de vértice. La descripción identifica los datos de entrada enlazados desde uno o varios búferes de vértice y ofrece al tiempo de ejecución la capacidad de comprobar los tipos de datos de entrada con los tipos de parámetros de entrada del sombreador. Esta comprobación de tipos no solo comprueba que los tipos son compatibles, sino que cada uno de los elementos que requiere el sombreador está disponible en los recursos de búfer.

Se crea un objeto de diseño de entrada a partir de una matriz de descripciones de elementos de entrada y un puntero al sombreador compilado (vea [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). La matriz contiene uno o varios elementos de entrada; cada elemento de entrada describe un único elemento de datos de vértice de un solo búfer de vértice. El conjunto completo de descripciones de elementos de entrada describe todos los elementos de datos de vértice de todos los búferes de vértices que se vincularán a la fase del ensamblador de entrada.

En la descripción de diseño siguiente se describe un búfer de vértice único que contiene tres elementos de datos de vértice:


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



Una descripción de elemento de entrada describe cada elemento contenido por un solo vértice en un búfer de vértice, incluido el tamaño, el tipo, la ubicación y el propósito. Cada fila identifica el tipo de datos mediante la semántica, el índice semántico y el formato de datos. Una [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) es una cadena de texto que identifica cómo se usarán los datos. En este ejemplo, la primera fila identifica los datos de posición de tres componentes *(xyz,* por ejemplo); la segunda fila identifica los datos de textura de 2 componentes *(UV,* por ejemplo); y la tercera fila identifica los datos normales.

En este ejemplo de una descripción de elemento de entrada, el índice semántico (que es el segundo parámetro) se establece en cero para las tres filas. El índice semántico ayuda a distinguir entre dos filas que usan la misma semántica. Puesto que no hay ninguna semántica similar en este ejemplo, el índice semántico se puede establecer en su valor predeterminado, cero.

El tercer parámetro es el *formato*. El formato (vea [**DXGI \_ FORMAT)**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)especifica el número de componentes por elemento y el tipo de datos , que define el tamaño de los datos para cada elemento. El formato se puede escribir completamente en el momento de la creación de recursos, o puede crear un recurso mediante un **FORMATO DXGI \_**, que identifica el número de componentes de un elemento, pero deja el tipo de datos sin definir.

### <a name="input-slots"></a>Ranuras de entrada

Los datos entran en la fase IA a través de entradas denominadas *ranuras de entrada,* como se muestra en la ilustración siguiente. La fase IA tiene *n ranuras* de entrada, que están diseñadas para alojar hasta *n* búferes de vértices que proporcionan datos de entrada. Cada búfer de vértice debe asignarse a una ranura diferente; esta información se almacena en la declaración input-layout cuando se crea el objeto input-layout. También puede especificar un desplazamiento desde el inicio de cada búfer hasta el primer elemento del búfer que se va a leer.

![ilustración de las ranuras de entrada para la fase ia](images/d3d10-ia-slots.png)

Los dos parámetros siguientes son la ranura *de entrada y* el desplazamiento de *entrada.* Cuando se usan varios búferes, se pueden enlazar a una o varias ranuras de entrada. El desplazamiento de entrada es el número de bytes entre el inicio del búfer y el principio de los datos.

### <a name="reusing-input-layout-objects"></a>Volver a Input-Layout objetos

Cada objeto de diseño de entrada se crea en función de una firma de sombreador; esto permite que la API valide los elementos input-layout-object con la firma de entrada del sombreador para asegurarse de que hay una coincidencia exacta de tipos y semántica. Puede crear un único objeto de diseño de entrada para muchos sombreadores, siempre y cuando todas las firmas de entrada del sombreador coincidan exactamente.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Enlazar objetos a la fase Input-Assembler datos

Después de crear recursos de búfer de vértices y un objeto de diseño de entrada, puede enlazarlos a la fase IA llamando a [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). En el ejemplo siguiente se muestra el enlace de un búfer de vértice único y un objeto de diseño de entrada a la fase IA:


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



Enlazar el objeto de diseño de entrada solo requiere un puntero al objeto .

En el ejemplo anterior, se enlaza un solo búfer de vértice; Sin embargo, varios búferes de vértices se pueden enlazar mediante una sola llamada a [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)y el código siguiente muestra una llamada de este tipo para enlazar tres búferes de vértice:


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



Un búfer de índice se enlaza a la fase IA mediante una llamada [**a ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Especificar el tipo primitivo

Una vez enlazados los búferes de entrada, se debe decir a la fase IA cómo ensamblar los vértices en primitivos. Para ello, se [](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) especifica el tipo primitivo llamando a [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); El código siguiente llama a esta función para definir los datos como una lista de triángulos sin adyacencia:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



El resto de los tipos primitivos se enumeran en [**TOPOLOGÍA \_ PRIMITIVA \_ D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Llamar a métodos draw

Una vez enlazados los recursos de entrada a la canalización, una aplicación llama a un método draw para representar primitivas. Hay varios métodos de dibujo, que se muestran en la tabla siguiente; Algunos usan búferes de índice, otros usan datos de instancia y otros reutilizan datos de la fase streaming-output como entrada a la fase input-assembler.



| Draw (métodos)                                                                                  | Descripción                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::D raw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Dibuje primitivas no indizadas y sin instancias.                                                            |
| [**ID3D11DeviceContext::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Dibuje primitivas no indizadas con instancias.                                                                |
| [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Dibuje primitivas indexadas sin instancias.                                                                |
| [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Dibuje primitivas indizadas e instancias.                                                                    |
| [**ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Dibuje primitivas no indizadas y sin instancias a partir de datos de entrada que proceden de la fase streaming-output. |



 

Cada método draw representa un único tipo de topología. Durante la representación, las primitivas incompletas (aquellas que no tienen suficientes vértices, carecen de índices, primitivas parciales, entre otras) se descartan silenciosamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 