---
description: Los búferes de vértices, representados por la interfaz IDirect3DVertexBuffer9, son búferes de memoria que contienen datos de vértices.
ms.assetid: vs|directx_sdk|~\vertex_buffers.htm
title: Búferes de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e38feb34e7b9f637f383bf451bff812d9ee6fb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580116"
---
# <a name="vertex-buffers-direct3d-9"></a>Búferes de vértices (Direct3D 9)

Los búferes de vértices, representados por la [**interfaz IDirect3DVertexBuffer9,**](/windows/desktop/api) son búferes de memoria que contienen datos de vértices. Los búferes de vértices pueden contener cualquier tipo de vértice (transformado o sin transformar, encendido o sin encender) que se pueda representar mediante el uso de los métodos de representación en la interfaz [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Puede procesar los vértices en un búfer de vértices para realizar operaciones como la transformación, la iluminación o la generación de marcas de recorte. La transformación siempre se realiza.

La flexibilidad de los búferes de vértices los convierte en puntos de almacenamiento provisional ideales para volver ausar la geometría transformada. Puede crear un búfer de vértice único, transformar, encender y recortar los vértices en él, y representar el modelo en la escena tantas veces como sea necesario sin volver a transformarlo, incluso con cambios de estado de representación intercalados. Esto resulta útil cuando se representan modelos que usan varias texturas: la geometría se transforma solo una vez y, a continuación, se pueden representar partes de ella según sea necesario, intercaladas con los cambios de textura necesarios. Los cambios de estado de representación realizados después de procesar los vértices se hacen efectivos la próxima vez que se procese los vértices.

-   [Descripción](#description)
-   [Uso y grupo de memoria](#memory-pool-and-usage)

## <a name="description"></a>Descripción

Un búfer de vértices se describe en términos de sus funcionalidades: si solo puede existir en la memoria del sistema, si solo se usa para operaciones de escritura, y el tipo y el número de vértices que puede contener. Todos estos rasgos se mantienen en una [**estructura \_ DESC D3DVERTEXBUFFER.**](d3dvertexbuffer-desc.md)

El miembro Format se establece en D3DFMT \_ VERTEXDATA para indicar que se trata de un búfer de vértices. El tipo identifica el tipo de recurso del búfer de vértices. El miembro usage structure contiene marcas de funcionalidad general. La marca D3DUSAGE SOFTWAREPROCESSING indica que el búfer de vértices se va a usar con el procesamiento de \_ vértices de software. La presencia de la marca WRITEONLY de D3DUSAGE en Uso indica que la memoria del búfer de vértices solo se usa \_ para las operaciones de escritura. Esto libera al controlador para colocar los datos del vértice en la mejor ubicación de memoria para permitir un procesamiento y una representación rápidos. Si no se usa la marca WRITEONLY de D3DUSAGE, es menos probable que el controlador coloque los datos en una ubicación ineficaz para las operaciones \_ de lectura. Esto sacrifique algo de velocidad de procesamiento y representación. Si no se especifica esta marca, se supone que las aplicaciones realizan operaciones de lectura y escritura en los datos dentro del búfer de vértices.

Pool especifica la clase de memoria que se asigna para el búfer de vértices. La marca SYSTEMMEM de D3DPOOL indica que el sistema creó el \_ búfer de vértices en la memoria del sistema.

El miembro Size almacena el tamaño, en bytes, de los datos del búfer de vértices. El miembro FVF contiene una combinación de [D3DFVF](d3dfvf.md) que identifica el tipo de vértices que contiene el búfer.

## <a name="memory-pool-and-usage"></a>Uso y grupo de memoria

Puede crear búferes de vértices con el método [**IDirect3DDevice9::CreateVertexBuffer,**](/windows/desktop/api) que toma parámetros de grupo (clase de memoria) y de uso. **IDirect3DDevice9::CreateVertexBuffer** también se puede crear con un código FVF especificado para su uso en el procesamiento de vértices de función fija o como salida de vértices de proceso. Para obtener más información, [vea FVF Vertex Buffers (Direct3D 9) (Búferes de vértices FVF [Direct3D 9]).](fvf-vertex-buffers.md)

La marca D3DUSAGE SOFTWAREPROCESSING se puede establecer cuando el procesamiento de vértices de software o de modo mixto \_ (D3DCREATE \_ MIXED \_ VERTEXPROCESSING/D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING) está habilitado para ese dispositivo. D3DUSAGE SOFTWAREPROCESSING debe establecerse para que los búferes se usen con el procesamiento de vértices de software en modo mixto, pero no se debe establecer para obtener el mejor rendimiento posible al usar el procesamiento de vértices de hardware en modo \_ mixto.( D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING). Sin embargo, establecer D3DUSAGE SOFTWAREPROCESSING es la única opción cuando se va a usar un solo búfer con el procesamiento de vértices \_ de hardware y software. D3DUSAGE SOFTWAREPROCESSING se permite para dispositivos de software y \_ mixtos.

Es posible forzar los búferes de vértices e índices en la memoria del sistema especificando D3DPOOL SYSTEMMEM, incluso cuando el procesamiento de vértices se realiza \_ en hardware. Se trata de una manera de evitar grandes cantidades de memoria bloqueada por páginas cuando un controlador coloca estos búferes en la memoria de AGP.

En esta sección se presentan los conceptos necesarios para comprender y usar búferes de vértices en una aplicación direct3D. La información se divide en las secciones siguientes.

-   [Crear un búfer de vértices (Direct3D 9)](creating-a-vertex-buffer.md)
-   [Acceso al contenido de un búfer de vértices (Direct3D 9)](accessing-the-contents-of-a-vertex-buffer.md)
-   [Representación desde un búfer de vértices (Direct3D 9)](rendering-from-a-vertex-buffer.md)
-   [Búferes de vértices FVF (Direct3D 9)](fvf-vertex-buffers.md)
-   [Procesamiento de vértices de función fija (Direct3D 9)](fixed-function-vertex-processing.md)
-   [Procesamiento de vértices programables (Direct3D 9)](programmable-vertex-processing.md)
-   [Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)](device-types-and-vertex-processing-requirements.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> <dt>

[Representación a partir de búferes de vértice e índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Búferes de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
