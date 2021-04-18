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
# <a name="getting-started-with-the-input-assembler-stage"></a>Introducción con la fase de Input-Assembler

Hay algunos pasos necesarios para inicializar la fase del ensamblador de entrada (IA). Por ejemplo, debe crear recursos de búfer con los datos de vértice que necesita la canalización, indicar a la fase de IA dónde están los búferes y qué tipo de datos contienen, y especificar el tipo de primitivas que se van a ensamblar a partir de los datos.

En este tema se describen los pasos básicos implicados en la configuración de la fase IA, que se muestra en la tabla siguiente.



| Paso                                                                                    | Descripción                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Crear búferes de entrada](#create-input-buffers)                                           | Crear e inicializar búferes de entrada con datos de vértices de entrada.                                           |
| [Crear el objeto Input-Layout](#create-the-input-layout-object)                       | Defina cómo se transmitirán los datos del búfer de vértices a la fase del IA mediante un objeto de diseño de entrada. |
| [Enlazar objetos a la fase Input-Assembler](#bind-objects-to-the-input-assembler-stage) | Enlazar los objetos creados (búferes de entrada y el objeto de diseño de entrada) a la fase de IA.                 |
| [Especificar el tipo primitivo](#specify-the-primitive-type)                               | Identifique cómo se ensamblarán los vértices en primitivos.                                          |
| [Llamar a métodos de Draw](#call-draw-methods)                                                 | Enviar los datos enlazados a la fase del IA a través de la canalización.                                             |



 

Una vez que comprenda estos pasos, continúe con el [uso de System-Generated valores](d3d10-graphics-programming-guide-input-assembler-stage-using.md).

## <a name="create-input-buffers"></a>Crear búferes de entrada

Hay dos tipos de búferes de entrada: [búferes de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y búferes de índice. Los búferes de vértices proporcionan datos de vértices a la fase de IA. Los búferes de índice son opcionales; proporcionan índices a los vértices del búfer de vértices. Puede crear uno o más búferes de vértices y, opcionalmente, un búfer de índice.

Después de crear los recursos de búfer, debe crear un objeto de diseño de entrada para describir el diseño de los datos en la fase del IA y, a continuación, debe enlazar los recursos de búfer a la fase de IA. No es necesario crear y enlazar búferes si los sombreadores no utilizan búferes. Para obtener un ejemplo de un sombreador de píxeles y vértices sencillo que dibuja un triángulo único, vea [usar la fase Input-Assembler sin búferes](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Para obtener ayuda con la creación de un búfer de vértices, vea [crear un búfer de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Para obtener ayuda con la creación de un búfer de índice, vea crear un búfer de índice.

## <a name="create-the-input-layout-object"></a>Crear el objeto Input-Layout

El objeto de diseño de entrada encapsula el estado de entrada de la fase de IA. Esto incluye una descripción de los datos de entrada que se enlazan a la fase de IA. Los datos se transmiten a la fase del IA desde la memoria, desde uno o más búferes de vértices. La descripción identifica los datos de entrada que están enlazados desde uno o más búferes de vértices y proporciona al tiempo de ejecución la capacidad de comprobar los tipos de datos de entrada con respecto a los tipos de parámetro de entrada de sombreador. Esta comprobación de tipos no solo comprueba si los tipos son compatibles, sino también que cada uno de los elementos que el sombreador requiere está disponible en los recursos de búfer.

Un objeto de diseño de entrada se crea a partir de una matriz de descripciones de elementos de entrada y un puntero al sombreador compilado (vea [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). La matriz contiene uno o varios elementos de entrada; cada elemento de entrada describe un elemento de datos de vértice único desde un búfer de vértice único. El conjunto completo de descripciones de elementos de entrada describe todos los elementos de datos de vértice de todos los búferes de vértices que se vincularán a la fase del ensamblador de entrada.

La descripción de diseño siguiente describe un búfer de vértice único que contiene tres elementos de datos de vértice:


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



Una descripción del elemento de entrada describe cada elemento incluido en un solo vértice en un búfer de vértices, incluidos el tamaño, el tipo, la ubicación y el propósito. Cada fila identifica el tipo de datos mediante la semántica, el índice semántico y el formato de datos. Una [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) es una cadena de texto que identifica cómo se utilizarán los datos. En este ejemplo, la primera fila identifica los datos de posición de 3 componentes (*XYZ*, por ejemplo); la segunda fila identifica los datos de textura de dos componentes (*UV*, por ejemplo); y la tercera fila identifica los datos normales.

En este ejemplo de una descripción del elemento de entrada, el índice semántico (que es el segundo parámetro) se establece en cero para las tres filas. El índice semántico ayuda a distinguir entre dos filas que usan la misma semántica. Dado que no hay ninguna semántica similar en este ejemplo, el índice semántico se puede establecer en su valor predeterminado, cero.

El tercer parámetro es el *formato*. El formato (vea [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) especifica el número de componentes por elemento y el tipo de datos, que define el tamaño de los datos de cada elemento. El formato se puede escribir totalmente en el momento de la creación de recursos o se puede crear un recurso con un **\_ formato de DXGI**, que identifica el número de componentes de un elemento, pero deja el tipo de datos sin definir.

### <a name="input-slots"></a>Ranuras de entrada

Los datos entran en la fase del IA a través de entradas llamadas *ranuras de entrada*, tal como se muestra en la siguiente ilustración. La fase IA tiene *n* ranuras de entrada, que están diseñadas para admitir hasta *n* búferes de vértices que proporcionan datos de entrada. Cada búfer de vértices debe estar asignado a una ranura diferente; Esta información se almacena en la declaración de diseño de entrada cuando se crea el objeto de diseño de entrada. También puede especificar un desplazamiento desde el inicio de cada búfer hasta el primer elemento del búfer que se va a leer.

![Ilustración de los espacios de entrada para la fase IA](images/d3d10-ia-slots.png)

Los dos parámetros siguientes son la *ranura de entrada* y el *desplazamiento de entrada*. Cuando se usan varios búferes, se pueden enlazar a uno o más espacios de entrada. El desplazamiento de entrada es el número de bytes entre el inicio del búfer y el principio de los datos.

### <a name="reusing-input-layout-objects"></a>Reutilizar objetos Input-Layout

Cada objeto de diseño de entrada se crea en función de una firma de sombreador; Esto permite que la API valide los elementos de objeto de diseño de entrada con la firma del sombreador de entrada para asegurarse de que hay una coincidencia exacta de los tipos y la semántica. Puede crear un único objeto de diseño de entrada para muchos sombreadores, siempre y cuando todas las firmas de entrada de sombreador coincidan exactamente.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Enlazar objetos a la fase Input-Assembler

Después de crear los recursos de búfer de vértices y un objeto de diseño de entrada, puede enlazarlos a la fase de IA llamando a [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) y [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). En el ejemplo siguiente se muestra el enlace de un búfer de vértice único y un objeto de diseño de entrada a la fase del IA:


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



El enlace del objeto de diseño de entrada solo requiere un puntero al objeto.

En el ejemplo anterior, se enlaza un solo búfer de vértices; sin embargo, varios búferes de vértices se pueden enlazar mediante una única llamada a [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)y el código siguiente muestra este tipo de llamada para enlazar tres búferes de vértice:


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



Un búfer de índice se enlaza a la fase del IA llamando a [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Especificar el tipo primitivo

Después de enlazar los búferes de entrada, se debe indicar a la fase del IA Cómo ensamblar los vértices en primitivas. Esto se hace especificando el [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) llamando a [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); el código siguiente llama a esta función para definir los datos como una lista de triángulos sin adyacencias:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



El resto de los tipos primitivos se enumeran en la [**topología de D3D \_ Primitive \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Llamar a métodos de Draw

Una vez que los recursos de entrada se han enlazado a la canalización, una aplicación llama a un método draw para representar primitivas. Hay varios métodos Draw, que se muestran en la tabla siguiente: Algunos utilizan búferes de índice, algunos datos de instancia de uso y algunos datos de reutilización de la fase de transmisión por secuencias como entrada para la fase del ensamblador de entrada.



| Dibujar métodos                                                                                  | Descripción                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::D RAW**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Dibuje primitivos no indizados sin instancia.                                                            |
| [**ID3D11DeviceContext::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Dibuje primitivos con instancias no indizadas.                                                                |
| [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Dibuje primitivos indizados sin instancia.                                                                |
| [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Dibuje primitivos con instancias indizadas.                                                                    |
| [**ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Dibuje primitivos no indexados sin instancia de los datos de entrada que provienen de la fase de streaming-output. |



 

Cada método draw representa un tipo de topología única. Durante la representación, se descartan los primitivos incompletos (aquellos que no tienen suficientes vértices, faltan índices, primitivas parciales, etc.).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 