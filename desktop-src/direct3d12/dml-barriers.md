---
title: Barreras de UAV y barreras de estado de recursos en DirectML
description: Describe las ventajas de la corrección de barreras y cómo puede trabajar con ellas en DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104549119"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>Barreras de UAV y barreras de estado de recursos en DirectML

## <a name="unordered-access-view-uav-barrier-requirements"></a>Requisitos de barrera de la vista de acceso desordenado (UAV)

### <a name="uav-barriers-in-direct3d-12"></a>Barreras UAV en Direct3D 12

En Direct3D 12, las distribuciones adyacentes del sombreador de cálculo dentro de la misma lista de comandos tienen permiso para ejecutarse en paralelo en la GPU, a menos que estén sincronizadas con una barrera de vista de acceso no ordenada (UAV) que intervenga. Esto puede mejorar el rendimiento al aumentar el uso del hardware de la GPU. Sin embargo, de forma predeterminada, sin el uso de una barrera UAV, la ejecución en paralelo de dos distribuidores adyacentes puede producir una condición de carrera si existe una dependencia de datos entre los dos envíos; o bien, si ambos envíos realizan escrituras UAV en las mismas regiones de memoria.

Una barrera UAV obliga a que todas las distribuciones enviadas previamente completen ejecución en la GPU antes de que puedan comenzar los envíos posteriores. Las barreras de UAV se usan para sincronizar los envíos en la misma lista de comandos para evitar carreras de datos. Puede emitir una barrera UAV mediante el [método **ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

### <a name="uav-barriers-in-directml"></a>Barreras de UAV en DirectML

En DirectML, los operadores se envían de una manera similar a la forma en que se envían los sombreadores de cálculo en Direct3D 12. Es decir, se permite que se ejecuten en paralelo los envíos de operadores adyacentes en la GPU, a menos que exista una barrera UAV intermedia entre ellos. Un modelo de aprendizaje automático típico contiene dependencias de datos entre sus operadores; por ejemplo, la salida de un operador se alimenta en la entrada de otro. Por lo tanto, es importante usar barreras UAV para sincronizar correctamente los envíos.

DirectML garantiza que solo se leerán los datos de entrada (y nunca se escribirán). También garantiza que nunca fabricará escrituras en un tensores de salida fuera del intervalo del miembro [**DML_BUFFER_TENSOR_DESC:: TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) de la tensores. Esto significa que se puede hacer referencia a las dependencias de datos entre los operadores de DirectML mirando solo en los enlaces de entrada y salida de un operador.

Por ejemplo, estas garantías permiten enviar dos operadores que enlazan la misma región de un recurso como entrada, sin tener que emitir una barrera UAV intermedia. Esto siempre es seguro porque DirectML nunca escribe en los datos de entrada. Otro ejemplo sería que siempre es seguro enlazar los decenas de dos operadores simultáneos al mismo recurso de Direct3D 12 (siempre y cuando sus decenas no se superpongan), ya que DirectML nunca escribe fuera de los límites de un tensores (tal y como se define en **DML_BUFFER_TENSOR_DESC:: TotalTensorSizeInBytes**) de tensores.

Como las barreras de UAV son una forma de sincronización, el uso innecesario de barreras de UAV puede afectar negativamente al rendimiento. Por lo tanto, es mejor usar el número mínimo de barreras UAV necesarias para sincronizar correctamente los envíos dentro de una lista de comandos.

### <a name="example-1"></a>Ejemplo 1

En el ejemplo siguiente, la salida del operador de circunvolución se introduce en una activación de ReLU, seguida de una normalización por lotes.

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

Dado que existe una dependencia de datos entre los tres operadores, necesitará una barrera UAV entre cada envío sucesivo (consulte [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barrera UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**Barrera UAV**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`

### <a name="example-2"></a>Ejemplo 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

Aquí, la salida de la agrupación se introduce en dos convolución, cuyas salidas se concatenan con el operador de combinación. Existe una dependencia de datos entre y y, así como `pool1` `conv1` `conv2` entre y y `conv1` `conv2` `join1` . Esta es una manera válida de ejecutar este gráfico.

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barrera UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**Barrera UAV**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`

En este caso, `conv1` y pueden `conv2` ejecutarse simultáneamente en la GPU, lo que puede mejorar el rendimiento.

## <a name="resource-barrier-state-requirements"></a>Requisitos de estado de barrera de recursos

Como autor de la llamada, es su responsabilidad asegurarse de que todos los recursos de Direct3D 12 se encuentran en el estado de barrera de recursos correcto antes de ejecutar los envíos de DirectML en la GPU. DirectML no realiza ninguna barrera de transición en su nombre.

Antes de la ejecución de [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) en la GPU, debe pasar todos los recursos enlazados al estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** , o a un estado que se pueda promover implícitamente a **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, como **D3D12_RESOURCE_STATE_COMMON**. Una vez finalizada esta llamada, los recursos permanecen en el estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . Para obtener más información, vea [Binding in DirectML](dml-binding.md).

## <a name="see-also"></a>Consulte también

* [Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [Enlaces en DirectML](dml-binding.md)
