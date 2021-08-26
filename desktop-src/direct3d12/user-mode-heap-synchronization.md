---
title: Sincronización de varios motores
description: En este tema se describe cómo sincronizar el acceso a los varios motores independientes que se encuentran en las GPU más modernas.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: 2d250133d8cacb26d933d3774f397de4c949c72b7b58114759791c103d374c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987564"
---
# <a name="multi-engine-synchronization"></a>Sincronización de varios motores

Las GPU más modernas contienen varios motores independientes que proporcionan funcionalidad especializada. Muchos tienen uno o varios motores de copia dedicados y un motor de proceso, normalmente distinto del motor 3D. Cada uno de estos motores puede ejecutar comandos en paralelo entre sí. Direct3D 12 proporciona acceso por completo a los motores 3D, de proceso y de copia, mediante colas y listas de comandos.

## <a name="gpu-engines"></a>Motores de GPU

En el diagrama siguiente se muestran los subprocesos de CPU de un título, y cada uno de ellos rellenará una o varias de las colas de copia, proceso y 3D. La cola 3D puede impulsar los tres motores de GPU; la cola de proceso puede impulsar los motores de proceso y copia; y la cola de copia simplemente el motor de copia.

A medida que los distintos subprocesos rellenan las colas, no puede haber ninguna garantía sencilla del orden de ejecución, de ahí la necesidad de mecanismos de sincronización cuando el título &mdash; las requiera.

![cuatro subprocesos que envían comandos a tres colas](images/gpu-engines.png)

En la imagen siguiente se muestra cómo un título puede programar el trabajo en varios motores de GPU, incluida la sincronización entre motores cuando sea necesario: muestra las cargas de trabajo por motor con dependencias entre motores. En este ejemplo, el motor de copia copia primero parte de la geometría necesaria para la representación. El motor 3D espera a que se completen estas copias y representa un paso previo sobre la geometría. A continuación, el motor de proceso lo consume. El motor 3D consume los resultados de [**dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motor de proceso, junto con varias operaciones de copia de textura en el motor de copia para la llamada [**draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.

![copia, gráficos y motores de proceso que se comunican](images/gpu-sync.png)

En el pseudocódigo siguiente se muestra cómo un título podría enviar este tipo de carga de trabajo.

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

El siguiente pseudocódigo ilustra la sincronización entre los motores de copia y 3D para realizar la asignación de memoria como montón a través de un búfer en anillo. Los títulos tienen la flexibilidad de elegir el equilibrio adecuado entre maximizar el paralelismo (a través de un búfer grande) y reducir el consumo y la latencia de memoria (a través de un búfer pequeño).

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

Direct3D 12 permite evitar que accidentalmente se ejecuten ineficiencias causadas por retrasos inesperados en la sincronización. También permite introducir la sincronización en un nivel superior, donde la sincronización necesaria se puede determinar con mayor certeza. Un segundo problema que abordan los varios motores es que las operaciones costosas son más explícitas, lo que incluye transiciones entre 3D y vídeo que tradicionalmente eran costosas debido a la sincronización entre varios contextos de kernel.

En concreto, se pueden abordar los siguientes escenarios con Direct3D 12.

-   Trabajo de GPU asincrónico y de prioridad baja. Esto permite la ejecución simultánea de operaciones atómicas y de trabajo de GPU de prioridad baja que permiten que un subproceso de GPU consuma los resultados de otro subproceso sin sincronizar sin bloqueo.
-   Trabajo de proceso de alta prioridad. Con el proceso en segundo plano es posible interrumpir la representación en 3D para realizar una pequeña cantidad de trabajo de proceso de alta prioridad. Los resultados de este trabajo se pueden obtener pronto para un procesamiento adicional en la CPU.
-   Trabajo de proceso en segundo plano. Una cola de prioridad baja independiente para cargas de trabajo de proceso permite que una aplicación use ciclos de GPU de reserva para realizar cálculos en segundo plano sin afectar negativamente a las tareas de representación principal (u otras). Las tareas en segundo plano pueden incluir la descompresión de recursos o la actualización de simulaciones o estructuras de aceleración. Las tareas en segundo plano se deben sincronizar en la CPU con poca frecuencia (aproximadamente una vez por fotograma) para evitar detener o ralentizar el trabajo en primer plano.
-   Streaming y carga de datos. Una cola de copia independiente reemplaza los conceptos D3D11 de los datos iniciales y los recursos de actualización. Aunque la aplicación es responsable de más detalles en el modelo Direct3D 12, esta responsabilidad viene con potencia. La aplicación puede controlar la cantidad de memoria del sistema dedicada al almacenamiento en búfer de los datos de carga. La aplicación puede elegir cuándo y cómo (CPU frente a GPU, bloqueo frente a no bloqueo) para sincronizarse, y puede realizar un seguimiento del progreso y controlar la cantidad de trabajo en cola.
-   Mayor paralelismo. Las aplicaciones pueden usar colas más profundas para cargas de trabajo en segundo plano (por ejemplo, descodificación de vídeo) cuando tienen colas independientes para el trabajo en primer plano.

En Direct3D 12, el concepto de cola de comandos es la representación de API de una secuencia de trabajo en serie aproximadamente enviada por la aplicación. Las barreras y otras técnicas permiten que este trabajo se ejecute en una canalización o fuera de orden, pero la aplicación solo ve una escala de tiempo de finalización única. Esto corresponde al contexto inmediato en D3D11.

## <a name="synchronization-apis"></a>API de sincronización

### <a name="devices-and-queues"></a>Dispositivos y colas

El dispositivo Direct3D 12 tiene métodos para crear y recuperar colas de comandos de diferentes tipos y prioridades. La mayoría de las aplicaciones deben usar las colas de comandos predeterminadas porque permiten el uso compartido por parte de otros componentes. Las aplicaciones con requisitos de simultaneidad adicionales pueden crear colas adicionales. Las colas se especifican mediante el tipo de lista de comandos que consumen.

Consulte los siguientes métodos de creación [**de ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) crea una cola de comandos basada en la información de una estructura [**\_ \_ \_ DESC COMMAND QUEUE de Direct3D 12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) crea una lista de comandos de tipo [**Direct3D 12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) crea una barrera y marca las marcas de [**direct3D 12 \_ FENCE \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Las barreras se usan para sincronizar las colas.

Las colas de todos los tipos (3D, proceso y copia) comparten la misma interfaz y se basan en la lista de comandos.

Consulte los métodos siguientes de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**ExecuteCommandLists:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) envía una matriz de listas de comandos para su ejecución. Cada lista de comandos que se define [**mediante ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Señal:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) establece un valor de barrera cuando la cola (que se ejecuta en la GPU) alcanza un punto determinado.
-   [**Wait:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) la cola espera hasta que la barrera especificada alcanza el valor especificado.

Tenga en cuenta que las agrupaciones no las consume ninguna cola y, por tanto, este tipo no se puede usar para crear una cola.

### <a name="fences"></a>Barreras

La API de varios motores proporciona API explícitas para crear y sincronizar mediante barreras. Una barrera es una construcción de sincronización controlada por un valor UINT64. La aplicación establece los valores de barrera. Una operación de señal modifica el valor de la barrera y una operación de espera se bloquea hasta que la barrera ha alcanzado el valor solicitado o superior. Se puede desencadena un evento cuando una barrera alcanza un valor determinado.

Consulte los métodos de la [**interfaz ID3D12Fence.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)

-   [**GetCompletedValue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) devuelve el valor actual de la barrera.
-   [**SetEventOnCompletion:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) hace que un evento se desenlome cuando la barrera alcanza un valor determinado.
-   [**Señal:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) establece la barrera en el valor especificado.

Las barreras permiten el acceso de CPU al valor de barrera actual y las esperas y señales de CPU.

El [**método Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) de la interfaz [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) actualiza una barrera desde el lado de la CPU. Esta actualización se produce inmediatamente. El [**método Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) en [**ID3D12CommandQueue actualiza**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) una barrera del lado de GPU. Esta actualización se produce después de que se hayan completado todas las demás operaciones de la cola de comandos.

Todos los nodos de una configuración de varios motores pueden leer y reaccionar ante cualquier barrera que alcance el valor correcto.

Las aplicaciones establecen sus propios valores de barrera, un buen punto de partida podría ser aumentar una barrera una vez por fotograma.

Se puede *volver* a *abrir una barrera.* Esto significa que el valor de la barrera no tiene que incrementarse únicamente. Si  una operación Signal se pone en cola en dos colas de comandos diferentes, o si dos subprocesos de CPU llaman a **Signal** en una barrera, puede haber una carrera para determinar qué **señal** se completa en último lugar y, por tanto, qué valor de barrera es el que permanecerá. Si se vuelve a abrir una barrera, las nuevas esperas (incluidas las solicitudes **SetEventOnCompletion)** se compararán con el nuevo valor de barrera inferior y, por lo tanto, es posible que no se satisfagan, incluso si el valor de la barrera anteriormente había sido lo suficientemente alto como para satisfacerlos. Si se produce una carrera, entre un valor que cumplirá una espera  pendiente y un valor inferior que no lo hará, la espera se cumplirá independientemente del valor que permanezca más adelante.

Las API de barrera proporcionan una funcionalidad de sincronización eficaz, pero pueden crear problemas potencialmente difíciles de depurar. Se recomienda que cada barrera solo se utilice para indicar el progreso en una escala de tiempo para evitar carreras entre los señalizadores.

### <a name="copy-and-compute-command-lists"></a>Copiar y calcular listas de comandos

Los tres tipos de lista de comandos usan la interfaz [**ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) pero solo se admite un subconjunto de los métodos para la copia y el proceso.

Las listas de comandos de copia y proceso pueden usar los métodos siguientes.

-   [**Cerrar**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Restablecer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Las listas de comandos de proceso también pueden usar los métodos siguientes.

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

Las listas de comandos de proceso deben establecer un PSO de proceso al llamar a [**SetPipelineState.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)

Las agrupaciones no se pueden usar con listas o colas de comandos de proceso o copia.

## <a name="pipelined-compute-and-graphics-example"></a>Ejemplo de proceso y gráficos canalizados

En este ejemplo se muestra cómo se puede usar la sincronización de barreras para crear una canalización de trabajo de proceso en una cola (a la que hace referencia ) que consume el trabajo de gráficos `pComputeQueue` en la cola `pGraphicsQueue` . El trabajo de proceso y gráficos se canaliza con la cola de gráficos que consume el resultado del trabajo de proceso de varios fotogramas hacia atrás, y se usa un evento de CPU para limitar el trabajo total en cola.

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

Para admitir esta canalización, debe haber un búfer de diferentes copias de los datos que pasan de la cola de proceso a `ComputeGraphicsLatency+1` la cola de gráficos. Las listas de comandos deben usar UAV y direccionamiento indirecto para leer y escribir desde la "versión" adecuada de los datos en el búfer. La cola de proceso debe esperar hasta que la cola de gráficos haya terminado de leer de los datos del fotograma N antes de poder escribir el marco `N+ComputeGraphicsLatency` .

Tenga en cuenta que la cantidad de cola de proceso que ha funcionado en relación con la CPU no depende directamente de la cantidad de almacenamiento en búfer necesaria; sin embargo, el trabajo de la GPU en cola más allá de la cantidad de espacio de búfer disponible es menos valioso.

Un mecanismo alternativo para evitar el direccionamiento indirecto sería crear varias listas de comandos correspondientes a cada una de las versiones "con nombre" de los datos. En el ejemplo siguiente se usa esta técnica al ampliar el ejemplo anterior para permitir que las colas de proceso y gráficos se ejecuten de forma más asincrónica.

## <a name="asynchronous-compute-and-graphics-example"></a>Ejemplo de gráficos y proceso asincrónico

En este ejemplo siguiente se permite que los gráficos se represente de forma asincrónica desde la cola de proceso. Todavía hay una cantidad fija de datos almacenados en búfer entre las dos fases, pero ahora el trabajo de gráficos continúa de forma independiente y usa el resultado más actualizado de la fase de proceso, como se conoce en la CPU cuando el trabajo de gráficos se pone en cola. Esto sería útil si otro origen actualizase el trabajo de gráficos, por ejemplo, la entrada del usuario. Debe haber varias listas de comandos para permitir que los fotogramas de los gráficos funcionen a la vez y la función representa la actualización de la lista de comandos para incluir los datos de entrada más recientes y leer de los datos de proceso desde el búfer `ComputeGraphicsLatency` `UpdateGraphicsCommandList` adecuado.

La cola de proceso todavía debe esperar a que la cola de gráficos finalice con los búferes de canalización, pero se introduce una tercera barrera ( ) para que se pueda realizar un seguimiento del progreso del trabajo de proceso de lectura de gráficos frente al progreso de gráficos en `pGraphicsComputeFence` general. Esto refleja el hecho de que ahora los fotogramas gráficos consecutivos podrían leer desde el mismo resultado de proceso o podrían omitir un resultado de proceso. Un diseño más eficaz, pero ligeramente más complicado, usaría solo la barrera de gráficos única y almacenaría una asignación a los fotogramas de proceso utilizados por cada fotograma gráfico.

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

Para acceder a un recurso en más de una cola, una aplicación debe cumplir las reglas siguientes.

-   El acceso a los recursos (consulte [**Direct3D 12 \_ RESOURCE \_ STATES)**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)viene determinado por la clase de tipo de cola no el objeto queue. Hay dos clases de tipo de cola: Compute/3D queue es una clase de tipo, Copy es una segunda clase de tipo. Por lo tanto, un recurso que tiene una barrera para el estado NON PIXEL SHADER RESOURCE en una cola 3D se puede usar en ese estado en cualquier cola 3D o Compute, sujeto a los requisitos de sincronización que requieren que la mayoría de las escrituras se puedan \_ \_ \_ serializar. Los estados de recursos que se comparten entre las dos clases de tipo (COPY SOURCE y COPY DEST) se consideran estados diferentes \_ para cada clase de \_ tipo. De modo que si un recurso pasa a COPY DEST en una cola de copia, no se puede acceder a él como destino de copia desde las colas 3D o Compute, \_ y viceversa.

    Para resumir.

    -   Un "objeto" de cola es cualquier cola única.
    -   Un "tipo" de cola es cualquiera de estos tres: Compute, 3D y Copy.
    -   Una "clase de tipo" de cola es cualquiera de estas dos: Compute/3D y Copy.

-   Las marcas COPY (COPY DEST y COPY SOURCE) usadas como estados iniciales representan los estados de la clase de tipo \_ \_ 3D/Compute. Para usar un recurso inicialmente en una cola de copia, debe iniciarse en el estado COMMON. El estado COMMON se puede usar para todos los usos de una cola de copia mediante las transiciones de estado implícitas. 
-   Aunque el estado del recurso se comparte entre todas las colas de Proceso y 3D, no se permite escribir en el recurso simultáneamente en distintas colas. "Simultáneamente" aquí significa sin sincronizar, y no se puede ejecutar sin sincronizar en algún hardware. Se aplican las reglas siguientes.

    -   Solo una cola puede escribir en un recurso a la vez.
    -   Varias colas pueden leer desde el recurso siempre y cuando no lean los bytes modificados por el escritor (la lectura de bytes que se escriben simultáneamente genera resultados indefinidos).
    -   Se debe usar una barrera para sincronizar después de escribir antes de que otra cola pueda leer los bytes escritos o realizar cualquier acceso de escritura.

-   Los búferes de reserva que se presentan deben estar en el estado COMMON DE RESOURCE STATE de Direct3D \_ \_ 12. \_ 

## <a name="related-topics"></a>Temas relacionados

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)

[Uso de barreras de recursos para sincronizar estados de recursos en Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Administración de memoria en Direct3D 12](memory-management.md)
