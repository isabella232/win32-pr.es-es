---
description: Obtenga información sobre la compatibilidad con mallas en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Compatibilidad con malla en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1600b372432d59357a7431c70ce70ce2958002c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408138"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Compatibilidad con malla en D3DX (Direct3D 9)

D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.

## <a name="meshes"></a>Mallas

D3DX implementa la construcción de malla para cargar, manipular y representar el contenido del archivo .x. Una malla es básicamente una colección de vértices que definen parte de la geometría y un conjunto de índices que definen las caras. Hay varios tipos de malla.

[**ID3DXBaseMesh proporciona**](id3dxbasemesh.md) los aspectos básicos. [**ID3DXMesh**](id3dxmesh.md) hereda de ID3DXBaseMesh y agrega optimización de malla mediante la caché de vértices por chip. [**ID3DXSkinInfo proporciona**](id3dxskininfo.md) compatibilidad con malla de máscara.

[**ID3DXBaseMesh proporciona métodos**](id3dxbasemesh.md) para manipular y consultar objetos de malla [**ID3DXMesh,**](id3dxmesh.md) que heredan de la malla base. Esto incluye operaciones de adyacencia, recuperación del búfer de geometría, operaciones de bloqueo y desbloqueo (vértice e índice) y copia, representación, cara y información de vértices.

> [!Note]  
> Se han eliminado las interfaces ID3DXPMesh e ID3DXSPMesh (para admitir mallas progresivas y simplificadas, respectivamente) disponibles en versiones anteriores de Direct3D 9.

 

## <a name="mesh-architecture"></a>Arquitectura de malla

Una malla contiene los datos de un modelo complejo. Es un contenedor de datos abstracto que contiene recursos como texturas y materiales, y atributos como datos de posición y datos de adyacencia. Hay varias operaciones de malla que mejoran el rendimiento del dibujo y la apariencia de una superficie. Además, hay una serie de otros conceptos de malla que afecta a la funcionalidad de las operaciones de malla. Comprender estos conceptos de malla para que pueda aplicarlos mejorará el rendimiento de la malla.

## <a name="mesh-object-data"></a>Datos de objeto de malla

Una malla contiene un búfer de vértices, un búfer de índice y un búfer de atributos.

-   El búfer de vértices contiene los datos del vértice, que son los vértices de malla.
-   El búfer de índice contiene índices de vértices para acceder al búfer de vértices. Esto puede reducir el tamaño del búfer de vértices reduciendo los vértices duplicados. Solo una malla indexada usa el búfer de índice. Si una malla se forma de una lista de triángulos, por ejemplo, no usa el búfer de índice.
-   El búfer de atributos contiene datos de atributo. Los atributos son propiedades de los vértices de malla, sin ningún orden determinado. Una malla D3DX almacena atributos en un grupo de DWORDS, para cada cara.

### <a name="attribute-tables"></a>Tablas de atributos

Una tabla de atributos es una representación concisa del contenido de un búfer de atributos. Las tablas de atributos se pueden crear llamando a uno de los métodos Optimize con D3DXMESHOPT ATTRSORT, bloqueando el búfer de atributos y llen guardarlo con datos, o llamando a \_ SetAttributeTable. Una malla contiene una tabla de atributos cuando la malla se reordena en grupos. Esto sucede cuando se llama a Optimize, suponiendo que se proporciona una opción de ordenación de atributos (D3DXMESHOPT \_ ATTRSORT o superior). Las mallas D3DX usan listas de triángulos indexadas y, por tanto, se dibujan con [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Las tablas de atributos se crean como resultado de llamar a Optimize. Las caras no tienen que ser adyacentes, porque Optimizar las reordenará para que sean adyacentes. Por ejemplo, las manos de una malla humana podrían usar el mismo atributo. El identificador ayuda a ordenar las caras en grupos. Las mallas de los archivos .x han generado automáticamente atributos para las propiedades de material y textura. Debe llamar a Optimize(ATTRSORT) o a optimize(VERTEXCACHE) más eficaz para obtener un buen rendimiento. Las funciones de carga intentan presentar los datos en el formato exacto en el que se guardaron. Si usa una malla basada en búfer de vértices o búfer de índice, la API de malla proporciona funciones de optimización y transformaciones de despejado con poca sobrecarga.

Los tipos de optimización son acumulativos, empezando por el menos óptimo (D3DXMESHOPT COMPACT) hasta el más óptimo \_ (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER realiza una compactación y una ordenación de atributos. D3DXMESHOPT \_ VERTEXCACHE siempre se recomienda, incluso en dispositivos sin una caché de vértices verdadera.

## <a name="application-data"></a>Datos de aplicaciones

Los datos de aplicación son datos de malla administrados por una aplicación. Hay un acoplamiento estricto entre los datos del vértice de malla y los datos administrados por estos búferes.

El búfer de materiales contiene n materiales. La función Load devuelve los materiales cuando se carga el archivo .x. Cada subconjunto puede tener sus propios materiales y texturas. El búfer de materiales es estático.

El búfer de adyacencia contiene información sobre los bordes, las caras y las caras adyacentes. Algunas operaciones de malla dependen de saber qué caras son adyacentes entre sí. Esta información, denominada datos de adyacencia, se mantiene en un búfer de adyacencia. No forma parte de la malla, pero la aplicación la mantiene y debe proporcionarse a los métodos de malla cuando sea necesario.

El búfer de instancia de efectos contiene una lista de instancias de efecto. Una instancia de efecto almacena el estado. Esta información de estado se usa para inicializar la canalización. Una instancia de efecto contiene pares nombre-valor en un efecto.

## <a name="advanced-mesh-topics"></a>Temas de Malla avanzada

Las mallas optimizadas se basan en la funcionalidad de malla base y agregan funcionalidad de optimización de caché de vértices con dos métodos: Optimize, que crea una nueva malla, y OptimizeInPlace, que modifica la malla original.

D3DXGeneratePMesh usa el algoritmo de simplificación D3DX para generar una malla progresiva a partir de la malla de entrada. D3DXSimplifyMesh genera una malla estándar del nivel de detalle especificado a partir de una malla de entrada mediante el mismo algoritmo de simplificación. El usuario tiene control sobre la métrica de error utilizada a través de los pesos especificados por componente de vértice y pesos especificados por vértice. Los pesos por componente se multiplican con respecto a la parte de componentes de error calculada por contracción del borde. Los pesos por vértice se multiplican con respecto al valor de métrica de error determinado para la eliminación de ese vértice. Por ejemplo, si nunca desea que se quite un vértice, establezca el peso de ese vértice específico en un valor grande. Por el contrario, si desea quitarlo anteriormente, esta establezca en un valor pequeño (menor que 1).

[**ID3DXSkinInfo admite**](id3dxskininfo.md) caracteres con máscara. Un carácter de máscara se define mediante un conjunto de mallas y un conjunto de pórticos que afectan a los vértices de las mallas. Los esqueletos se representan como una jerarquía de transformación. Para cada malla, hay una matriz para cada pórnica que le afecta, que transforma la malla en el espacio de coordenadas local del póreo. Esta matriz es la transformación del espacio de los tejidos de la malla. Esto se define en el momento en que el esqueleto está asociado a la malla en el proceso de creación.

### <a name="skinning"></a>Pelar

Esquiar es una técnica para transformar vértices de malla mediante ramas. Normalmente, los esqueletos se organizan en un esqueleto jerárquico, de forma muy parecido a los esqueletos de un cuerpo humano. A continuación, los vértices de objeto se asocian a los pórticos, como la asociación de la máscara al esqueleto. Cuando los ojos se transforman, la máscara también se transforma.

Las mallas de máscara usan los esqueletos para influir en una serie de vértices. El usuario proporciona los datos de transformación de los tejidos para influir en cómo aplicar SRT al tejido. La malla usa los tejidos transformados para influir en los vértices asociados con los tejidos. Las paletas son matrices de transformaciones SRT. A menudo, las paletas se implementan como matrices, pero pueden contener valores SRT.

### <a name="progressive-mesh-trimming"></a>Recorte de malla progresiva

Las áreas con pocos detalles pueden permitirse perder vértices que no cambian el aspecto representado de la superficie. Esto es especialmente cierto para los objetos a medida que se mueven más lejos de la cámara. Esto se conoce como nivel de detalle. Los usuarios tienen controles de representación de nivel de API para establecer el nivel de detalle para maximizar la eficacia de la representación.

Los objetos de malla progresiva comienzan con un gran número de caras y usan la simplificación para reducir el número de caras. Una malla progresiva que es independiente de la vista se conoce como malla progresiva independiente de la vista (VIPM).

Otra manera de reducir el número de caras es recortando. Esto realmente quita los vértices y las caras de la malla. El recorte se puede realizar en el extremo superior (para limitar el número máximo de caras) o en el extremo inferior (para limitar el número mínimo de caras). El recorte mejora el rendimiento del dibujo; sin embargo, se debe usar la atención para conservar la calidad visual. El recorte se muestra en el ejemplo del SDK de Malla progresiva.

En el caso de las áreas de alta visibilidad, la resolución se puede aumentar mediante el nivel de detalle progresiva (PXD). Se trata de una técnica para dividir una sola cara en dos caras.

### <a name="patch-meshes"></a>Mallas de revisión

También se admiten dos tipos especializados de mallas de revisión: revisiones de rectángulo y triángulo. La malla de revisión del rectángulo es una malla de revisión cuyos puntos de control se menten en una secuencia rectangular sinuoso. Las revisiones de rectángulo y triángulo se usan para crear superficies de orden alto. No se usan con frecuencia como mallas de triángulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
