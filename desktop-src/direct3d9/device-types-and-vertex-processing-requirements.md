---
description: El rendimiento de las operaciones de procesamiento de vértices, incluida la transformación y la iluminación, depende en gran medida de dónde existe el búfer de vértices en la memoria y qué tipo de dispositivo de representación se está usando.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537234"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)

El rendimiento de las operaciones de procesamiento de vértices, incluida la transformación y la iluminación, depende en gran medida de dónde existe el búfer de vértices en la memoria y qué tipo de dispositivo de representación se está usando. Las aplicaciones controlan la asignación de memoria para los búferes de vértices cuando se crean. Cuando \_ se establece la marca de memoria D3DPOOL SYSTEMMEM, el búfer de vértices se crea en la memoria del sistema. Cuando \_ se usa la marca de memoria predeterminada de D3DPOOL, el controlador de dispositivo determina dónde se asigna mejor la memoria para el búfer de vértices, que a menudo se conoce como memoria óptima para el controlador. La memoria óptima del controlador puede ser la memoria de vídeo local, la memoria de vídeo no local o la memoria del sistema.

La configuración de la \_ constante D3DUSAGE SOFTWAREPROCESSING con [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) permite el procesamiento de vértices de software en los datos de búfer de vértices. Esta marca es necesaria para el procesamiento de vértices de software en modo mixto. La marca no se puede usar para el modo de procesamiento de vértices de hardware. Los búferes de vértices usados con el procesamiento de vértices de software incluyen los siguientes:

-   Todos los flujos de entrada para [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).
-   Todos los flujos de entrada para [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) y [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

El razonamiento que se usa para determinar la ubicación de memoria: el sistema o el controlador óptimos para los búferes de vértice es el mismo que para las texturas. El procesamiento de vértices, incluida la transformación y la iluminación, en el hardware funciona mejor cuando se asignan los búferes de vértices en memoria óptima del controlador, mientras que el procesamiento de vértices de software funciona mejor con los búferes de vértices asignados en la memoria del sistema. En el caso de las texturas, la rasterización de hardware funciona mejor cuando se asignan texturas en la memoria óptima del controlador, mientras que la rasterización de software funciona mejor con las texturas de memoria del sistema.

Microsoft Direct3D 9 admite el procesamiento independiente de vértices, sin representar ningún primitivo con el método [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) . Este procesamiento de vértices independiente siempre se realiza en el software del procesador del host. Por este motivo, los búferes de vértices usados como orígenes establecidos con [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) deben crearse con la \_ marca D3DUSAGE SOFTWAREPROCESSING. La funcionalidad proporcionada por **IDirect3DDevice9::P rocessvertices** es idéntica a la de los métodos [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) y [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) al usar el procesamiento de vértices de software.

Si la aplicación realiza su propio procesamiento de vértices y pasa los vértices transformados, iluminados y recortados a los métodos de representación, la aplicación puede escribir directamente vértices en un búfer de vértices asignado en la memoria óptima del controlador. Esta técnica evita una operación de copia redundante más adelante. Tenga en cuenta que esta técnica no funcionará bien si la aplicación vuelve a leer los datos de un búfer de vértices, ya que las operaciones de lectura realizadas por el host desde la memoria óptima del controlador pueden ser muy lentas. Por lo tanto, si la aplicación necesita leer durante el procesamiento o escribe datos en el búfer de forma errática, un búfer de vértices de la memoria del sistema es una opción mejor.

Cuando se usan las características de procesamiento de vértices de Direct3D (pasando vértices no transformados a métodos de representación de búfer de vértices), el procesamiento puede producirse en el hardware o el software según el tipo de dispositivo y las marcas de creación de dispositivos. Se recomienda asignar búferes de vértices en el grupo D3DPOOL \_ predeterminado para obtener el mejor rendimiento en casi todos los casos. Cuando un dispositivo usa el procesamiento de vértices de hardware, hay una serie de optimizaciones adicionales que se pueden realizar en función de las marcas D3DUSAGE \_ Dynamic y D3DUSAGE \_ WRITEONLY. Vea IDirect3DDevice9:: CreateVertexBuffer para obtener más información sobre el uso de estas marcas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
