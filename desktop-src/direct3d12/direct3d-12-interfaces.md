---
title: Interfaces principales (gráficos de Direct3D 12)
description: Las interfaces siguientes se declaran en d3d12.h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 0cc8fcecec2e2a0966ed34e23eb65ed9acd37e76
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812884"
---
# <a name="core-interfaces"></a>Interfaces principales

Las interfaces siguientes se declaran en d3d12.h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Representa las asignaciones de almacenamiento para los comandos de unidad de procesamiento gráfico (GPU). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Interfaz de la que [**se hereda ID3D12GraphicsCommandList.**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) Representa un conjunto ordenado de comandos que ejecuta la GPU, al tiempo que permite que la extensión admita otras listas de comandos que solo las de gráficos (por ejemplo, proceso y copia). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Proporciona métodos para enviar listas de comandos, sincronizar la ejecución de la lista de comandos, instrumentar la cola de comandos y actualizar las asignaciones de mosaicos de recursos. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Un objeto de firma de comando permite a las aplicaciones especificar el dibujo indirecto, incluido el formato de búfer, el tipo de comando y los enlaces de recursos que se usarán. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. Los montones de descriptores contienen muchos tipos de objeto que no forman parte de un objeto de estado de canalización (PSO), como vistas de recursos de sombreador (SRV), vistas de acceso desordenado (UAV), vistas de búfer constante (CBV) y muestreadores. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Representa un adaptador virtual; se usa para crear asignadores de comandos, listas de comandos, colas de comandos, barreras, recursos, objetos de estado de canalización, montones, firmas raíz, muestreadores y muchas vistas de recursos. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Representa un adaptador virtual y se expande en el intervalo de métodos proporcionados por [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Representa un adaptador virtual. Esta interfaz amplía [**ID3D12Device1 para**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) crear objetos de estado de canalización a partir de descripciones de flujo de estado de canalización. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Representa un adaptador virtual. Esta interfaz amplía [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) para admitir la creación de montones de diagnóstico de propósito especial en la memoria del sistema que persisten incluso en caso de un escenario de error de GPU o de dispositivo quitado. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device3.](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device4.](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device5.](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device6.](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device7.](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | Representa un adaptador virtual. Esta interfaz amplía [ID3D12Device8](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) para agregar métodos para administrar cachés de sombreador. |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Interfaz de la que heredan otras interfaces principales, como [**ID3D12PipelineLibrary,**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) [**ID3D12CommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)e [**ID3D12RootSignature.**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) Proporciona un método para volver al objeto de dispositivo en el que se creó. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Proporciona acceso en tiempo de ejecución a los datos de datos extendidos (DRED) quitados del dispositivo. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Esta interfaz controla la configuración de datos extendidos (DRED) quitados del dispositivo. |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Representa una barrera, un objeto utilizado para la sincronización de la CPU y una o varias GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Representa una barrera. Esta interfaz amplía [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)y admite la recuperación de las marcas usadas para crear la barrera original.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Encapsula una lista de comandos gráficos para la representación. Incluye API para instrumentar la ejecución de la lista de comandos y para establecer y borrar el estado de la canalización. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Encapsula una lista de comandos gráficos para la representación, ampliando el inicial para admitir posiciones de muestra programables, copias atómicas para implementar técnicas de bloqueos en tiempo de ejecución y pruebas opcionales de límites de profundidad. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Encapsula una lista de comandos gráficos para la representación, ampliando la interfaz para admitir la escritura de valores inmediatos directamente en un búfer. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Encapsula una lista de comandos gráficos para la representación. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Encapsula una lista de comandos gráficos para la representación, ampliando la interfaz para admitir el seguimiento de rayos y los pases de representación. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Un montón es una abstracción de asignación de memoria contigua, que se usa para administrar la memoria física. Este montón se puede usar con objetos [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) para admitir recursos colocados o recursos reservados. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Representa una devolución de llamada definida por la aplicación que se usa para recibir notificaciones de los cambios de duración de un objeto. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Representa los servicios para controlar la duración de un objeto de seguimiento de duración. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Representa un meta comando. Un meta comando es un objeto direct3D 12 que representa un algoritmo acelerado por proveedores de hardware independientes (IHV). Es una referencia opaca a un generador de comandos que implementa el controlador. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Interfaz de la que [**se heredan ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) e [**ID3D12DeviceChild.**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) Proporciona métodos para asociar datos privados y anotar nombres de objeto. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Interfaz de la que heredan muchas otras interfaces principales. Indica que el tipo de objeto encapsula cierta cantidad de memoria accesible para GPU; pero no indica claramente si la aplicación puede manipular la residencia del objeto.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Administra una biblioteca de canalizaciones, en particular cargando y recuperando PSO individuales. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Administra una biblioteca de canalizaciones. Esta interfaz amplía [**ID3D12PipelineLibrary para**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) cargar PSO desde una descripción de flujo de estado de canalización. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Representa el estado de todos los sombreadores establecidos actualmente, así como de determinados objetos de estado de función fijos. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Administra un montón de consultas. Un montón de consultas contiene una matriz de consultas a las que hacen referencia los índices. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Encapsula una capacidad generalizada de la CPU y la GPU para leer y escribir en memoria física o montones. Contiene abstracciones para organizar y manipular matrices simples de datos, así como datos multidimensionales optimizados para el muestreo del sombreador. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | La firma raíz define qué recursos están enlazados a la canalización de gráficos. La aplicación configura una firma raíz y vincula las listas de comandos a los recursos que requieren los sombreadores. Actualmente, hay un gráfico y una firma raíz de proceso por aplicación. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contiene un método para devolver la estructura de datos [**D3D12-ROOT-SIGNATURE-DESC deserialización**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) de una firma raíz serializada versión 1.0.  |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | Representa una sesión de caché de sombreador. |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Representa una cantidad variable de estado de configuración, incluidos los sombreadores, que una aplicación administra como una sola unidad y que se asigna a un controlador de forma atómica para procesar, como compilar u optimizar.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Proporciona métodos para obtener y establecer las propiedades de [**id3D12StateObject.**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject)  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Esta interfaz se usa para configurar el tiempo de ejecución para herramientas como CLR. No está previsto ni es compatible con ningún otro escenario. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contiene métodos para devolver la estructura de datos [**D3D12-ROOT-SIGNATURE-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) deserialización de cualquier versión de una firma raíz serializada.  |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
* [Jerarquía de la interfaz](interface-hierarchy.md)