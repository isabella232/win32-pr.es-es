---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Compatibilidad de malla en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0b2b1dd0e5d4c5a212005afe400bb559f1689a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997636"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Compatibilidad de malla en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="meshes"></a>Mallas

D3DX implementa la construcción de malla para cargar, manipular y representar el contenido del archivo. x. Una malla es básicamente una colección de vértices que definen alguna geometría y un conjunto de índices que definen las caras. Hay varios tipos de malla.

[**ID3DXBaseMesh**](id3dxbasemesh.md) proporciona los aspectos básicos. [**ID3DXMesh**](id3dxmesh.md) hereda de ID3DXBaseMesh y agrega optimización de malla mediante la caché de vértices por chip. [**ID3DXSkinInfo**](id3dxskininfo.md) proporciona compatibilidad con la malla con máscaras.

[**ID3DXBaseMesh**](id3dxbasemesh.md) proporciona métodos para manipular y consultar objetos de malla [**ID3DXMesh**](id3dxmesh.md) , que heredan de la malla base. Esto incluye las operaciones de adyacencia, la recuperación del búfer de geometría, las operaciones de bloqueo/desbloqueo (vértice e índice) y la información de copia, representación, superficie y vértice.

> [!Note]  
> Las interfaces ID3DXPMesh y ID3DXSPMesh (para admitir mallas progresivas y simplificadas, respectivamente) disponibles en versiones anteriores de Direct3D 9 se han quitado.

 

## <a name="mesh-architecture"></a>Arquitectura de malla

Una malla contiene los datos para un modelo complejo. Es un contenedor de datos abstracto que contiene recursos como texturas y materiales, y atributos como datos de posición y datos de adyacencia. Hay varias operaciones de malla que mejoran el rendimiento del dibujo y la apariencia de una superficie. Además, hay otros conceptos de malla que afectarán a la funcionalidad de las operaciones de malla. Comprender estos conceptos de malla para que pueda aplicarlos mejorará el rendimiento de la malla.

## <a name="mesh-object-data"></a>Datos del objeto Mesh

Una malla contiene un búfer de vértices, un búfer de índice y un búfer de atributo.

-   El búfer de vértice contiene los datos de vértice, que son los vértices de la malla.
-   El búfer de índice contiene índices de vértices para tener acceso al búfer de vértices. Esto puede reducir el tamaño del búfer de vértices reduciendo los vértices duplicados. Solo una malla indizada usa el búfer de índice. Si una malla se compone de una lista de triángulos, por ejemplo, no utiliza el búfer de índice.
-   El búfer de atributo contiene datos de atributos. Los atributos son propiedades de los vértices de la malla, en ningún orden determinado. Una malla de D3DX almacena los atributos de un grupo de DWORDs para cada tipo.

### <a name="attribute-tables"></a>Tablas de atributos

Una tabla de atributos es una representación concisa del contenido de un búfer de atributo. Las tablas de atributos se pueden crear mediante una llamada a uno de los métodos Optimize con D3DXMESHOPT \_ ATTRSORT, bloqueando el búfer de atributo y rellenándolo con datos, o llamando a SetAttributeTable. Una malla contiene una tabla de atributos cuando la malla se reordena en grupos. Esto sucede cuando se llama a optimize, suponiendo que se proporcione una opción de ordenación de atributos (D3DXMESHOPT \_ ATTRSORT o superior). Las mallas de D3DX usan listas de triángulos indizadas y, por lo tanto, se dibujan con [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Las tablas de atributos se crean como resultado de llamar a Optimize. No es necesario que las caras sean adyacentes, ya que optimizar las reordenará para ser adyacentes. Por ejemplo, las manos de una malla humana podrían usar el mismo atributo. El identificador ayuda a ordenar los rostros en grupos. Las mallas de los archivos. x tienen atributos generados automáticamente para las propiedades de material y de textura. Necesita llamar a Optimize (ATTRSORT) o a Optimize (VERTEXCACHE) más eficaz para obtener un buen rendimiento. Las funciones de carga intentan presentar los datos en el formato exacto en el que se guardaron. Si usa una malla basada en búfer de índice o búfer de vértices, la API de malla proporciona funciones de optimización y transformación de máscaras con poca sobrecarga.

Los tipos de optimización son acumulativos, empezando por el menos óptimo (D3DXMESHOPT \_ Compact) hasta el óptimo (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER realiza una ordenación de atributos y compactación. \_Siempre se recomienda D3DXMESHOPT VERTEXCACHE, incluso en dispositivos sin una memoria caché de vértices verdadera.

## <a name="application-data"></a>Datos de aplicaciones

Los datos de aplicación son datos de malla administrados por una aplicación. Hay un acoplamiento estrecho entre los datos de vértice de la malla y los datos administrados por estos búferes.

El búfer de materiales contiene n materiales. La función Load devuelve los materiales cuando se carga el archivo. x. Cada subconjunto puede tener sus propios materiales y texturas. El búfer de materiales es estático.

El búfer de adyacencia contiene información sobre los bordes, caras y caras adyacentes. Algunas operaciones de malla dependen de saber qué caras son adyacentes entre sí. Esta información, denominada datos de adyacencia, se mantiene en un búfer de adyacencia. No forma parte de la malla pero la aplicación la mantiene y debe proporcionarse a los métodos de malla cuando sea necesario.

El búfer de instancia de efectos contiene una lista de instancias de efecto. Una instancia de efecto almacena el estado. Esta información de estado se usa para inicializar la canalización. Una instancia de efecto contiene pares de nombre y valor en un efecto.

## <a name="advanced-mesh-topics"></a>Temas avanzados sobre la malla

Las mallas optimizadas se basan en la funcionalidad de la malla base y agregan la capacidad de optimización de la memoria caché de vértices con dos métodos: optimize, que crea una nueva malla y OptimizeInPlace, que modifica la malla original.

D3DXGeneratePMesh usa el algoritmo de simplificación de D3DX para generar una malla progresiva desde la malla de entrada. D3DXSimplifyMesh genera una malla estándar del nivel de detalle dado de una malla de entrada mediante el mismo algoritmo de simplificación. El usuario tiene control sobre la métrica de error utilizada a través de los pesos especificados por componente y pesos especificados por vértice. Los pesos por componente se multiplican con respecto a la parte de los componentes de error calculada por contracción perimetral. Los pesos por vértice se multiplican por el valor de métrica de error determinado para la eliminación de ese vértice. Por ejemplo, si nunca desea quitar un vértice, establezca el peso de ese vértice específico en un valor grande. Por el contrario, si desea que se quite anteriormente, establézcalo en un valor pequeño (menor que 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) admite caracteres de máscaras. Un carácter de aspecto se define mediante un conjunto de mallas y un conjunto de huesos que afectan a los vértices de las mallas. Los huesos se representan como una jerarquía de transformación. Para cada malla, hay una matriz por cada hueso que lo afecta, que transforma la malla en el espacio de coordenadas local del hueso. Esta matriz es la transformación de espacio de hueso del hueso de la malla. Esto se define en el momento en que el esqueleto está asociado a la malla en el proceso de creación.

### <a name="skinning"></a>Máscaras

El uso de aspectos es una técnica para transformar los vértices de malla mediante huesos. Los huesos suelen organizarse en un esqueleto jerárquico, de forma muy similar a los huesos de un cuerpo humano. Los vértices de objeto se asocian a los huesos, como adjuntar la piel a los huesos. Cuando se transforman los huesos, también se transforma la máscara.

Las mallas estratificadas usan los huesos para influir en un número de vértices. Los datos de la transformación del hueso son proporcionados por el usuario, para influir en la manera en que se preparan los huesos. La malla utiliza los huesos transformados para influir en los vértices asociados con los huesos. Las paletas son matrices de transformaciones de SRT. Las paletas se suelen implementar como matrices, pero pueden contener valores de SRT.

### <a name="progressive-mesh-trimming"></a>Recorte de malla progresiva

Las áreas de menor detalle pueden permitirse perder vértices que no cambian la apariencia representada de la superficie. Esto es especialmente cierto en los objetos a medida que se alejan de la cámara. Esto se conoce como nivel de detalle. Los usuarios tienen controles de representación de nivel de API para establecer el nivel de detalle para maximizar la eficacia de la representación.

Los objetos de malla progresiva comienzan con un gran número de caras y usan la simplificación para reducir el número de caras. Una malla progresiva que sea vista independiente se conoce como malla progresiva independiente de la vista (VIPM).

Otra forma de reducir el número de caras es mediante un recorte. En realidad, se quitan los vértices y caras de la malla. El recorte se puede realizar en el extremo superior (para limitar el número máximo de caras) o en el extremo inferior (para limitar el número mínimo de caras). El recorte mejora el rendimiento del dibujo, sin embargo, debe usarse para conservar la calidad visual. El recorte se muestra en el ejemplo de SDK de malla progresiva.

En el caso de las áreas de alta visibilidad, la resolución se puede aumentar con el nivel de detalle progresiva (PLOD). Se trata de una técnica para dividir una sola cara en dos caras.

### <a name="patch-meshes"></a>Mallas de revisión

También se admiten dos tipos especializados de mallas de revisión: revisiones de rectángulos y triángulos. La malla de la revisión del rectángulo es una malla de parches cuyos puntos de control se colocan en una secuencia de bobinado y rectangular. Las revisiones de rectángulos y triángulos se usan para crear superficies de orden superior. No se usan normalmente como mallas de triángulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
