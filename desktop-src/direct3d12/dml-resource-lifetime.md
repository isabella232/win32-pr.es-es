---
title: Duración y sincronización de los recursos
description: Para evitar un comportamiento no definido, la aplicación DirectML debe administrar correctamente la duración de los objetos y la sincronización entre la CPU y la GPU.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104579"
---
# <a name="resource-lifetime-and-synchronization"></a>Duración y sincronización de los recursos

Al igual que con Direct3D 12, la aplicación DirectML debe (con el fin de evitar un comportamiento no definido) administrar correctamente la duración de los objetos y la sincronización entre la CPU y la GPU. DirectML sigue un modelo de duración de recursos idéntico al de Direct3D 12.

- Las dependencias de duración entre dos objetos de CPU se mantienen mediante DirectML con recuentos de referencias seguros. La aplicación no tiene que administrar manualmente las dependencias de la duración de la CPU. Por ejemplo, cada elemento secundario de dispositivo contiene una referencia segura a su dispositivo primario.
- Las dependencias de duración entre los objetos &mdash; de GPU o las dependencias que abarcan entre la CPU y la GPU &mdash; no se administran automáticamente. Es responsabilidad de la aplicación asegurarse de que los recursos de GPU viven al menos hasta que todo el trabajo que usa ese recurso ha completado la ejecución en la GPU.

## <a name="directml-devices"></a>Dispositivos DirectML

El dispositivo DirectML es un objeto de generador sin estado seguro para subprocesos. Cada dispositivo secundario (consulte [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) contiene una referencia segura a su dispositivo DirectML primario (consulte [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice)). Esto significa que siempre puede recuperar la interfaz de dispositivo primaria desde cualquier interfaz secundaria del dispositivo.

A su vez, un dispositivo DirectML mantiene una referencia segura al dispositivo de Direct3D 12 que se usó para crearlo (vea [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)e interfaces derivadas).

Dado que el dispositivo DirectML no tiene estado, es seguro para subprocesos implícitamente. Puede llamar a métodos en el dispositivo DirectML desde varios subprocesos de forma simultánea sin necesidad de sincronización externa.

Sin embargo, a diferencia del dispositivo Direct3D 12, el dispositivo DirectML no es un objeto singleton. Puede crear tantos dispositivos DirectML como desee. Sin embargo, no puede mezclar y hacer coincidir los elementos secundarios de los dispositivos que pertenecen a distintos dispositivos. Por ejemplo, [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) y [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) son dos tipos de elementos secundarios del dispositivo (ambas interfaces derivan directa o indirectamente de **IDMLDeviceChild**). Y no puede usar una tabla de enlace (**IDMLBindingTable**) para enlazar un operador (**IDMLCompiledOperator**) si el operador y la tabla de enlace pertenecen a distintas instancias de dispositivo DirectML.

Dado que el dispositivo DirectML no es un singleton, la eliminación del dispositivo se produce por dispositivo, en lugar de ser un evento en todo el proceso, como es para un dispositivo Direct3D 12. Para obtener más información, consulte [control de errores y eliminación de dispositivos en DirectML](dml-errors.md).

## <a name="lifetime-requirements-of-gpu-resources"></a>Requisitos de duración de los recursos de GPU

Como Direct3D 12, DirectML no se sincroniza automáticamente entre la CPU y la GPU; tampoco mantiene los recursos activos automáticamente mientras están en uso en la GPU. En su lugar, estas son las responsabilidades de la aplicación.

Al ejecutar una lista de comandos que contiene distribuciones de DirectML, la aplicación debe asegurarse de que los recursos de la GPU se mantienen activos hasta que todo el trabajo que usa esos recursos ha completado la ejecución en la GPU.

En el caso de [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) para un operador DirectML, que incluye los siguientes objetos.

- [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) que se está ejecutando (o [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) en su lugar, si se realiza la inicialización del operador).
- **IDMLCompiledOperator** que respalda la tabla de enlace que se usa para enlazar el operador.
- Los objetos [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) enlazados como entradas/salidas del operador.
- Los objetos **ID3D12Resource** enlazados como recursos persistentes y temporales, si procede.
- [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) que respalda la propia lista de comandos.

No todas las interfaces DirectML representan recursos de GPU. Por ejemplo, *no* es necesario mantener activa una tabla de enlace hasta que todos los envíos que lo usan hayan completado su ejecución en la GPU. Esto se debe a que la tabla de enlace no posee ningún recurso de GPU. En su lugar, el montón de descriptores sí lo hace. Por lo tanto, el *montón descriptor* subyacente es el objeto que debe mantenerse activo hasta que se complete la ejecución y no la tabla de enlace.

Existe un concepto similar en Direct3D 12. Un *asignador* de comandos debe mantenerse activo hasta que todas las ejecuciones que lo usen se hayan completado en la GPU; puesto que posee la memoria de la GPU. Pero una *lista* de comandos no posee la memoria de la GPU, por lo que se puede restablecer o liberar en cuanto se envíe para su ejecución.

En DirectML, los operadores compilados ([**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) y los inicializadores de operador ([**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) poseen directamente recursos de GPU, por lo que deben mantenerse activos hasta que todos los envíos que los usen hayan completado su ejecución en la GPU. Además, cualquier recurso de Direct3D 12 que se use (asignadores de comandos, montones de descriptores, búferes, como ejemplos) debe mantenerse activo de forma similar en la aplicación.

Si se libera prematuramente un objeto mientras está siendo utilizado por la GPU, el resultado es un comportamiento indefinido, que tiene la posibilidad de producir la eliminación del dispositivo u otros errores.

## <a name="cpu-and-gpu-synchronization"></a>Sincronización de CPU y GPU

DirectML no envía ningún trabajo para su ejecución en la GPU. En su lugar, el [método **IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) *registra* el envío de ese trabajo en una lista de comandos para su ejecución posterior. A continuación, la aplicación debe cerrar y enviar la lista de comandos para su ejecución mediante una llamada a [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists), como con cualquier lista de comandos de Direct3D 12.

Dado que DirectML no envía ningún trabajo para su ejecución en la GPU, tampoco crea ninguna barrera ni realiza ninguna forma de sincronización de CPU/GPU en su nombre. Es responsabilidad de la aplicación usar las primitivas de Direct3D 12 adecuadas para esperar a que el trabajo enviado complete su ejecución en la GPU, si es necesario. Para obtener más información, vea [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) y [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal).

## <a name="see-also"></a>Consulte también

* [Ejecutar y sincronizar listas de comandos](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [Control de errores y eliminación de dispositivos en DirectML](dml-errors.md)