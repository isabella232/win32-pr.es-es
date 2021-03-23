---
title: Sincronización de varios motores
description: En este tema se describe la sincronización del acceso a varios motores independientes que se encuentran en la mayoría de las GPU modernas.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2020
ms.locfileid: "104549065"
---
# <a name="multi-engine-synchronization"></a>Sincronización de varios motores

La mayoría de las GPU modernas contienen varios motores independientes que proporcionan una funcionalidad especializada. Muchos tienen uno o más motores de copia dedicados y un motor de proceso, que normalmente es distinto del motor 3D. Cada uno de estos motores puede ejecutar comandos en paralelo entre sí. Direct3D 12 proporciona acceso específico a los motores 3D, de proceso y de copia mediante colas y listas de comandos.

## <a name="gpu-engines"></a>Motores de GPU

En el diagrama siguiente se muestran los subprocesos de la CPU de un título, cada uno de los cuales rellena una o varias colas de copia, proceso y 3D. La cola 3D puede impulsar los tres motores de GPU; la cola de proceso puede impulsar los motores de proceso y de copia; y la cola de copia simplemente el motor de copia.

A medida que los distintos subprocesos rellenan las colas, no puede haber ninguna garantía sencilla del orden de ejecución, por lo tanto, la necesidad de mecanismos de sincronización &mdash; cuando el título los requiere.

![cuatro subprocesos que envían comandos a tres colas](images/gpu-engines.png)

En la imagen siguiente se muestra cómo un título puede programar el trabajo en varios motores de GPU, incluida la sincronización entre motores cuando sea necesario: muestra las cargas de trabajo por motor con dependencias entre motores. En este ejemplo, el motor de copia copia primero parte de la geometría necesaria para la representación. El motor 3D espera a que se completen estas copias y representa un paso previo de la geometría. Después, el motor de proceso lo usa. Los resultados de la [**distribución**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motor de proceso, junto con varias operaciones de copia de textura en el motor de copia, se consumen en el motor 3D para la llamada de [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.

![copia, gráficos y motores de proceso que se comunican](images/gpu-sync.png)

En el siguiente pseudocódigo se muestra cómo un título puede enviar este tipo de carga de trabajo.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

En el siguiente pseudocódigo se muestra la sincronización entre los motores de copia y 3D para realizar la asignación de memoria de tipo montón a través de un búfer en anillo. Los títulos tienen la flexibilidad de elegir el equilibrio adecuado entre maximizar el paralelismo (a través de un búfer grande) y reducir el consumo de memoria y la latencia (a través de un búfer pequeño).

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Escenarios de varios motores

Direct3D 12 le permite evitar la ejecución accidental de ineficiencias producidas por retrasos inesperados en la sincronización. También permite introducir la sincronización en un nivel superior en el que se puede determinar la sincronización necesaria con mayor certeza. Un segundo problema que trata las direcciones de varios motores es hacer que las operaciones costosas sean más explícitas, lo que incluye las transiciones entre el vídeo y el 3D que tradicionalmente eran costosas debido a la sincronización entre varios contextos de kernel.

En concreto, se pueden solucionar los siguientes escenarios con Direct3D 12.

-   Trabajo de GPU asincrónica y de prioridad baja. Esto permite la ejecución simultánea de trabajo de GPU de baja prioridad y operaciones atómicas que permiten que un subproceso de GPU consuma los resultados de otro subproceso no sincronizado sin bloqueos.
-   Trabajo de proceso de alta prioridad. Con el proceso en segundo plano es posible interrumpir la representación en 3D para realizar una pequeña cantidad de trabajo de proceso de alta prioridad. Los resultados de este trabajo pueden obtenerse pronto para el procesamiento adicional de la CPU.
-   Trabajo de proceso en segundo plano. Una cola de baja prioridad independiente para cargas de trabajo de proceso permite que una aplicación Use ciclos de GPU de reserva para realizar el cálculo en segundo plano sin un impacto negativo en las tareas de representación principal (u otras). Las tareas en segundo plano pueden incluir la descompresión de recursos o la actualización de simulaciones o estructuras de aceleración. Las tareas en segundo plano deben sincronizarse en la CPU con poca frecuencia (aproximadamente una vez por fotograma) para evitar la detención o la ralentización del trabajo en primer plano.
-   Transmisión por secuencias y carga de datos. Una cola de copia independiente reemplaza los conceptos de D3D11 de los datos iniciales y los recursos de actualización. Aunque la aplicación es responsable de obtener más detalles en el modelo de Direct3D 12, esta responsabilidad se refiere a la eficacia. La aplicación puede controlar la cantidad de memoria del sistema dedicada a almacenar en búfer los datos de carga. La aplicación puede elegir cuándo y cómo (CPU frente a GPU, bloqueo frente a no bloqueo) sincronizar y puede realizar un seguimiento del progreso y controlar la cantidad de trabajo en cola.
-   Mayor paralelismo. Las aplicaciones pueden usar colas más profundas para cargas de trabajo en segundo plano (por ejemplo, descodificación de vídeo) cuando tienen colas independientes para el trabajo en primer plano.

En Direct3D 12, el concepto de una cola de comandos es la representación de la API de una secuencia de trabajo de serie de aproximadamente que envía la aplicación. Las barreras y otras técnicas permiten que este trabajo se ejecute en una canalización o desordenado, pero la aplicación solo ve una escala de tiempo de finalización única. Esto corresponde al contexto inmediato en D3D11.

## <a name="synchronization-apis"></a>API de sincronización

### <a name="devices-and-queues"></a>Dispositivos y colas

El dispositivo Direct3D 12 tiene métodos para crear y recuperar colas de comandos de diferentes tipos y prioridades. La mayoría de las aplicaciones deben usar las colas de comandos predeterminadas porque permiten el uso compartido por parte de otros componentes. Las aplicaciones con requisitos de simultaneidad adicionales pueden crear colas adicionales. Las colas se especifican mediante el tipo de lista de comandos que consumen.

Consulte los siguientes métodos de creación de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una cola de comandos basada en información en una estructura de DESC de la [**cola de comandos de Direct3D 12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crea una lista de comandos del tipo de [**lista de comandos de Direct3D 12 \_ \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crea una barrera, anotando las marcas en las [**marcas de \_ barrera \_ de Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Las barreras se utilizan para sincronizar las colas.

Las colas de todos los tipos (3D, Compute y Copy) comparten la misma interfaz y están basadas en todas las listas de comandos.

Consulte los siguientes métodos de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : envía una matriz de listas de comandos para su ejecución. Cada lista de comandos definida por [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : establece un valor de barrera cuando la cola (que se ejecuta en la GPU) alcanza un punto determinado.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la cola espera hasta que la barrera especificada alcance el valor especificado.

Tenga en cuenta que los conjuntos no se consumen en ninguna cola y, por lo tanto, este tipo no se puede usar para crear una cola.

### <a name="fences"></a>Barreras

La API de varios motores proporciona API explícitas para crear y sincronizar mediante barreras. Una barrera es una construcción de sincronización controlada por un valor UINT64. La aplicación establece los valores de barrera. Una operación Signal modifica el valor de barrera y una operación de espera se bloquea hasta que la barrera alcanza el valor solicitado o mayor. Se puede desencadenar un evento cuando una barrera alcanza un valor determinado.

Consulte los métodos de la interfaz [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .

-   [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : devuelve el valor actual de la barrera.
-   [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : hace que se desencadene un evento cuando la barrera alcanza un valor determinado.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : establece la barrera en el valor especificado.

Las barreras permiten el acceso de CPU al valor de barrera actual y esperas y señales de CPU.

El método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) de la interfaz [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) actualiza una barrera del lado de la CPU. Esta actualización se produce inmediatamente. El método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) actualiza una barrera del lado de la GPU. Esta actualización se produce cuando se han completado todas las demás operaciones en la cola de comandos.

Todos los nodos de una configuración de varios motores pueden leer y reaccionar a cualquier barrera que alcance el valor correcto.

Las aplicaciones establecen sus propios valores de barrera, un buen punto de partida puede estar aumentando una barrera una vez por fotograma.

Se *puede* *rebobinar* una barrera. Esto significa que no es necesario que el valor de barrera se incremente únicamente. Si una operación de **señal** se pone en cola en dos colas de comandos diferentes, o si dos subprocesos de CPU están llamando a **señal** en una barrera, puede haber una carrera para determinar qué **señal** se completa en último lugar y, por lo tanto, qué valor de barrera es el que permanecerá. Si se rebobina una barrera, las nuevas esperas (incluidas las solicitudes de **SetEventOnCompletion** ) se compararán con el nuevo valor de barrera inferior y, por lo tanto, no se cumplirán, incluso si el valor de barrera hubiera sido lo suficientemente alto como para satisfacerlos. Si se produce una carrera, entre un valor que satisfará una espera pendiente y un valor inferior no *, se cumplirá la espera independientemente* del valor que quede después.

Las API de barrera proporcionan una eficaz funcionalidad de sincronización, pero pueden provocar problemas de depuración. Se recomienda usar cada barrera para indicar el progreso en una escala de tiempo con el fin de evitar carreras entre señalizadores.

### <a name="copy-and-compute-command-lists"></a>Copiar y calcular listas de comandos

Los tres tipos de lista de comandos usan la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , pero solo se admite un subconjunto de los métodos para copiar y calcular.

Las listas de comandos de copia y cálculo pueden usar los métodos siguientes.

-   [**Cercanos**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Determinado**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Las listas de comandos de Compute también pueden usar los métodos siguientes.

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Las listas de comandos de Compute deben establecer un valor de Compute PSO al llamar a [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Los paquetes no se pueden usar con las listas o colas de comandos de proceso o copia.

## <a name="pipelined-compute-and-graphics-example"></a>Ejemplo de proceso y gráficos de canalización

En este ejemplo se muestra cómo se puede usar la sincronización de barrera para crear una canalización de trabajo de proceso en una cola (a la que hace referencia `pComputeQueue` ) que se usa en el trabajo de gráficos en la cola `pGraphicsQueue` . El trabajo de cálculo y gráficos se canaliza con la cola de gráficos que consume el resultado del trabajo de proceso de varios fotogramas, y se utiliza un evento de CPU para limitar el trabajo total en cola.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Para admitir esta canalización, debe haber un búfer de `ComputeGraphicsLatency+1` diferentes copias de los datos que pasan de la cola de proceso a la cola de gráficos. Las listas de comandos deben usar UAVs e direccionamiento indirecto para leer y escribir desde la "versión" adecuada de los datos en el búfer. La cola de proceso debe esperar hasta que la cola de gráficos haya terminado de leer los datos del marco N para poder escribir el marco `N+ComputeGraphicsLatency` .

Tenga en cuenta que la cantidad de la cola de proceso que funcionaba con respecto a la CPU no depende directamente de la cantidad de almacenamiento en búfer requerida. sin embargo, el trabajo de GPU de cola más allá de la cantidad de espacio en búfer disponible es menos valioso.

Un mecanismo alternativo para evitar el direccionamiento indirecto sería crear varias listas de comandos correspondientes a cada una de las versiones "cambiadas de nombre" de los datos. En el ejemplo siguiente se usa esta técnica mientras se amplía el ejemplo anterior para permitir que las colas de proceso y de gráficos se ejecuten de forma más asincrónica.

## <a name="asynchronous-compute-and-graphics-example"></a>Ejemplo de cálculo y gráficos asincrónicos

En el ejemplo siguiente, los gráficos se pueden representar de forma asincrónica desde la cola de proceso. Todavía existe una cantidad fija de datos almacenados en búfer entre las dos fases; sin embargo, ahora el trabajo de gráficos se realiza de forma independiente y usa el resultado más actualizado de la fase de proceso como se conoce en la CPU cuando el trabajo de gráficos se pone en cola. Esto sería útil si otro origen estaba actualizando el trabajo de gráficos, por ejemplo, datos proporcionados por el usuario. Debe haber varias listas de comandos para permitir `ComputeGraphicsLatency` que los fotogramas de los gráficos funcionen al mismo tiempo, y la función `UpdateGraphicsCommandList` representa la actualización de la lista de comandos para incluir los datos de entrada más recientes y leer los datos de proceso del búfer adecuado.

La cola de proceso debe esperar a que la cola de gráficos finalice con los búferes de canalización, pero se ha introducido una tercera barrera ( `pGraphicsComputeFence` ) para que se pueda realizar un seguimiento del progreso de los gráficos que leen el trabajo de cálculo y el progreso de gráficos en general. Esto refleja el hecho de que los fotogramas de gráficos consecutivos podrían leer el mismo resultado de proceso u omitir un resultado de proceso. Un diseño más eficaz pero ligeramente más complicado usaría solo la barrera de gráficos única y almacenaría una asignación a las tramas de proceso utilizadas por cada fotograma gráfico.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Acceso a recursos de varias colas

Para tener acceso a un recurso de más de una cola, una aplicación debe cumplir las siguientes reglas.

-   El acceso a los recursos (consulte [**\_ \_ Estados de recursos de Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) viene determinado por la clase de tipo de cola no es un objeto de cola. Hay dos clases de tipo de cola: Compute/3D Queue es una clase de tipo, Copy es una segunda clase de tipo. Por lo tanto, un recurso que tiene una barrera para el \_ \_ Estado del recurso de sombreador que no es de píxeles \_ en una cola 3D se puede usar en ese estado en cualquier cola 3D o de proceso, en función de los requisitos de sincronización que requieren la mayoría de las escrituras que se van a serializar. Los Estados de los recursos que se comparten entre las dos clases de tipo (copia de \_ origen y \_ destino de copia) se consideran Estados diferentes para cada clase de tipo. De modo que si un recurso realiza la transición al destino \_ de copia en una cola de copia, no se puede acceder a él como destino de copia de las colas 3D o de proceso, y viceversa.

    En resumen.

    -   Un "objeto" de la cola es una sola cola.
    -   Una cola "tipo" es cualquiera de estas tres: compute, 3D y Copy.
    -   Una cola "clase de tipo" es cualquiera de estas dos: Compute/3D y Copy.

-   Las marcas de copia (copia del destino y el origen de la copia \_ \_ ) utilizadas como Estados iniciales representan los Estados de la clase de tipo de proceso o 3D. Para usar un recurso inicialmente en una cola de copia, debe comenzar en el Estado común. El Estado común se puede usar para todos los usos de una cola de copia mediante las transiciones de estado implícitas. 
-   Aunque el estado del recurso se comparte entre todas las colas de proceso y 3D, no se permite escribir en el recurso simultáneamente en diferentes colas. "Simultáneamente" significa que no está sincronizado. la ejecución no sincronizada no es posible en algún hardware. Se aplican las siguientes reglas.

    -   Solo una cola puede escribir en un recurso a la vez.
    -   Varias colas pueden leer desde el recurso siempre que no lean los bytes modificados por el escritor (la lectura de bytes que se escriben simultáneamente genera resultados no definidos).
    -   Una barrera debe usarse para sincronizar después de la escritura antes de que otra cola pueda leer los bytes escritos o realizar un acceso de escritura.

-   Los búferes de reserva que se presentan deben estar en \_ el \_ Estado común de estado de los recursos de Direct3D 12 \_ . 

## <a name="related-topics"></a>Temas relacionados

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)

[Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Administración de la memoria en Direct3D 12](memory-management.md)
