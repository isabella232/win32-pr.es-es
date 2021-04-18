---
description: 'Todos los recursos utilizados por la canalización de Direct3D derivan de dos tipos de recursos básicos: búferes y texturas. Un búfer es una colección de datos sin procesar (elementos); una textura es una colección de textura (elementos de textura).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Tipos de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec6ec9b57a2e504c137d424b19c61f2353d685e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569420"
---
# <a name="resource-types-direct3d-10"></a>Tipos de recursos (Direct3D 10)

Todos los recursos utilizados por la canalización de Direct3D derivan de dos tipos de recursos básicos: [búferes](#buffer-resources) y [texturas](#texture-resources). Un búfer es una colección de datos sin procesar (elementos); una textura es una colección de textura (elementos de textura).

-   [Recursos de búfer](#buffer-resources)
    -   [Tipos de búfer](#buffer-types)
-   [Recursos de textura](#texture-resources)
    -   [Tipos de textura](#texture-types)
    -   [Subrecursos](#subresources)
    -   [Strong frente a tipos débiles](#strong-vs-weak-typing)
-   [Temas relacionados](#related-topics)

Hay dos maneras de especificar por completo el diseño (o la superficie de memoria) de un recurso:



| Elemento                                                                                                 | Descripción                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Con tipo<br/>             | Especifique totalmente el tipo cuando se cree el recurso.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Sin tipo<br/> | Especifique totalmente el tipo cuando el recurso esté enlazado a la canalización.<br/> |



 

## <a name="buffer-resources"></a>Recursos de búfer

Un recurso de búfer es una colección de datos totalmente tipados; internamente, un búfer contiene elementos. Un elemento se compone de 1 a 4 componentes. Algunos ejemplos de tipos de datos de elementos son: un valor de datos empaquetado (como R8G8B8A8), un solo entero de 8 bits, valores Float de 4 32 bits. Estos tipos de datos se usan para almacenar datos, como un vector de posición, un vector normal, una coordenada de textura en un búfer de vértices, un índice en un búfer de índice o el estado del dispositivo.

Un búfer se crea como un recurso no estructurado. Dado que no está estructurado, un búfer no puede contener ningún nivel de mipmap, no se filtrará cuando se lea y no se podrá realizar un muestreo multimuestreado.

### <a name="buffer-types"></a>Tipos de búfer

-   [Búfer de vértices](#vertex-buffer)
-   [Búfer de índice](#index-buffer)
-   [Búfer de constantes](#constant-buffer)

### <a name="vertex-buffer"></a>Búfer de vértices

Un búfer es una colección de elementos; un búfer de vértice contiene datos por vértice. El ejemplo más sencillo es un búfer de vértices que contiene un tipo de datos, como los datos de posición. Se puede visualizar como la siguiente ilustración.

![Ilustración de un búfer de vértices que contiene datos de posición](images/d3d10-resources-single-element-vb2.png)

Con mayor frecuencia, un búfer de vértice contiene todos los datos necesarios para especificar por completo los vértices 3D. Un ejemplo de esto podría ser un búfer de vértices que contenga la posición por vértice, las coordenadas normales y de textura. Normalmente, estos datos se organizan como conjuntos de elementos por vértice, tal como se muestra en la siguiente ilustración.

![Ilustración de un búfer de vértices que contiene datos de posición, normal y de textura](images/d3d10-vertex-buffer-element.png)

Este búfer de vértice contiene datos por vértice para ocho vértices; cada vértice almacena tres elementos (coordenadas de posición, normal y de textura). La posición y la normal se especifican normalmente con los flotantes de 3 32 bits (formato de DXGI \_ \_ R32G32B32 \_ float) y las coordenadas de textura con los flotantes de 2 32 bits (dxgi \_ format \_ R32G32 \_ float).

Para tener acceso a los datos de un búfer de vértices, debe saber qué vértice tiene acceso y estos otros parámetros de búfer:

-   Offset: el número de bytes desde el inicio del búfer hasta los datos del primer vértice. El desplazamiento se proporciona a [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers).
-   BaseVertexLocation: el número de bytes desde el desplazamiento hasta el primer vértice usado por la llamada a Draw adecuada (vea [métodos de dibujo](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Antes de crear un búfer de vértices, debe definir su diseño mediante la creación [**de un objeto de diseño de entrada**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout). Esto se hace llamando a [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout). Una vez creado el objeto de diseño de entrada, enlácelo a la fase de ensamblador de entrada mediante una llamada a [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Para crear un búfer de vértices, llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

### <a name="index-buffer"></a>Búfer de índice

Un búfer de índice contiene un conjunto secuencial de índices de 16 o 32 bits; cada índice se usa para identificar un vértice en un búfer de vértice. El uso de un búfer de índice con uno o varios búferes de vértices para proporcionar datos a la fase de IA se denomina indexación. Un búfer de índice se puede visualizar como la siguiente ilustración.

![Ilustración de un búfer de índice](images/d3d10-index-buffer.png)

Los índices secuenciales almacenados en un búfer de índice se encuentran con los parámetros siguientes:

-   Offset: el número de bytes desde el inicio del búfer hasta el primer índice. El desplazamiento se proporciona a [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer).
-   StartIndexLocation: el número de bytes desde el desplazamiento hasta el primer vértice usado por la llamada a Draw adecuada (vea [métodos de dibujo](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: número de índices que se van a representar.

Para crear un búfer de índice, llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

Un búfer de índice puede unir varias [franjas de líneas o triángulos](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) separando cada una de ellas con un índice de corte de franja. Un índice de corte de banda permite dibujar varias franjas de líneas o triángulos con una sola llamada a Draw. Un índice de corte de banda es simplemente el valor máximo posible para el índice (0xFFFF para un índice de 16 bits, 0xFFFFFFFF para un índice de 32 bits). El índice de corte de franja restablece el orden de bobinado en los primitivos indizados y se puede usar para quitar la necesidad de triángulos degenerados que, de lo contrario, podría ser necesario para mantener el orden de bobinado adecuado en una franja de triángulo. En la ilustración siguiente se muestra un ejemplo de un índice de corte de banda.

![Ilustración de un índice de corte de franja](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Búfer de constantes

Direct3D 10 presentó un nuevo búfer para proporcionar constantes de sombreador denominado búfer de constantes de sombreador o simplemente un búfer de constantes. Conceptualmente, se parece a un búfer de vértice de un solo elemento, tal como se muestra en la siguiente ilustración.

![Ilustración de un búfer de constantes de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento almacena una constante de componente de 1 a 4, determinada por el formato de los datos almacenados.

Los búferes de constantes reducen el ancho de banda necesario para actualizar las constantes de sombreador al permitir que las constantes de sombreador se agrupen y se confirmen al mismo tiempo, en lugar de realizar llamadas individuales para confirmar cada constante por separado.

Para crear un búfer de constantes del sombreador, llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) y especifique el marcador de enlace de búfer de constantes D3D10 de búfer de constantes de enlace \_ \_ \_ (consulte [**D3D10 \_ enlace \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).

Para enlazar un búfer de constantes de sombreador a la canalización, llame a uno de estos métodos: [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)o [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Tenga en cuenta que cuando se usa la interfaz de [**interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , el proceso de creación, enlace y concesión de un búfer de constantes se controla mediante la instancia de la **interfaz ID3D10Effect** . En ese caso, solo se nescesary para obtener la variable del efecto con uno de los métodos GetVariable como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) y actualizar la variable con uno de los métodos SetVariable como [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Para obtener un ejemplo del uso de la **interfaz ID3D10Effect** para administrar un búfer de constantes, vea el [tutorial 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Un sombreador sigue leyendo variables en un búfer de constantes directamente por nombre de variable de la misma manera que se leen las variables que no forman parte de un búfer de constantes.

Cada fase del sombreador permite hasta 15 búferes de constantes de sombreador; cada búfer puede contener hasta 4096 constantes.

Use un búfer de constantes para almacenar los resultados de la fase de flujo de salida.

Consulte [constantes de sombreador (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) para obtener un ejemplo de cómo declarar un búfer de constantes en un sombreador.

## <a name="texture-resources"></a>Recursos de textura

Un recurso de textura es una colección estructurada de datos diseñada para almacenar textura. A diferencia de los búferes, las texturas se pueden filtrar por muestras de texturas, ya que las unidades de sombreador las leen. El tipo de textura afecta al modo en que se filtra la textura. Un textura representa la unidad más pequeña de una textura que se puede leer o escribir en la canalización. Cada textura contiene de 1 a 4 componentes, organizados en uno de los formatos de DXGI (consulte [**\_ formato de dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Las texturas se crean como un recurso estructurado para que se conozca su tamaño. Sin embargo, cada textura se puede escribir o escribir menos en el momento de la creación de recursos, siempre que el tipo se especifique por completo utilizando una vista cuando la textura esté enlazada a la canalización.

-   [Tipos de textura](#texture-types)
-   [Subrecursos](#subresources)
-   [Strong frente a tipos débiles](#strong-vs-weak-typing)

### <a name="texture-types"></a>Tipos de textura

Hay varios tipos de texturas: 1D, 2D y 3D, cada una de las cuales se puede crear con o sin mapas MIP. Direct3D 10 también admite matrices de texturas y texturas multimuestreadas.

-   [Textura 1D](#1d-texture)
-   [Matriz de textura 1D](#1d-texture-array)
-   [Textura 2D y matriz de textura 2D](#2d-texture-and-2d-texture-array)
-   [Textura 3D](#3d-texture)

### <a name="1d-texture"></a>Textura 1D

Una textura 1D en su forma más simple contiene datos de textura que se pueden direccionar con una sola coordenada de textura. se puede visualizar como una matriz de textura, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura 1D](images/d3d10-1d-texture.png)

Cada textura contiene una serie de componentes de color dependiendo del formato de los datos almacenados. Agregar más complejidad, puede crear una textura 1D con niveles de mipmap, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura 1D con niveles de mipmap](images/d3d10-resource-texture1d.png)

Un nivel de mipmap es una textura que es una potencia de dos menor que el nivel superior. El nivel superior contiene la mayoría de los detalles, cada nivel posterior es más pequeño; en el caso de un mipmap 1D, el nivel más pequeño contiene un textura. Los distintos niveles se identifican mediante un índice denominado LOD (nivel de detalle); puede usar el LOD para tener acceso a una textura más pequeña al representar geometría que no es tan cercana a la cámara.

### <a name="1d-texture-array"></a>Matriz de textura 1D

Direct3D 10 también tiene una nueva estructura de datos para una matriz de texturas. Una matriz de texturas 1D es conceptualmente similar a la siguiente ilustración.

![Ilustración de una matriz de textura 1D](images/d3d10-resource-texture1darray.png)

Esta matriz de texturas contiene tres texturas. Cada una de las tres texturas tiene un ancho de textura de 5 (que es el número de elementos de la primera capa). Cada textura también contiene un mipmap de 3 niveles.

Todas las matrices de texturas en Direct3D son una matriz de texturas homogénea; Esto significa que todas las texturas de una matriz de textura deben tener el mismo formato de datos y el mismo tamaño (incluido el ancho de la textura y el número de niveles de mipmap). Puede crear matrices de texturas de diferentes tamaños, siempre que todas las texturas de cada matriz coincidan en tamaño.

### <a name="2d-texture-and-2d-texture-array"></a>Textura 2D y matriz de textura 2D

Un recurso Texture2D contiene una cuadrícula 2D de textura. Cada textura es direccionable por un vector u, v. Dado que se trata de un recurso de textura, puede contener niveles de mipmap y Subrecursos. Un recurso de textura 2D totalmente rellenado tiene un aspecto similar al de la siguiente ilustración.

![Ilustración de un recurso de textura 2D](images/d3d10-resource-texture2d.png)

Este recurso de textura contiene una sola textura 3x5 con tres niveles de mipmap.

Un recurso Texture2DArray es una matriz homogénea de texturas 2D; es decir, cada textura tiene el mismo formato de datos y dimensiones (incluidos los niveles de mipmap). Tiene un diseño similar al de la matriz de texturas 1D, salvo que las texturas contienen ahora datos 2D y, por tanto, tienen un aspecto similar al de la siguiente ilustración.

![Ilustración de una matriz de recursos de textura 2D](images/d3d10-resource-texture2darray.png)

Esta matriz de texturas contiene tres texturas; cada textura se 3x5 con dos niveles de mipmap.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Usar un Texture2DArray como un cubo de textura

Un cubo de textura es una matriz de textura 2D que contiene 6 texturas, una para cada una de las caras del cubo. Un cubo de textura totalmente rellenado tiene un aspecto similar al de la siguiente ilustración.

![Ilustración de una matriz de recursos de textura 2D que representan un cubo de textura](images/d3d10-resource-texturecube.png)

Una matriz de textura 2D que contiene 6 texturas se puede leer desde los sombreadores con las funciones intrínsecas de mapa de cubo, una vez enlazadas a la canalización con una vista de textura de cubo. Los cubos de textura se dirigen desde el sombreador con un vector 3D que señala hacia fuera del centro del cubo de textura.

### <a name="3d-texture"></a>Textura 3D

Un recurso Texture3D (también conocido como textura de volumen) contiene un volumen 3D de textura. Dado que se trata de un recurso de textura, puede contener niveles de mipmap. Una [**textura 3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) totalmente rellenada es similar a la siguiente ilustración.

![Ilustración de un recurso de textura 3D](images/d3d10-resource-texture3d.png)

Cuando un segmento MIP de textura 3D se enlaza como salida de destino de representación (con una vista de destino de representación), la textura 3D se comporta de forma idéntica a una matriz de textura 2D con n segmentos. El segmento de representación determinado se elige en la fase de sombreador de geometría, declarando un componente escalar de los datos de salida como el \_ valor del sistema VP RenderTargetArrayIndex.

No hay ningún concepto de una matriz de textura 3D; por lo tanto, un subrecurso de textura 3D es un solo nivel de mipmap.

### <a name="subresources"></a>Subrecursos

La API de Direct3D 10 hace referencia a los recursos o subconjuntos de recursos completos. Para especificar parte de los recursos, Direct3D ha acuñó el término Subrecursos, lo que significa que es un subconjunto de un recurso.

Un búfer se define como un subrecurso único. Las texturas son un poco más complicadas, ya que existen distintos tipos de textura (1D, 2D, etc.), algunos de los cuales admiten niveles de mipmap o matrices de texturas. A partir del caso más simple, una textura 1D se define como un subrecurso único, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura 1D](images/d3d10-1d-texture.png)

Esto significa que la matriz de textura que componen una textura 1D está contenida en un solo subrecurso.

Si expande una textura 1D con tres niveles de mipmap, se puede visualizar como esto.

![Ilustración de una textura 1D con niveles de mipmap](images/d3d10-resource-texture1d.png)

Piense en esto como una textura única que se compone de tres subtexturas. Cada subtextura se cuenta como un subrecurso, por lo que esta textura 1D contiene 3 Subrecursos. Una subtextura (o subrecurso) se puede indizar mediante el nivel de detalle (LOD) para una sola textura. Cuando se usa una matriz de texturas, el acceso a una subtextura determinada requiere el LOD y la textura determinada. Como alternativa, la API combina estos dos fragmentos de información en un único índice de subrecurso basado en cero, tal como se muestra aquí.

![Ilustración de un índice de subrecurso basado en cero](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Selección de Subrecursos

Algunas API tienen acceso a un recurso completo (por ejemplo, [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)), mientras que otras acceden a una parte de un recurso (por ejemplo, [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) o [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)). Las API que tienen acceso a una parte de un recurso suelen usar una descripción de la vista (como [**D3D10 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)) para especificar los Subrecursos a los que se va a tener acceso.

Estas figuras muestran los términos utilizados por una descripción de la vista al obtener acceso a una matriz de texturas.

### <a name="array-slice"></a>Segmento de matriz

Dada una matriz de texturas, cada textura con los mapas MIP, un segmento de matriz (representado por el rectángulo blanco) incluye una textura y todas sus subtexturas, tal y como se muestra en la siguiente ilustración.

![Ilustración de una inserción de matriz](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Segmento MIP

Un segmento de MIP (representado por el rectángulo blanco) incluye un nivel de mipmap para cada textura de una matriz, como se muestra en la siguiente ilustración.

![Ilustración de una inserción de MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selección de un único subrecurso

Puede usar estos dos tipos de segmentos para elegir un solo subrecurso, tal como se muestra en la siguiente ilustración.

![Ilustración de la elección de un subrecurso mediante el uso de un segmento de matriz y un empalme de MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Seleccionar varios Subrecursos

También puede usar estos dos tipos de segmentos con el número de niveles de mipmap y/o el número de texturas para elegir varios Subrecursos.

![Ilustración de la elección de varios Subrecursos](images/d3d10-resource-subresources-2.png)

Independientemente del tipo de textura que esté utilizando, con o sin los mapas MIP, con o sin una matriz de textura, puede usar la función auxiliar [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)para calcular el índice de un subrecurso determinado.

### <a name="strong-vs-weak-typing"></a>Strong frente a tipos débiles

Al crear un recurso totalmente tipado, se restringe el recurso al formato con el que se creó. Esto permite al motor en tiempo de ejecución optimizar el acceso, especialmente si el recurso se crea con marcas que indican que la aplicación no puede [asignarlo](d3d10-graphics-programming-guide-resources-mapping.md) . Los recursos creados con un tipo específico no se pueden reinterpretar mediante el mecanismo de vista.

En un recurso de tipo menos, se desconoce el tipo de datos cuando el recurso se crea por primera vez. La aplicación debe elegir entre los formatos de tipo disponibles menos ( [**consulte \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Debe especificar el tamaño de la memoria que se va a asignar y si el tiempo de ejecución necesitará generar las subtexturas en un mipmap. Sin embargo, el formato de datos exacto (si la memoria se interpreta como enteros, valores de punto flotante, enteros sin signo, etc.) no se determina hasta que el recurso se enlaza a la canalización con una vista. Dado que el formato de textura sigue siendo flexible hasta que la textura se enlaza a la canalización, el recurso se denomina almacenamiento débilmente tipado. El almacenamiento débilmente tipado tiene la ventaja de que se puede reutilizar o reinterpretar (en otro formato) siempre que el bit del componente del nuevo formato coincida con el recuento de bits del formato anterior.

Un solo recurso se puede enlazar a varias fases de canalización, siempre y cuando cada una tenga una vista única, que califique por completo los formatos en cada ubicación. Por ejemplo, un recurso creado con el formato DXGI \_ format \_ R32G32B32A32 \_ no puede usarse como un formato de \_ dxgi \_ R32G32B32A32 \_ float y un \_ formato \_ de dxgi R32G32B32A32 \_ uint en diferentes ubicaciones de la canalización simultáneamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
