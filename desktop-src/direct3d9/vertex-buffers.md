---
description: Los búferes de vértices, representados por la interfaz IDirect3DVertexBuffer9, son búferes de memoria que contienen datos de vértices.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Búferes de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805732"
---
# <a name="vertex-buffers-direct3d-9"></a>Búferes de vértices (Direct3D 9)

Los búferes de vértices, representados por la interfaz [**IDirect3DVertexBuffer9**](/windows/desktop/api) , son búferes de memoria que contienen datos de vértices. Los búferes de vértices pueden contener cualquier tipo de vértice, transformado o sin transformar, LIT o sin iluminación, que se puede representar mediante el uso de los métodos de representación en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Puede procesar los vértices en un búfer de vértice para realizar operaciones como la transformación, la iluminación o la generación de marcas de recorte. Siempre se realiza la transformación.

La flexibilidad de los búferes de vértices los convierte en puntos de ensayo ideales para reutilizar geometría transformada. Puede crear un solo búfer de vértices, transformar, aclarar y recortar los vértices en él, y representar el modelo en la escena tantas veces como sea necesario sin volver a transformarlo, incluso con los cambios de estado de representación intercalados. Esto resulta útil al representar modelos que usan varias texturas: la geometría se transforma solo una vez y, a continuación, se pueden representar partes de ella según sea necesario, intercaladas con los cambios de textura necesarios. Los cambios de estado de representación realizados después de que se procesen los vértices surten efecto la próxima vez que se procesan los vértices.

-   [Descripción](#description)
-   [Bloque de memoria y uso](#memory-pool-and-usage)

## <a name="description"></a>Descripción

Un búfer de vértices se describe en términos de sus capacidades: si solo existe en la memoria del sistema, si solo se usa para operaciones de escritura, y el tipo y el número de vértices que puede contener. Todos estos rasgos se encuentran en una estructura [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) .

El miembro de formato se establece en D3DFMT \_ VERTEXDATA para indicar que se trata de un búfer de vértices. El tipo identifica el tipo de recurso del búfer de vértices. El miembro de la estructura Usage contiene marcas de capacidad generales. La \_ marca D3DUSAGE SOFTWAREPROCESSING indica que el búfer de vértices se va a usar con el procesamiento de vértices de software. La presencia de la \_ marca WRITEONLY de D3DUSAGE en uso indica que la memoria del búfer de vértices solo se usa para las operaciones de escritura. Esto libera el controlador para colocar los datos de vértice en la mejor ubicación de memoria para habilitar el procesamiento y la representación rápidos. Si \_ no se usa la marca WRITEONLY de D3DUSAGE, es menos probable que el controlador Coloque los datos en una ubicación que sea ineficaz para las operaciones de lectura. Esto sacrifica la velocidad de procesamiento y representación. Si no se especifica esta marca, se supone que las aplicaciones realizan operaciones de lectura y escritura en los datos dentro del búfer de vértices.

Grupo especifica la clase de memoria que se asigna para el búfer de vértices. La \_ marca D3DPOOL SYSTEMMEM indica que el sistema creó el búfer de vértices en la memoria del sistema.

El miembro size almacena el tamaño, en bytes, de los datos del búfer de vértices. El miembro FVF contiene una combinación de [D3DFVF](d3dfvf.md) que identifican el tipo de vértices que contiene el búfer.

## <a name="memory-pool-and-usage"></a>Bloque de memoria y uso

Puede crear búferes de vértices con el método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) , que toma el grupo (clase de memoria) y los parámetros de uso. **IDirect3DDevice9:: CreateVertexBuffer** también se puede crear con un código FVF especificado para su uso en el procesamiento de vértices de función fija o como salida de los vértices de proceso. Para obtener más información, vea [búferes de vértices de FVF (Direct3D 9)](fvf-vertex-buffers.md).

La \_ marca D3DUSAGE SOFTWAREPROCESSING se puede establecer cuando el procesamiento de vértices de modo mixto o software (D3DCREATE \_ mixto \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) está habilitado para ese dispositivo. D3DUSAGE \_ SOFTWAREPROCESSING se debe establecer para que los búferes se usen con el procesamiento de vértices de software en modo mixto, pero no se debe establecer para el mejor rendimiento posible al usar el procesamiento de vértices de hardware en modo mixto. ( D3DCREATE \_ hardware \_ VERTEXPROCESSING). Sin embargo, el establecimiento de D3DUSAGE \_ SOFTWAREPROCESSING es la única opción cuando se va a usar un solo búfer con el procesamiento de vértices de hardware y software. D3DUSAGE \_ SOFTWAREPROCESSING se permite para dispositivos mixtos y de software.

Es posible forzar búferes de vértices y de índices en la memoria del sistema mediante \_ la especificación de D3DPOOL SYSTEMMEM, incluso cuando el procesamiento de vértices se realiza en el hardware. Se trata de una manera de evitar grandes cantidades excesivas de memoria bloqueada en páginas cuando un controlador coloca estos búferes en la memoria AGP.

En esta sección se presentan los conceptos necesarios para entender y usar búferes de vértices en una aplicación Direct3D. La información se divide en las secciones siguientes.

-   [Crear un búfer de vértices (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Acceder al contenido de un búfer de vértices (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Representar desde un búfer de vértice (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Búferes de vértices de FVF (Direct3D 9)](fvf-vertex-buffers.md)
-   [Procesamiento de vértices de funciones fijas (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Procesamiento de vértices programable (Direct3D 9)](programmable-vertex-processing.md)
-   [Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> <dt>

[Representación de búferes de vértices y de índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Búferes de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
