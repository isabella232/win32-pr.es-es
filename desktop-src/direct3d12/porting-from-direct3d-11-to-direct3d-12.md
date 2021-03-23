---
title: Portar de Direct3D 11 a Direct3D 12
description: En esta sección se proporcionan instrucciones sobre cómo migrar desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b5bc6784d6f96c3c1599a601a57bf68b0d612d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549158"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Portar de Direct3D 11 a Direct3D 12

En esta sección se proporcionan instrucciones sobre cómo migrar desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.

-   [Creación de dispositivos](#device-creation)
-   [Recursos confirmados](#committed-resources)
-   [Recursos reservados](#reserved-resources)
-   [Cargar datos](#uploading-data)
-   [Sombreadores y objetos de sombreador](#shaders-and-shader-objects)
-   [Enviar trabajo a la GPU](#submitting-work-to-the-gpu)
-   [Sincronización de CPU/GPU](#cpugpu-synchronization)
-   [Enlace de recursos](#resource-binding)
-   [Estado del recurso](#resource-state)
-   [Intercambio](#swapchains)
-   [Representación de funciones fijas](#fixed-function-rendering)
-   [Probabilidades y finalización](#odds-and-ends)
-   [Temas relacionados](#related-topics)

## <a name="device-creation"></a>Creación de dispositivos

Tanto Direct3D 11 como Direct3D 12 comparten un patrón de creación de dispositivos como. Los controladores de Direct3D 12 existentes son **D3D_FEATURE_LEVEL_11_0** o mejores, por lo que puede omitir los niveles de características más antiguos y los lmitations asociados.

Tenga en cuenta también que con Direct3D 12, debe enumerar explícitamente la información del dispositivo mediante interfaces de DXGI. En Direct3D 11, podría *encadenar de nuevo* al dispositivo DXGI desde el dispositivo Direct3D y esto no es compatible con Direct3D 12.

La creación de un dispositivo de software dewarp en Direct3D 12 se realiza proporcionando un adaptador explícito Obtenido de **IDXGIFcatory4:: EnumWarpAdapter**. El dispositivo WARP para Direct3D 12 solo está disponible en sistemas con la característica opcional **herramientas de gráficos** habilitada.

> [!NOTE]
> No hay ningún equivalente a **D3D11CreateDeviceAndSwapChain**. Incluso con Direct3D 11, se desaconseja el uso de esta función ya que a menudo es mejor crear el dispositivo y intercambio en pasos distintos.

## <a name="committed-resources"></a>Recursos confirmados

Los objetos creados con las siguientes interfaces en Direct3D 11, se traducen a lo que se denominan "recursos asignados" en Direct3D 12. Un recurso confirmado es un recurso que tiene asociado tanto el espacio de direcciones virtuales como las páginas físicas. Este es un concepto del modelo de memoria de controlador de dispositivos de Microsoft Windows 2 (WDD2), en el que se basa Direct3D 12.

Recursos de Direct3D 11:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) y [ **ID3D11Device:: CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) y [ **ID3D11Device: CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) y [ **ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) y [ **ID3D11Device:: CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

En Direct3D 12, todos se representan mediante [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) y [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Recursos reservados

Los recursos reservados son recursos donde solo se ha asignado el espacio de direcciones virtuales; la memoria física no se asigna hasta que haya una llamada a [**ID3D12Device:: CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Este es esencialmente el mismo concepto que los recursos en mosaico en Direct3D 11.

Las marcas ([**\_ \_ \_ marca de recursos varios de D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)) usadas en Direct3D 11 para configurar recursos en mosaico y, a continuación, asignarlas a la memoria física.

-   \_Recurso D3D11 \_ varios en \_ mosaico
-   \_Grupo de \_ iconos de varios recursos \_ de D3D11 \_

## <a name="uploading-data"></a>Cargar datos

En Direct3D 11 hay la apariencia de una sola escala de tiempo (llama a después de una secuencia, como los datos inicializados con los [**\_ \_ datos de subrecurso D3D11**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data), se realiza una llamada a [**ID3D11DeviceContext:: UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)y, a continuación, una llamada a [**ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). El número de copias creadas de los datos no es obvio para un desarrollador de Direct3D 11.

En Direct3D 12 hay dos escalas de tiempo: la escala de tiempo de la GPU (configurada mediante llamadas a [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)y [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) desde la memoria asignable) y la escala de tiempo de la CPU (determinada por las llamadas a [**map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)). Se proporcionan funciones auxiliares (en el archivo d3dx12. h) llamadas [**Updatesubresources**](updatesubresources1.md) que usan una escala de tiempo compartida. Hay varias variaciones de esta función auxiliar, una que usa [**ID3D12Device:: GetCopyableFootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints), otra que usa un mecanismo de asignación de montones y otra que usa un mecanismo de asignación de pila. Estas funciones auxiliares copian recursos en la GPU y la CPU, a través de un área de almacenamiento provisional intermedia de la memoria.

Normalmente, la GPU y la CPU tienen su propia copia de un recurso enlazada a su propia escala de tiempo. De forma similar, el enfoque de la escala de tiempo compartida mantiene dos copias.

## <a name="shaders-and-shader-objects"></a>Sombreadores y objetos de sombreador

En Direct3D 11 hay una gran cantidad de creación de objetos de sombreador y de estado, y el establecimiento del estado de esos objetos mediante los métodos de creación de [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) y los métodos de conjunto de [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) . Normalmente se realiza un gran número de llamadas a estos métodos, que luego se combinan en el momento de dibujar por el controlador para establecer el estado correcto de la canalización.

En Direct3D 12, este valor de estado de la canalización se ha combinado en un único objeto ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) para un motor de proceso y [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) para un motor de gráficos), que después se adjunta a una lista de comandos antes de la llamada a Draw con una llamada a [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Estas llamadas reemplazan todas las llamadas individuales para establecer sombreadores, el diseño de entrada, el estado de Blend, el estado de rasterizador, el estado de estarcido de profundidad, etc., en Direct3D 11

- Métodos de dispositivo 11: ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` , andD ``CreateRasterizerState`` .
- Métodos de contexto de dispositivo 11:  ``IASetInputLayout`` , ``xxSetShader`` , ``OMSetBlendState`` , ``OMSetDepthStencilState`` y ``RSSetState`` .

Aunque Direct3D 12 admite blobs compilados más antiguos, los sombreadores se deben compilar con el modelo de sombreador 5,1 con las API de FXC/D3DCompile o con el modelo de sombreador 6 mediante el compilador DXIL DXC. Debe validar la compatibilidad con el modelo de sombreador 6 con [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) y **D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Enviar trabajo a la GPU

en Direct3D 11, hay poco control sobre la forma en que se envía el trabajo, que se controla en gran medida por el controlador, aunque algún control se habilita a través de las llamadas [**ID3D11DeviceContext:: Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) y [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) .

En Direct3D 12, el envío de trabajo es muy explícito y está controlado por la aplicación. La construcción principal para el trabajo de envío es [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist), que se usa para registrar todos los comandos de aplicaciones (y es bastante similar en concepto al contexto diferido de ID3D11). La copia de seguridad de una lista de comandos la proporciona el [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator), que permite que la aplicación administre el uso de memoria de la lista de comandos al exponer realmente la memoria que el controlador de Direct3D 12 va a usar para almacenar la lista de comandos.

Por último, [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) es una cola primero en salir que almacena el orden correcto de las listas de comandos para su envío a la GPU. Solo cuando se haya completado la ejecución de una lista de comandos en la GPU, el controlador enviará la siguiente lista de comandos de la cola.

En Direct3D 11 no hay ningún concepto explícito de una cola de comandos. En la configuración común de Direct3D 12, la lista de comandos abierta actualmente **D3D12_COMMAND_LIST_TYPE_DIRECT** del marco actual se puede considerar análoga al contexto inmediato de Direct3D 11. Esto proporciona muchas de las mismas funciones.


| D3D11DeviceContext                  | Lista de ID3D12GraphicsCommand     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Draw, DrawInstanced                 | DrawInstanced                  |
| DrawIndexed, DrawIndexedInstanced   | DrawIndexedInstanced           |
| Dispatch                            | Dispatch                       |
| IASetInputLayout, xxSetShader, etc. | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> Una lista de comandos creada con **D3D12_COMMAND_LIST_TYPE_BUNDLE** se como a un contexto diferido. Direct3D 12 también admite el abiilty para tener acceso a algunas características de un *contexto inmediato* de forma simultánea para la representación a través de **D3D12_COMMAND_LIST_TYPE_COPY** y **D3D12_COMMAND_LIST_TYPE_COMPUTE** tipos de lista de comandos.

## <a name="cpugpu-synchronization"></a>Sincronización de CPU/GPU

En Direct3D 11, la sincronización de CPU/GPU era en gran medida automática y no había necesidad de que la aplicación conserve el estado de la memoria física.

en Direct3D 12, la aplicación debe administrar las dos escalas de tiempo (CPU y GPU) explícitamente. Esto requiere que la aplicación tenga que mantener la información, en qué recursos necesita la GPU y durante cuánto tiempo. Esto también significa que la aplicación es responsable de garantizar que el contenido de los recursos (por ejemplo, los recursos confirmados, los montones, los asignadores de comandos) no cambie hasta que la GPU haya terminado de usarlas.

El objeto principal para sincronizar las escalas de tiempo es el objeto [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) . La operación de vallas es sencilla y permite que la GPU señale Cuándo se ha completado una tarea. La GPU y la CPU pueden señalar y pueden esperar en las barreras.

Normalmente, el enfoque es que cuando se envía una lista de comandos para su ejecución, la GPU transmite una señal de barrera al finalizar (cuando ha terminado de leer los datos), lo que permite que la CPU reutilice o destruya los recursos.

En Direct3D 11, la marca [**ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) D3D11 de \_ escritura de asignación \_ \_ trata esencialmente cada recurso como un suministro interminable de memoria en el que la aplicación podría escribir (un proceso conocido como "cambio de nombre"). En Direct3D 12 de nuevo, el proceso es explícito: debe asignarse memoria adicional y deben usarse barreras para sincronizar las operaciones. Los búferes de anillo (que se componen de búferes grandes) pueden ser una buena técnica para esto; consulte el escenario de búfer de anillo en la [Administración de recursos basada en valla](fence-based-resource-management.md).

![usar un búfer en anillo](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Enlace de recursos

Las vistas de Direct3D 11 (vistas de recursos del sombreador, vistas de destino de representación, etc.), se han reemplazado en Direct3D 12 con el concepto de descriptor. Los métodos de creación todavía existen en Direct3D 12 (como [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) y [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)), a los que se llama después de haber creado el montón de descriptores, para escribir los datos en el montón. Ahora, los identificadores de descriptor descritos en una firma raíz controlan el enlace en Direct3D 12 y se envían mediante los métodos [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) o [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) .

Las firmas de raíz detallan las asignaciones entre el número de la ranura de firma raíz y las tablas de descriptor, donde la tabla de descriptores puede contener referencias a los recursos disponibles para los sombreadores de vértices, sombreadores de píxeles y otros sombreadores, como los búferes de constantes, las vistas de recursos del sombreador y los muestreadores. Esta flexibilidad desconecta el espacio de registro de HLSL del espacio de enlace de la API en Direct3D 12, a diferencia de Direct3D 11, donde hay una asignación de uno a uno entre ellos.

Una de las implicaciones de este sistema es que la aplicación es responsable de cambiar el nombre de las tablas de descriptores, lo que permite a los desarrolladores comprender el costo de rendimiento de cambiar incluso un único descriptor por llamada a Draw.

Una nueva característica de Direct3D 12 es que una aplicación puede controlar qué descriptores se comparten entre las fases del sombreador. En Direct3D 11, los recursos como UAVs se comparten entre todas las fases del sombreador. Al habilitar los descriptores para que se deshabiliten en determinadas fases del sombreador, los registros utilizados por los descriptores que se han deshabilitado están disponibles para que los descriptores que están habilitados para una fase de sombreador determinada puedan usarlos.

En la tabla siguiente se muestra una firma raíz de ejemplo.



| Espacio de parámetros raíz | Entrada de la tabla de descriptores         |
|---------------------|--------------------------------|
| 0                   | Rango de descriptores de VS B0-B13     |
| 1                   | Rango de descriptores de VS T0-T127    |
| 2                   | Rango de descriptores de VS S0-S16     |
| 3                   | Rango de descriptores de PS B0-B13     |
| ...                 |                                |
| 14                  | Rango de descriptores de DS S0-16      |
| 15                  | Intervalo de descriptor compartido U0-U63 |



 

## <a name="resource-state"></a>Estado del recurso

En Direct3D 11, el estado de los recursos no es mantenido por la aplicación, sino por el controlador.

En Direct3D 12, mantener el estado de los recursos se convierte en la responsabilidad de la aplicación, para habilitar el paralelismo completo en la grabación de las listas de comandos: la aplicación debe controlar las escalas de tiempo de grabación para las listas de comandos (que se pueden realizar en paralelo) y las escalas de tiempo de ejecución que deben ser secuenciales.

El método [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) controla la transición de estado de los recursos. Principalmente, la aplicación debe informar al controlador cuando el uso de recursos cambia. Por ejemplo, si un recurso se usa como destino de representación y, a continuación, se va a utilizar como entrada para un sombreador de vértices en la siguiente llamada a Draw, esto podría requerir una breve operación de detención en la GPU para completar la operación de destino de representación antes de controlar el sombreador de vértices.

Este sistema permite la sincronización exhaustiva (la GPU se detiene) de la canalización de gráficos, así como los vaciados de caché y, posiblemente, algunos cambios de diseño de memoria (como la vista de destino de representación para la descompresión de la vista de estarcido de profundidad).

Esto se conoce como barrera de transición. Hay otros tipos de barreras, en Direct3D 11, [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) ha habilitado la misma memoria física que van a usar dos recursos en mosaico diferentes. En Direct3D 12, esto se conoce como "barrera de alias". Las barreras de alias se pueden usar para los recursos en mosaico y colocados en Direct3D 12. Además, hay una barrera UAV. En Direct3D 11, es necesario serializar todas las operaciones de envío y dibujo de UAV, aunque estas operaciones se pueden canalizar o trabajar en paralelo. En Direct3D 12, esta restricción se quita mediante la adición de una barrera UAV. Una barrera UAV garantiza que las operaciones de UAV son secuenciales, por lo que si una segunda operación requiere que la primera se complete, la segunda se forzará a esperar por la adición de la barrera. La operación predeterminada para UAVs es simplemente que las operaciones se realizarán lo más rápido posible.

Claramente hay mejoras de rendimiento si se puede ejecutar una carga de trabajo en paralelo.

## <a name="swapchains"></a>Intercambio

La cadena de intercambio de DXGI es la base de las cadenas de intercambio en Direct3D 11 y 12. Hay algunas pequeñas diferencias, en Direct3D 11, los tres tipos de cadena de intercambio son SECUENCIAles, discard y FLIP \_ secuencial. En Direct3D 12 hay solo dos tipos: FLIP \_ Sequential y flip \_ discard. Como se indicó anteriormente, debe crear explícitamente el intercambio a través de **IDXGIFactory4**, o una versión posterior, y usar la misma interfaz para cualquier enumeración de adaptador.

En Direct3D 11 hay una rotación de búferes pendientes automática: solo se necesita una vista de destino de representación para el búfer de reserva 0. En Direct3D 12, la rotación del búfer es explícita, debe haber una vista de destino de representación para cada búfer de reserva. Use el método [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) para seleccionar el que se va a representar. De nuevo, esta flexibilidad adicional permite una mayor paralelización.

> [!NOTE]
> Aunque hay muchas maneras de configurar la aplicación, las aplicaciones suelen tener un **ID3D12CommandAllocator** por cada búfer de cadena de intercambio. Esto permite a la aplicación continuar con la creación de un conjunto de comandos para el siguiente fotograma mientras la GPU representa el anterior.

## <a name="fixed-function-rendering"></a>Representación de funciones fijas

En Direct3D 11, había algunos métodos que simplificaban varias operaciones de nivel superior, como [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (crear cadenas MIP completas) y [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (mediante la salida de flujo como entrada de sombreador sin ninguna otra entrada de la aplicación). Estos métodos no están disponibles en Direct3D 12, ya que la aplicación necesita controlar estas operaciones mediante la creación de sombreadores para realizarlos.

## <a name="odds-and-ends"></a>Probabilidades y finalización

En la tabla siguiente se muestran varias características similares a las de Direct3D 11 y 12, pero no son idénticas.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) permite agrupar las consultas, lo que reduce el costo.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Ahora, Predication se habilita mediante el uso de datos en un búfer completamente transparente. El objeto [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) de Direct3D 11 se ha reemplazado por [**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), que debe seguir una llamada a [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) y una operación de sincronización de GPU mediante una barrera para esperar a que los datos estén listos. Consulte [Predication](predication.md). |
| UAV/SO oculto contador                                                                  | La aplicación es responsable de la asignación y administración de los contadores de SO/UAV. Consulte los contadores de [salida de Stream](stream-output-counters.md) y los [contadores de UAV](uav-counters.md).                                                                                                                                                                                                                                                             |
| Resource Dynamic MinLOD (nivel de detalle de los detalles)                                       | Esto se ha pasado a la MinLOD estática del descriptor SRV.                                                                                                                                                                                                                                                                                                                                                                                 |
| Dibujo \* indirecto/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Los métodos indirectos de dibujo se combinan en el método de un [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .                                                                                                                                                                                                                                                                                                        |
| Los formatos de DepthStencil se intercalan                                                   | Los formatos de DepthStencil son planos. Por ejemplo, un formato de 24 bits de profundidad, 8 bits de la galería de símbolos se almacenaría en el formato 24/8/24/8... etc. en Direct3D 11, pero como 24/24/24... seguido de 8/8/8... en Direct3D 12. Tenga en cuenta que cada plano es su propio subrecurso en D3D12 (consulte [Subrecursos](subresources.md)).                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Los recursos reservados se pueden asignar a varios montones. Cuando un grupo de mosaicos se hubiera crecido en D3D11, se puede asignar un montón adicional en D3D12 en su lugar.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Guía de migración de DirectX 11 a DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
</dt> </dl>