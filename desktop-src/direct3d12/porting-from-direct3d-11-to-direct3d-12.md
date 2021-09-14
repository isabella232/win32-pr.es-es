---
title: Portar de Direct3D 11 a Direct3D 12
description: En esta sección se proporcionan algunas instrucciones sobre cómo portear desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072928"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Portar de Direct3D 11 a Direct3D 12

En esta sección se proporcionan algunas instrucciones sobre cómo portear desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.

-   [Creación de dispositivos](#device-creation)
-   [Recursos confirmados](#committed-resources)
-   [Recursos reservados](#reserved-resources)
-   [Carga de datos](#uploading-data)
-   [Sombreadores y objetos de sombreador](#shaders-and-shader-objects)
-   [Envío de trabajo a la GPU](#submitting-work-to-the-gpu)
-   [Sincronización de CPU/GPU](#cpugpu-synchronization)
-   [Enlace de recursos](#resource-binding)
-   [Estado del recurso](#resource-state)
-   [Cadenas de intercambio](#swapchains)
-   [Representación de funciones fijas](#fixed-function-rendering)
-   [Probabilidades y finales](#odds-and-ends)
-   [Temas relacionados](#related-topics)

## <a name="device-creation"></a>Creación de dispositivos

Tanto Direct3D 11 como Direct3D 12 comparten un patrón de creación de dispositivos similar. Los controladores existentes de Direct3D 12 D3D_FEATURE_LEVEL_11_0 o superiores, por lo que puede omitir los niveles de características anteriores y las limitaciones asociadas. 

Tenga en cuenta también que, con Direct3D 12, debe enumerar explícitamente la información del dispositivo mediante interfaces DXGI. En Direct3D 11,  podría encadenar de nuevo al dispositivo DXGI desde el dispositivo Direct3D, y esto no es compatible con Direct3D 12.

La creación de un dispositivo de software WARP en Direct3D 12 se realiza proporcionando un adaptador explícito obtenido de **IDXGIFactory4::EnumWarpAdapter**. El dispositivo WARP para Direct3D 12 solo está disponible en sistemas con la característica **opcional Herramientas de** gráficos habilitada.

> [!NOTE]
> No hay ningún equivalente a **D3D11CreateDeviceAndSwapChain**. Incluso con Direct3D 11, desaconsejamos el uso de esta función, ya que a menudo es mejor crear el dispositivo e intercambiar cadenas en pasos distintos.

## <a name="committed-resources"></a>Recursos confirmados

Los objetos creados con las interfaces siguientes en Direct3D 11 se traducen en lo que se denominan "recursos confirmados" en Direct3D 12. Un recurso confirmado es un recurso que tiene asociadas tanto el espacio de direcciones virtuales como las páginas físicas. Este es un concepto del modelo de memoria de Microsoft Windows Device Driver 2 (WDD2), en el que se basa Direct3D 12.

Recursos de Direct3D 11:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) e [ **ID3D11Device::CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) e [ **ID3D11Device:CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) e [ **ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) e [ **ID3D11Device::CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

En Direct3D 12, todos ellos se representan mediante [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) e [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Recursos reservados

Los recursos reservados son recursos en los que solo se ha asignado espacio de direcciones virtuales, no se asigna memoria física hasta que se llama a [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Este es básicamente el mismo concepto que los recursos en mosaico en Direct3D 11.

Las marcas [**(D3D11 \_ RESOURCE \_ MISC \_ FLAG)**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)que se usan en Direct3D 11 para configurar recursos en mosaico y, a continuación, asignarlos a la memoria física.

-   MOSAICO DE RECURSOS D3D11 \_ \_ \_
-   GRUPO DE MOSAICOS \_ MISC DE RECURSOS \_ D3D11 \_ \_

## <a name="uploading-data"></a>Carga de datos

En Direct3D 11 hay la apariencia de una sola escala de tiempo (llama a después de una secuencia, como los datos inicializados con [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data), se realiza una llamada a [**ID3D11DeviceContext::UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)y, a continuación, una llamada a [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). El número de copias creadas de los datos no es obvio para un desarrollador de Direct3D 11.

En Direct3D 12 hay dos escalas de tiempo, la escala de tiempo de GPU (configurada por llamadas a [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)y [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) desde la memoria asignable) y la escala de tiempo de CPU (determinada por llamadas a [**Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)). Se proporcionan funciones auxiliares (en el archivo d3dx12.h) [**denominadas Updatesubresources**](updatesubresources1.md) que usan una escala de tiempo compartida. Hay varias variaciones de esta función auxiliar, una que usa [**ID3D12Device::GetCopyableFootprints,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)otra que usa un mecanismo de asignación de montón y otra que usa un mecanismo de asignación de pila. Estas funciones auxiliares copian recursos en la GPU y la CPU, a través de un área de almacenamiento provisional intermedia de memoria.

Normalmente, la GPU y la CPU tienen su propia copia de un recurso vinculado a su propia escala de tiempo. El enfoque de escala de tiempo compartido mantiene de forma similar dos copias.

## <a name="shaders-and-shader-objects"></a>Sombreadores y objetos de sombreador

En Direct3D 11 hay una gran cantidad de creación de objetos de sombreador y estado, y el establecimiento del estado de esos objetos, mediante los métodos de creación [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) y los métodos de conjunto [**ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) Normalmente, se realiza un gran número de llamadas a estos métodos, que el controlador combina en tiempo de dibujo para establecer el estado de canalización correcto.

En Direct3D 12, esta configuración de estado de canalización se ha combinado en un único objeto ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) para un motor de proceso y [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) para un motor de gráficos), que luego se adjunta a una lista de comandos antes de la llamada draw con una llamada a [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Estas llamadas reemplazan todas las llamadas individuales para establecer sombreadores, diseño de entrada, estado de mezcla, estado de rasterizador, estado de galería de símbolos de profundidad, y así sucesivamente, en Direct3D 11

- Métodos del dispositivo 11: ``CreateInputLayout`` ``CreateXShader`` , , ``CreateDepthStencilState`` yD ``CreateRasterizerState`` .
- Métodos del contexto de dispositivo 11:  ``IASetInputLayout`` , , , y ``xxSetShader`` ``OMSetBlendState`` ``OMSetDepthStencilState`` ``RSSetState`` .

Aunque Direct3D 12 puede admitir blobs de sombreador compilados más antiguos, los sombreadores deben compilarse mediante el modelo de sombreador 5.1 con las API FXC/D3DCompile o mediante el modelo de sombreador 6 mediante el compilador DXIL DXC. Debe validar la compatibilidad de Shader Model 6 con [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) **y D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Envío de trabajo a la GPU

En Direct3D 11 hay poco control sobre cómo se envía realmente el trabajo, lo controla en gran medida el controlador, aunque se habilita algún control a través de las llamadas [**ID3D11DeviceContext::Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) e [**IDXGISwapChain1::P resent1.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)

En Direct3D 12, el envío de trabajo es muy explícito y controlado por la aplicación. La construcción principal para enviar el trabajo es [**ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)que se usa para registrar todos los comandos de aplicaciones (y es bastante similar en concepto al contexto diferido ID3D11). El almacén de respaldo de una lista de comandos lo proporciona [**id3D12CommandAllocator,**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)que permite a la aplicación administrar el uso de memoria de la lista de comandos exponiendo realmente la memoria que el controlador Direct3D 12 va a usar para almacenar la lista de comandos.

Por [**último, ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) es una cola de primer en salir que almacena el orden correcto de las listas de comandos para su envío a la GPU. Solo cuando una lista de comandos haya completado la ejecución en la GPU, el controlador envía la siguiente lista de comandos de la cola.

En Direct3D 11 no hay ningún concepto explícito de una cola de comandos. En la configuración común de Direct3D 12, la lista de comandos D3D12_COMMAND_LIST_TYPE_DIRECT abierta actualmente para el marco actual se puede considerar análoga **al** contexto inmediato de Direct3D 11. Esto proporciona muchas de las mismas funciones.


| D3D11DeviceContext                  | ID3D12GraphicsCommand List     |
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
> Una lista de comandos creada **con D3D12_COMMAND_LIST_TYPE_BUNDLE** es simliar a un contexto aplazado. Direct3D 12 también admite la abiilty  para acceder a  algunas características de un contexto inmediato simultáneamente a la representación a través de D3D12_COMMAND_LIST_TYPE_COPY y **D3D12_COMMAND_LIST_TYPE_COMPUTE** de lista de comandos.

## <a name="cpugpu-synchronization"></a>Sincronización de CPU/GPU

En Direct3D 11, la sincronización de CPU/GPU era en gran medida automática y no era necesario que la aplicación conservase el estado de la memoria física.

En Direct3D 12, la aplicación debe administrar explícitamente las dos escalas de tiempo (CPU y GPU). Esto requiere que la aplicación mantenga la información sobre qué recursos necesita la GPU y durante cuánto tiempo. Esto también significa que la aplicación es responsable de garantizar que el contenido de los recursos (recursos confirmados, montones, asignadores de comandos, por ejemplo) no cambie hasta que la GPU haya terminado de usarlos.

El objeto principal para sincronizar las escalas de tiempo es [**el objeto ID3D12Fence.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) El funcionamiento de las barreras es bastante sencillo, ya que permiten que la GPU señale cuando se ha completado una tarea. Tanto la GPU como la CPU pueden señalar y pueden esperar en barreras.

Normalmente, el enfoque es que al enviar una lista de comandos para su ejecución, la GPU transmite una señal de barrera al finalizar (cuando ha terminado de leer los datos), lo que permite que la CPU reutilice o destruya los recursos.

En Direct3D 11, la marca de mapa [**D3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) flag D3D11 MAP WRITE DISCARD trata básicamente cada recurso como una fuente infinita de memoria en la que la aplicación podría escribir (un proceso conocido como "cambio de \_ \_ \_ nombre"). En Direct3D 12 de nuevo, el proceso es explícito: es necesario asignar memoria adicional y se deben usar barreras para sincronizar las operaciones. Los búferes en anillo (que constan de búferes grandes) pueden ser una buena técnica para esto; consulte el escenario de búfer en anillo en [Fence-Based Resource Management](fence-based-resource-management.md).

![uso de un búfer en anillo](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Enlace de recursos

Las vistas de Direct3D 11 (vistas de recursos de sombreador, vistas de destino de representación, entre otras), se han reemplazado en gran medida en Direct3D 12 por el concepto de descriptor. Los métodos de creación siguen existiendo en Direct3D 12 (como [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) y [**CreateRenderTargetView),**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)a los que se llama después de crear el montón de descriptores, para escribir los datos en el montón. El enlace en Direct3D 12 ahora se controla mediante identificadores de descriptor descritos en una firma raíz y se envían mediante los [**métodos SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) o [**SetComputeRootDescriptorTable.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)

Las firmas raíz detallan las asignaciones entre el número de ranura de firma raíz y las tablas de descriptores, donde la tabla de descriptores puede contener referencias a recursos disponibles para sombreadores de vértices, sombreadores de píxeles y otros sombreadores, como búferes constantes, vistas de recursos de sombreador y muestreadores. Esta flexibilidad desconecta el espacio de registro HLSL del espacio de enlace de API en Direct3D 12, a diferencia de Direct3D 11, donde hay una asignación de uno a uno entre estos.

Una de las implicaciones de este sistema es que la aplicación es responsable de cambiar el nombre de las tablas de descriptores, lo que permite a los desarrolladores comprender el costo de rendimiento de cambiar incluso un único descriptor por llamada a draw.

Una nueva característica de Direct3D 12 es que una aplicación puede controlar qué descriptores se comparten entre las fases del sombreador. En Direct3D 11, los recursos, como los UAV, se comparten entre todas las fases del sombreador. Al permitir que los descriptores se deshabiliten para determinadas fases del sombreador, los registros que usan los descriptores que se han deshabilitado están disponibles para que los utilicen los descriptores que están habilitados para una fase de sombreador determinada.

En la tabla siguiente se muestra una firma raíz de ejemplo.



| Ranura de parámetros raíz | Entrada de tabla descriptor         |
|---------------------|--------------------------------|
| 0                   | Intervalo de descriptores de VS b0-b13     |
| 1                   | Intervalo de descriptores de VS t0-t127    |
| 2                   | Intervalo de descriptores de VS s0-s16     |
| 3                   | Intervalo del descriptor de PS b0-b13     |
| ...                 |                                |
| 14                  | Intervalo de descriptores de DS s0-16      |
| 15                  | Intervalo de descriptor compartido u0-u63 |



 

## <a name="resource-state"></a>Estado del recurso

En Direct3D 11, el estado del recurso no lo mantiene la aplicación, sino el controlador.

En Direct3D 12, el mantenimiento del estado de los recursos se convierte en responsabilidad de la aplicación, para habilitar el paralelismo completo en la grabación de listas de comandos: la aplicación debe controlar las escalas de tiempo de grabación de las listas de comandos (que se pueden realizar en paralelo) y las escalas de tiempo de ejecución que deben ser secuenciales.

El método [**ResourceBarija**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) controla una transición de estado de recurso. Principalmente, la aplicación debe informar al controlador cuándo cambia el uso de recursos. Por ejemplo, si un recurso se usa como destino de representación y, a continuación, se va a usar como entrada para un sombreador de vértices en la siguiente llamada a draw, esto podría requerir un breve período de detención en la operación de GPU para completar la operación de destino de representación antes de controlar el sombreador de vértices.

Este sistema permite la sincronización más específica (las detenciones de GPU) de la canalización de gráficos, así como vaciados de caché y posiblemente algunos cambios de diseño de memoria (como la vista de destino de representación para descomprimir la vista de galería de símbolos de profundidad).

Esto se conoce como barrera de transición. Hay otros tipos de barreras, en Direct3D 11, [**id3D11DeviceContext2::TiledResourceBarresource habilitó**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) la misma memoria física para que la usen dos recursos en mosaico diferentes. En Direct3D 12, esto se conoce como una "barrera de alias". Las barreras de alias se pueden usar para los recursos en mosaico y colocados en Direct3D 12. Además, existe la barrera UAV. En Direct3D 11, es necesario serializar todas las operaciones de envío y dibujo de UAV, aunque estas operaciones se pueden canalizaciones o funcionan en paralelo. Para Direct3D 12, esta restricción se quita mediante la adición de una barrera UAV. Una barrera UAV garantiza que las operaciones de UAV son secuenciales, por lo que si una segunda operación requiere que la primera se complete, la segunda se verá forzada a esperar por la adición de la barrera. La operación predeterminada para los UAV es simplemente que las operaciones continúen lo más rápido posible.

Claramente, hay mejoras de rendimiento si se puede paralelizar una carga de trabajo.

## <a name="swapchains"></a>Cadenas de intercambio

La cadena de intercambio DXGI es la base para las cadenas de intercambio en Direct3D 11 y 12. Hay algunas diferencias menores, en Direct3D 11 los tres tipos de cadena de intercambio son SEQUENTIAL, DISCARD y FLIP \_ SEQUENTIAL. Para Direct3D 12 solo hay dos tipos: FLIP \_ SEQUENTIAL y FLIP \_ DISCARD. Como se indicó anteriormente, debe crear explícitamente la cadena de intercambio a través de **IDXGIFactory4** o posterior, y usar la misma interfaz para cualquier enumeración de adaptador.

En Direct3D 11 hay rotación automática del búfer de reserva: solo se necesita una vista de destino de representación para el búfer de reserva 0. En Direct3D 12, la rotación de búferes es explícita, debe haber una vista de destino de representación para cada búfer de reserva. Use el [**método IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) para seleccionar en qué se va a representar. De nuevo, esta flexibilidad adicional permite una mayor paralelización.

> [!NOTE]
> Aunque hay muchas maneras de configurar la aplicación, por lo general las aplicaciones tienen un **ID3D12CommandAllocator** por búfer de cadena de intercambio. Esto permite a la aplicación continuar con la creación de un conjunto de comandos para el siguiente fotograma mientras la GPU representa el anterior.

## <a name="fixed-function-rendering"></a>Representación de funciones fijas

En Direct3D 11 había algunos métodos que simplificaban varias operaciones de nivel superior, como [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (creación de cadenas mip completa) y [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (mediante la salida de flujo como entrada del sombreador sin más entrada de la aplicación). Estos métodos no están disponibles en Direct3D 12; la aplicación debe controlar estas operaciones mediante la creación de sombreadores para realizarlas.

## <a name="odds-and-ends"></a>Probabilidades y finales

En la tabla siguiente se muestra una serie de características que son similares entre Direct3D 11 y 12, pero no son idénticas.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) permite agrupar las consultas, lo que reduce el costo.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | La predicación ahora está habilitada al tener datos en un búfer totalmente transparente. El objeto Id3D 11 [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) se reemplaza por [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), que debe seguir una llamada a [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) y una operación de sincronización de GPU mediante una barrera para esperar a que los datos estén listos. Consulte [Predication](predication.md). |
| Contador oculto UAV/SO                                                                  | La aplicación es responsable de la asignación y administración de contadores SO/UAV. Consulte [Contadores de salida de flujo y](stream-output-counters.md) [Contadores de UAV.](uav-counters.md)                                                                                                                                                                                                                                                             |
| MinLOD dinámico de recursos (nivel mínimo de detalle)                                       | Se ha movido al minLOD estático del descriptor SRV.                                                                                                                                                                                                                                                                                                                                                                                 |
| Draw \* Indirect/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Los métodos indirectos de dibujo se combinan en el único [**método ExecuteIndirect.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)                                                                                                                                                                                                                                                                                                        |
| Los formatos depthStencil se intercalan                                                   | Los formatos depthStencil son planas. Por ejemplo, un formato de 24 bits de profundidad, 8 bits de galería de símbolos se almacenarían con el formato 24/8/24/8... etc en Direct3D 11, pero como 24/24/24... seguido de 8/8/8... en Direct3D 12. Tenga en cuenta que cada plano es su propio subrecurso en D3D12 (consulte [Subrecursos).](subresources.md)                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Los recursos reservados se pueden asignar a varios montones. Cuando se hubiera crecido un grupo de mosaicos en D3D11, se puede asignar un montón adicional en D3D12 en su lugar.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Guía de porte de DirectX 11 a DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md)
</dt> </dl>
