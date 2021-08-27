---
description: 'Todos los recursos utilizados por la canalización de Direct3D derivan de dos tipos de recursos básicos: búferes y texturas. Un búfer es una colección de datos sin procesar (elementos); una textura es una colección de texturas (elementos de textura).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Tipos de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0f757eac93fac8c0ffd49641441fa4570824670dfcca9c3d271f954054548b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120173"
---
# <a name="resource-types-direct3d-10"></a>Tipos de recursos (Direct3D 10)

Todos los recursos utilizados por la canalización de Direct3D derivan de dos tipos de recursos básicos: [búferes](#buffer-resources) [y texturas.](#texture-resources) Un búfer es una colección de datos sin procesar (elementos); una textura es una colección de texturas (elementos de textura).

-   [Recursos de búfer](#buffer-resources)
    -   [Tipos de búfer](#buffer-types)
-   [Recursos de textura](#texture-resources)
    -   [Tipos de textura](#texture-types)
    -   [Subrecursos](#subresources)
    -   [Escritura fuerte frente a débil](#strong-vs-weak-typing)
-   [Temas relacionados](#related-topics)

Hay dos maneras de especificar completamente el diseño (o la superficie de memoria) de un recurso:



| Elemento                                                                                                 | Descripción                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Escrito<br/>             | Especifique completamente el tipo cuando se cree el recurso.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Sin tipo<br/> | Especifique completamente el tipo cuando el recurso esté enlazado a la canalización.<br/> |



 

## <a name="buffer-resources"></a>Recursos de búfer

Un recurso de búfer es una colección de datos totalmente con tipo. internamente, un búfer contiene elementos. Un elemento se forma de 1 a 4 componentes. Algunos ejemplos de tipos de datos de elementos son: un valor de datos empaquetados (como R8G8B8A8), un único entero de 8 bits, cuatro valores float de 32 bits. Estos tipos de datos se usan para almacenar datos, como un vector de posición, un vector normal, una coordenada de textura en un búfer de vértices, un índice en un búfer de índice o el estado del dispositivo.

Un búfer se crea como un recurso no estructurado. Dado que no está estructurado, un búfer no puede contener ningún nivel de mapa mip, no se filtra cuando se lee y no se puede multimuestrear.

### <a name="buffer-types"></a>Tipos de búfer

-   [Búfer de vértices](#vertex-buffer)
-   [Búfer de índice](#index-buffer)
-   [Búfer constante](#constant-buffer)

### <a name="vertex-buffer"></a>Búfer de vértices

Un búfer es una colección de elementos; un búfer de vértices contiene datos por vértice. El ejemplo más sencillo es un búfer de vértices que contiene un tipo de datos, como los datos de posición. Se puede visualizar como en la ilustración siguiente.

![ilustración de un búfer de vértices que contiene datos de posición](images/d3d10-resources-single-element-vb2.png)

Más a menudo, un búfer de vértices contiene todos los datos necesarios para especificar completamente los vértices 3D. Un ejemplo de esto podría ser un búfer de vértices que contiene coordenadas de posición por vértice, normal y de textura. Normalmente, estos datos se organizan como conjuntos de elementos por vértice, como se muestra en la ilustración siguiente.

![ilustración de un búfer de vértices que contiene datos de posición, normales y de textura](images/d3d10-vertex-buffer-element.png)

Este búfer de vértice contiene datos por vértice para ocho vértices; cada vértice almacena tres elementos (coordenadas de posición, normal y de textura). La posición y la normal se especifican normalmente mediante tres flotantes de 32 bits (DXGI FORMAT R32G32B32 FLOAT) y las coordenadas de textura mediante dos flotantes de \_ \_ 32 bits \_ (DXGI \_ FORMAT \_ R32G32 \_ FLOAT).

Para acceder a los datos desde un búfer de vértices, debe saber a qué vértice se va a acceder y a estos otros parámetros de búfer:

-   Desplazamiento: el número de bytes desde el inicio del búfer hasta los datos del primer vértice. El desplazamiento se proporciona a [**IASetVertexBuffers.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)
-   BaseVertexLocation: el número de bytes desde el desplazamiento hasta el primer vértice usado por la llamada a draw adecuada (vea [Draw Methods](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Antes de crear un búfer de vértices, debe definir su diseño mediante la creación de un [**objeto de diseño de entrada**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout); Para ello, se llama [**a CreateInputLayout.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout) Una vez creado el objeto de diseño de entrada, vincólelo a la fase de ensamblador de entrada mediante una [**llamada a IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Para crear un búfer de vértices, llame [**a CreateBuffer.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)

### <a name="index-buffer"></a>Búfer de índice

Un búfer de índice contiene un conjunto secuencial de índices de 16 o 32 bits; cada índice se usa para identificar un vértice en un búfer de vértices. El uso de un búfer de índice con uno o varios búferes de vértices para proporcionar datos a la fase IA se denomina indexación. Se puede visualizar un búfer de índice como en la ilustración siguiente.

![ilustración de un búfer de índice](images/d3d10-index-buffer.png)

Los índices secuenciales almacenados en un búfer de índice se encuentran con los parámetros siguientes:

-   Offset: el número de bytes desde el inicio del búfer hasta el primer índice. El desplazamiento se proporciona a [**IASetIndexBuffer.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)
-   StartIndexLocation: el número de bytes desde el desplazamiento hasta el primer vértice utilizado por la llamada a draw adecuada (vea [Draw Methods](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: el número de índices que se representará.

Para crear un búfer de índice, llame a [**CreateBuffer.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)

Un búfer de índice puede unir varias franjas de línea [o triángulo separando](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) cada una con un índice de corte de franja. Un índice de corte de bandas permite dibujar varias franjas de línea o triángulo con una sola llamada a draw. Un índice de corte seccionado es simplemente el valor máximo posible para el índice (0xffff para un índice de 16 bits, 0xffffffff para un índice de 32 bits). El índice de corte de bandas restablece el orden de desenlaz de las primitivas indexadas y se puede usar para eliminar la necesidad de triángulos degenerados que, de lo contrario, pueden ser necesarios para mantener el orden de desenlazado adecuado en una franja de triángulo. En la ilustración siguiente se muestra un ejemplo de un índice de corte seccionado.

![ilustración de un índice de corte seccionado](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Búfer constante

Direct3D 10 introdujo un nuevo búfer para proporcionar constantes de sombreador denominadas búfer constante de sombreador o simplemente búfer constante. Conceptualmente, se parece a un búfer de vértice de un solo elemento, como se muestra en la ilustración siguiente.

![ilustración de un búfer de constante de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento almacena una constante de componente de 1 a 4, determinada por el formato de los datos almacenados.

Los búferes constantes reducen el ancho de banda necesario para actualizar las constantes del sombreador, ya que permiten agrupar y confirmar constantes de sombreador al mismo tiempo en lugar de realizar llamadas individuales para confirmar cada constante por separado.

Para crear un búfer constante de sombreador, llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) y especifique la marca de enlace de búfer constante D3D10 \_ BIND CONSTANT BUFFER \_ \_ (vea [**D3D10 \_ BIND \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).

Para enlazar un búfer constante de sombreador a la canalización, llame a uno de estos [**métodos: GSSetConstantBuffers,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers) [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)o [**VSSetConstantBuffers.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers)

Tenga en cuenta que cuando se usa la interfaz [**ID3D10Effect,**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) el proceso de creación, enlace y envío de un búfer constante se controla mediante la instancia de la interfaz **ID3D10Effect.** En ese caso, solo es nescesary obtener la variable del efecto con uno de los métodos GetVariable como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) y actualizar la variable con uno de los métodos SetVariable como [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Para obtener un ejemplo del uso **de la interfaz ID3D10Effect para** administrar un búfer constante, vea el tutorial [07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Un sombreador sigue leyendo variables en un búfer constante directamente por nombre de variable de la misma manera que se leen las variables que no forman parte de un búfer constante.

Cada fase del sombreador permite hasta 15 búferes constantes de sombreador; cada búfer puede contener hasta 4096 constantes.

Use un búfer constante para almacenar los resultados de la fase stream-output.

Vea [Constantes de sombreador (HLSL de DirectX)](../direct3dhlsl/dx-graphics-hlsl-constants.md) para obtener un ejemplo de declaración de un búfer constante en un sombreador.

## <a name="texture-resources"></a>Recursos de textura

Un recurso de textura es una colección estructurada de datos diseñada para almacenar elementos de textura. A diferencia de los búferes, las texturas se pueden filtrar por muestreadores de textura a medida que las unidades de sombreador las leen. El tipo de textura afecta a cómo se filtra la textura. Un texel representa la unidad más pequeña de una textura que se puede leer o escribir en la canalización. Cada texel contiene de 1 a 4 componentes, organizados en uno de los formatos DXGI (vea [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Las texturas se crean como un recurso estructurado para que se conozca su tamaño. Sin embargo, cada textura se puede escribir o escribir menos en el momento de la creación de recursos, siempre y cuando el tipo esté totalmente especificado mediante una vista cuando la textura esté enlazada a la canalización.

-   [Tipos de textura](#texture-types)
-   [Subrecursos](#subresources)
-   [Escritura fuerte frente a débil](#strong-vs-weak-typing)

### <a name="texture-types"></a>Tipos de textura

Hay varios tipos de texturas: 1D, 2D, 3D, cada una de las cuales se puede crear con o sin mapas mip. Direct3D 10 también admite matrices de texturas y texturas multimuestreo.

-   [Textura 1D](#1d-texture)
-   [Matriz de textura 1D](#1d-texture-array)
-   [Textura 2D y matriz de textura 2D](#2d-texture-and-2d-texture-array)
-   [Textura 3D](#3d-texture)

### <a name="1d-texture"></a>Textura 1D

Una textura 1D en su forma más sencilla contiene datos de textura que se pueden abordar con una sola coordenada de textura; se puede visualizar como una matriz de elementos de textura, como se muestra en la ilustración siguiente.

![ilustración de una textura 1d](images/d3d10-1d-texture.png)

Cada texel contiene una serie de componentes de color según el formato de los datos almacenados. Si agrega más complejidad, puede crear una textura 1D con niveles de mapa mip, como se muestra en la ilustración siguiente.

![ilustración de una textura 1d con niveles de mapa mip](images/d3d10-resource-texture1d.png)

Un nivel de mapa mip es una textura que es una potencia de dos más pequeña que el nivel por encima de él. El nivel superior contiene la mayor cantidad de detalles; cada nivel posterior es menor. para un mapa mipmap 1D, el nivel más pequeño contiene un elemento texel. Los distintos niveles se identifican mediante un índice denominado LOD (nivel de detalle); Puede usar el LOD para acceder a una textura más pequeña al representar geometría que no está tan cerca de la cámara.

### <a name="1d-texture-array"></a>Matriz de textura 1D

Direct3D 10 también tiene una nueva estructura de datos para una matriz de texturas. Una matriz de texturas 1D tiene un aspecto conceptual similar al de la ilustración siguiente.

![ilustración de una matriz de textura 1d](images/d3d10-resource-texture1darray.png)

Esta matriz de texturas contiene tres texturas. Cada una de las tres texturas tiene un ancho de textura de 5 (que es el número de elementos de la primera capa). Cada textura también contiene un mapa mipmap de 3 capas.

Todas las matrices de texturas de Direct3D son una matriz homogéneo de texturas; esto significa que todas las texturas de una matriz de texturas deben tener el mismo formato y tamaño de datos (incluido el ancho de textura y el número de niveles de mapa mip). Puede crear matrices de textura de diferentes tamaños, siempre y cuando todas las texturas de cada matriz coincidan en tamaño.

### <a name="2d-texture-and-2d-texture-array"></a>Textura 2D y matriz de textura 2D

Un recurso Texture2D contiene una cuadrícula 2D de elementos de textura. Cada texel es direccionable mediante un vector u, v. Dado que es un recurso de textura, puede contener niveles de mapa mip y subrecursos. Un recurso de textura 2D totalmente rellenado se parece a la ilustración siguiente.

![ilustración de un recurso de textura 2d](images/d3d10-resource-texture2d.png)

Este recurso de textura contiene una sola textura de 3x5 con tres niveles de mapa mip.

Un recurso Texture2DArray es una matriz homogéneo de texturas 2D; es decir, cada textura tiene el mismo formato de datos y dimensiones (incluidos los niveles de mapa mip). Tiene un diseño similar al de la matriz de texturas 1D, salvo que las texturas ahora contienen datos 2D y, por tanto, tienen un aspecto similar al de la ilustración siguiente.

![ilustración de una matriz de recursos de textura 2d](images/d3d10-resource-texture2darray.png)

Esta matriz de texturas contiene tres texturas; cada textura es 3x5 con dos niveles de mapa mip.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Usar Texture2DArray como un cubo de textura

Un cubo de textura es una matriz de textura 2D que contiene 6 texturas, una para cada cara del cubo. Un cubo de textura totalmente rellenado tiene un aspecto similar al de la ilustración siguiente.

![ilustración de una matriz de recursos de textura 2d que representan un cubo de textura](images/d3d10-resource-texturecube.png)

Una matriz de texturas 2D que contiene 6 texturas se puede leer desde los sombreadores con las funciones intrínsecas del mapa de cubo, después de enlazarse a la canalización con una vista de textura de cubo. Los cubos de textura se abordan desde el sombreador con un vector 3D que señala desde el centro del cubo de textura.

### <a name="3d-texture"></a>Textura 3D

Un recurso Texture3D (también conocido como textura de volumen) contiene un volumen 3D de texturas. Puesto que es un recurso de textura, puede contener niveles de mapa mip. Una textura [**3D totalmente rellenada**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) es similar a la siguiente ilustración.

![ilustración de un recurso de textura 3D](images/d3d10-resource-texture3d.png)

Cuando un segmento mipmap de textura 3D se enlaza como una salida de destino de representación (con una vista render-target), la textura 3D se comporta de forma idéntica a una matriz de textura 2D con n segmentos. El segmento de representación determinado se elige en la fase del sombreador de geometría, declarando un componente escalar de los datos de salida como el valor del sistema \_ SV RenderTargetArrayIndex.

No hay ningún concepto de una matriz de texturas 3D; por lo tanto, un subcurso de textura 3D es un único nivel de mapa mip.

### <a name="subresources"></a>Subrecursos

La API de Direct3D 10 hace referencia a recursos completos o subconjuntos de recursos. Para especificar parte de los recursos, Direct3D ha acuñado el término subrecursos, lo que significa un subconjunto de un recurso.

Un búfer se define como un único subrecurso. Las texturas son un poco más complicadas, ya que hay varios tipos de textura diferentes (1D, 2D, etc.) algunos de los cuales admiten niveles de mapa mip o matrices de textura. A partir del caso más sencillo, una textura 1D se define como un único subrecurso, como se muestra en la ilustración siguiente.

![ilustración de una textura 1d](images/d3d10-1d-texture.png)

Esto significa que la matriz de elementos de textura que forma una textura 1D se encuentra en un único subrecurso.

Si expande una textura 1D con tres niveles de mapa mip, se puede visualizar de esta manera.

![ilustración de una textura 1d con niveles de mapa mip](images/d3d10-resource-texture1d.png)

Piense en esto como una sola textura que se conste de tres subtexturas. Cada subtexto se cuenta como un subcurso, por lo que esta textura 1D contiene 3 subrecursos. Un subtexto (o subcurso) se puede indexar mediante el nivel de detalle (LOD) para una sola textura. Cuando se usa una matriz de texturas, el acceso a un subtexto determinado requiere el LOD y la textura determinada. Como alternativa, la API combina estos dos fragmentos de información en un único índice de subrecurso de base cero, como se muestra aquí.

![ilustración de un índice de subrecurso de base cero](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Selección de subrecursos

Algunas API acceden a un recurso completo (por [**ejemplo, CopyResource),**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)otras acceden a una parte de un recurso (por [**ejemplo, UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) o [**CopySubresourceRegion).**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) Las API que acceden a una parte de un recurso suelen usar una descripción de vista (como [**D3D10 \_ TEXAS2D \_ ARRAY \_ DSV)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)para especificar los subrecursos a los que se va a acceder.

Estas figuras ilustran los términos usados por una descripción de vista al acceder a una matriz de texturas.

### <a name="array-slice"></a>Segmento de matriz

Dada una matriz de texturas, cada textura con mapas mip, un segmento de matriz (representado por el rectángulo blanco) incluye una textura y todos sus subtextos, como se muestra en la ilustración siguiente.

![ilustración de una unión de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Segmento mip

Un segmento mip (representado por el rectángulo blanco) incluye un nivel de mapa mip para cada textura de una matriz, como se muestra en la ilustración siguiente.

![ilustración de una unión mip](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selección de un único subrecurso

Puede usar estos dos tipos de segmentos para elegir un único subrecurso, como se muestra en la ilustración siguiente.

![ilustración de la elección de un subrecurso mediante un segmento de matriz y una unión mip](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selección de varios subrecursos

O bien, puede usar estos dos tipos de segmentos con el número de niveles de asignación mipmap o el número de texturas para elegir varios subrecursos.

![ilustración de la elección de varios subrecursos](images/d3d10-resource-subresources-2.png)

Independientemente del tipo de textura que use, con o sin mapas mip, con o sin una matriz de texturas, puede usar la función auxiliar [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)para calcular el índice de un subrecurso determinado.

### <a name="strong-vs-weak-typing"></a>Escritura fuerte frente a débil

La creación de un recurso totalmente tipo restringe el recurso al formato con el que se creó. Esto permite que el tiempo de ejecución optimice el acceso, [](d3d10-graphics-programming-guide-resources-mapping.md) especialmente si el recurso se crea con marcas que indican que la aplicación no puede asignarlo. Los recursos creados con un tipo específico no se pueden reinterpretar mediante el mecanismo de vista.

En un recurso de tipo menos, el tipo de datos es desconocido cuando se crea el recurso por primera vez. La aplicación debe elegir entre el tipo disponible menos formatos (vea [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Debe especificar el tamaño de la memoria que se va a asignar y si el tiempo de ejecución tendrá que generar los subtextos en un mapa mip. Sin embargo, el formato de datos exacto (si la memoria se interpretará como enteros, valores de punto flotante, enteros sin signo, etc.) no se determina hasta que el recurso se enlaza a la canalización con una vista. A medida que el formato de textura sigue siendo flexible hasta que la textura se enlaza a la canalización, el recurso se conoce como almacenamiento con tipos débiles. El almacenamiento con tipos débiles tiene la ventaja de que se puede reutilizar o reinterpretar (en otro formato) siempre y cuando el bit de componente del nuevo formato coincida con el número de bits del formato anterior.

Un único recurso se puede enlazar a varias fases de canalización, siempre y cuando cada una tenga una vista única, que califica totalmente los formatos en cada ubicación. Por ejemplo, un recurso creado con el formato DXGI \_ FORMAT \_ R32G32B32A32A32 TYPELESS podría usarse como \_ DXGI \_ FORMAT \_ R32G32B32A32 FLOAT y \_ DXGI FORMAT \_ \_ R32G32B32A32A32 \_ UINT en diferentes ubicaciones de la canalización simultáneamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
