---
title: Interfaces principales (gráficos de Direct3D 12)
description: Las siguientes interfaces se declaran en d3d12. h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: a51e35fff74ab1d0251d64578de665ad4134a843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714393"
---
# <a name="core-interfaces"></a>Interfaces principales

Las siguientes interfaces se declaran en d3d12. h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Representa las asignaciones de almacenamiento para los comandos de la unidad de procesamiento de gráficos (GPU). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Una interfaz de la que [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) hereda. Representa un conjunto ordenado de comandos que se ejecutan en la GPU, a la vez que permite que la extensión admita otras listas de comandos que solo las de los gráficos (como compute y Copy). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Proporciona métodos para enviar listas de comandos, sincronizar la ejecución de la lista de comandos, instrumentar la cola de comandos y actualizar las asignaciones de iconos de recursos. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Un objeto de firma de comando permite a las aplicaciones especificar dibujos indirectos, incluido el formato de búfer, el tipo de comando y los enlaces de recursos que se van a usar. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor. Los montones descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Representa un adaptador virtual; se usa para crear asignadores de comandos, listas de comandos, colas de comandos, barreras, recursos, objetos de estado de canalización, montones, firmas de raíz, muestras y muchas vistas de recursos. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Representa un adaptador virtual y se expande en el intervalo de métodos proporcionado por [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Representa un adaptador virtual. Esta interfaz extiende [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) para crear objetos de estado de canalización a partir de descripciones de flujo de estado de canalización. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Representa un adaptador virtual. Esta interfaz extiende [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) para admitir la creación de montones de diagnóstico de propósito especial en la memoria del sistema que se conservan incluso en caso de que se produzca un escenario de error de GPU o de dispositivo quitado. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Representa un adaptador virtual. Esta interfaz extiende [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Representa un adaptador virtual. Esta interfaz extiende [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Representa un adaptador virtual. Esta interfaz extiende [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Una interfaz de la que heredan otras interfaces principales, incluidas [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)y [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Proporciona un método para volver al objeto de dispositivo con el que se creó. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Proporciona acceso en tiempo de ejecución a los datos de los datos extendidos (DRED) quitados del dispositivo. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Esta interfaz controla la configuración de los datos extendidos (DRED) eliminados del dispositivo. |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Representa una barrera, un objeto que se usa para la sincronización de la CPU y una o varias GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Representa una barrera. Esta interfaz extiende [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)y admite la recuperación de las marcas que se usan para crear la barrera original.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Encapsula una lista de comandos de gráficos para la representación. Incluye las API para instrumentar la ejecución de la lista de comandos y para establecer y borrar el estado de la canalización. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Encapsula una lista de comandos de gráficos para la representación, extendiendo la aplicación para admitir posiciones de ejemplo programables, copias atómicas para implementar técnicas de bloqueo temporal y pruebas de límites de profundidad opcionales. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Encapsula una lista de comandos de gráficos para la representación, extendiendo la interfaz para admitir la escritura de valores inmediatos directamente en un búfer. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Encapsula una lista de comandos de gráficos para la representación. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Encapsula una lista de comandos de gráficos para la representación, extendiendo la interfaz para admitir las pasadas de trazado y representación de Ray. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Un montón es una abstracción de la asignación de memoria contigua, que se usa para administrar la memoria física. Este montón se puede usar con objetos [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) para admitir recursos colocados o recursos reservados. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Representa una devolución de llamada definida por la aplicación que se utiliza para recibir notificaciones de los cambios de duración de un objeto. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Representa las funciones para controlar la duración de un objeto de seguimiento de duración. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Representa un comando meta. Un comando meta es un objeto de Direct3D 12 que representa un algoritmo acelerado por proveedores de hardware independientes (IHV). Es una referencia opaca a un generador de comandos implementado por el controlador. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Una interfaz de la que heredan [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) y [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) . Proporciona métodos para asociar los datos privados y anotar los nombres de objeto. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Una interfaz de la que muchas otras interfaces principales heredan de. Indica que el tipo de objeto encapsula cierta cantidad de memoria accesible por GPU; pero no indica fuertemente si la aplicación puede manipular la residencia del objeto.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Administra una biblioteca de canalizaciones, en particular la carga y la recuperación de PSO individuales. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Administra una biblioteca de canalizaciones. Esta interfaz extiende [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) para cargar PSO desde una descripción de flujo de estado de canalización. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Representa el estado de todos los sombreadores establecidos actualmente, así como ciertos objetos de estado de función fija. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Administra un montón de consulta. Un montón de consultas contiene una matriz de consultas, a la que hacen referencia los índices. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Encapsula una capacidad generalizada de la CPU y la GPU para leer y escribir en la memoria física, o en montones. Contiene abstracciones para organizar y manipular matrices simples de datos, así como datos multidimensionales optimizados para el muestreo del sombreador. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | La firma raíz define qué recursos se enlazan a la canalización de gráficos. La aplicación y los vínculos muestran las listas de comandos a los recursos que requieren los sombreadores. Actualmente, hay un gráfico y una firma de raíz de proceso por aplicación. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contiene un método para devolver la estructura de datos [**D3D12-root-Signature-DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserializada de una firma raíz serializada versión 1,0.  |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Representa una cantidad variable de estado de configuración, incluidos los sombreadores, que una aplicación administra como una sola unidad y que se asigna a un controlador que se va a procesar de forma atómica, como compilar u optimizar.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Proporciona métodos para obtener y establecer las propiedades de un [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Esta interfaz se utiliza para configurar el tiempo de ejecución para herramientas como PIX. No se pretende ni se admite en ningún otro escenario. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contiene métodos para devolver la estructura de datos [**D3D12-root-Signature-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) deserializada de cualquier versión de una firma raíz serializada.  |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
* [Jerarquía de la interfaz](interface-hierarchy.md)