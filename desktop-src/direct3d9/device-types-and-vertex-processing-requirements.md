---
description: El rendimiento de las operaciones de procesamiento de vértices, incluida la transformación y la iluminación, depende en gran medida de dónde exista el búfer de vértices en la memoria y del tipo de dispositivo de representación que se esté utilizando.
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964988"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a>Tipos de dispositivos y requisitos de procesamiento de vértices (Direct3D 9)

El rendimiento de las operaciones de procesamiento de vértices, incluida la transformación y la iluminación, depende en gran medida de dónde exista el búfer de vértices en la memoria y del tipo de dispositivo de representación que se esté utilizando. Las aplicaciones controlan la asignación de memoria para los búferes de vértices cuando se crean. Cuando se establece la marca de memoria D3DPOOL \_ SYSTEMMEM, el búfer de vértices se crea en la memoria del sistema. Cuando se usa la marca de memoria D3DPOOL DEFAULT, el controlador de dispositivo determina dónde se asigna mejor la memoria del búfer de vértices, a menudo denominada memoria óptima para el \_ controlador. La memoria óptima del controlador puede ser memoria de vídeo local, memoria de vídeo no local o memoria del sistema.

Establecer la constante D3DUSAGE \_ SOFTWAREPROCESSING con [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) habilita el procesamiento de vértices de software en los datos del búfer de vértices. Esta marca es necesaria para el procesamiento de vértices de software en modo mixto. La marca no se puede usar para el modo de procesamiento de vértices de hardware. Los búferes de vértices usados con el procesamiento de vértices de software incluyen lo siguiente:

-   Todos los flujos de entrada [**para IDirect3DDevice9::P rocessVertices .**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)
-   Todos los flujos de entrada [**para IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) [**e IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

El razonamiento que se usa para determinar la ubicación de memoria (sistema o controlador óptimo) para los búferes de vértices es el mismo que para las texturas. El procesamiento de vértices, incluida la transformación y la iluminación, en el hardware funciona mejor cuando los búferes de vértices se asignan en memoria óptima para el controlador, mientras que el procesamiento de vértices de software funciona mejor con búferes de vértices asignados en la memoria del sistema. En el caso de las texturas, la rasterización de hardware funciona mejor cuando las texturas se asignan en una memoria óptima para el controlador, mientras que la rasterización de software funciona mejor con texturas de memoria del sistema.

Microsoft Direct3D 9 admite el procesamiento independiente de vértices, sin representar ninguna primitiva con el método [**IDirect3DDevice9::P rocessVertices.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) Este procesamiento de vértices independiente siempre se realiza en software en el procesador host. Por este problema, los búferes de vértices que se usan como orígenes establecidos con [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) deben crearse con la marca D3DUSAGE \_ SOFTWAREPROCESSING. La funcionalidad proporcionada por **IDirect3DDevice9::P rocessVertices** es idéntica a la de los métodos [**IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) [**e IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) al usar el procesamiento de vértices de software.

Si la aplicación realiza su propio procesamiento de vértices y pasa vértices transformados, encendidos y recortados a los métodos de representación, la aplicación puede escribir directamente vértices en un búfer de vértice asignado en la memoria óptima del controlador. Esta técnica evita una operación de copia redundante más adelante. Tenga en cuenta que esta técnica no funcionará bien si la aplicación vuelve a leer los datos de un búfer de vértices, ya que las operaciones de lectura realizadas por el host desde la memoria óptima del controlador pueden ser muy lentas. Por lo tanto, si la aplicación necesita leer durante el procesamiento o escribe datos en el búfer de forma errática, un búfer de vértices de memoria del sistema es una mejor opción.

Cuando se usan las características de procesamiento de vértices de Direct3D (pasando vértices sin procesar a los métodos de representación de búfer de vértice), el procesamiento puede producirse en hardware o software en función del tipo de dispositivo y las marcas de creación de dispositivos. Se recomienda asignar búferes de vértices en el grupo D3DPOOL DEFAULT para obtener el mejor rendimiento \_ en prácticamente todos los casos. Cuando un dispositivo usa el procesamiento de vértices de hardware, hay una serie de optimizaciones adicionales que se pueden realizar en función de las marcas D3DUSAGE DYNAMIC y \_ D3DUSAGE \_ WRITEONLY. Vea IDirect3DDevice9::CreateVertexBuffer para obtener más información sobre el uso de estas marcas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
