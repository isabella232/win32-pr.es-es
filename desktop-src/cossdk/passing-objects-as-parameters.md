---
description: Pasar objetos como parámetros
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Pasar objetos como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a58e012138bc65cec481f714ac216bb8227fb924
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965132"
---
# <a name="passing-objects-as-parameters"></a>Pasar objetos como parámetros

El servicio de componentes en cola de COM+ no habilita la cola para todos los componentes COM existentes. Existen restricciones en los tipos de métodos que se pueden poner en cola. Debido a las restricciones de mensajería, los métodos deben cumplir las reglas siguientes:

-   Solo deben contener parámetros de entrada.
-   No deben devolver ningún resultado específico de la aplicación.

Además, hay restricciones en los tipos de parámetros de entrada que se pueden pasar a un componente en cola. En tiempo de ejecución, el servicio de componentes en cola empaqueta los argumentos en el cliente y los pasa al componente de servidor mediante [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). Los tipos simples, como enteros y booleanos, se pueden serializar fácilmente; los tipos más complejos no se pueden serializar sin ayuda.

En el caso de pasar un objeto a través de la llamada de método de un componente en cola como parámetro, el cliente pasa el objeto a la grabadora. La grabadora serializa el objeto en un mensaje de Message Queuing y lo pasa al agente de escucha. Después de que el agente de escucha recoge el mensaje y lo pasa al reproductor, el reproductor debe volver a crear la base del objeto para enviarlo a la llamada al método especificada por el cliente. En función de la duración del cliente y del servidor en un entorno en cola, la implicación es que estos objetos deben poder serializar por valor. Dado que COM+ no proporciona semántica de paso por valor para objetos COM estándar, la grabadora y el reproductor necesitan ayuda del componente para serializar y desmarshal el objeto.

Las referencias de objeto [**que admiten IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) se pueden usar como parámetros para llamar a métodos en componentes en cola. El objeto no puede hacer suposiciones sobre cuándo se volverá a crear. Por ejemplo, es posible que el servidor no esté disponible o que el componente del servidor no se haya iniciado hasta más adelante en el día. Los objetos que no **admiten IPersistStream** devolverán un error.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Objetos persistentes

Microsoft Visual Basic 6 permite crear objetos persistentes. Estos objetos [**admiten IPersistStream y**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) se pueden pasar como parámetros a llamadas a métodos de componentes en cola. Para que Visual Basic objeto se pueda pasar a un componente en cola, se debe inicializar el objeto persistente. Esto se puede hacer de una de las dos maneras siguientes:

-   Si la aplicación que crea el objeto persistente se escribe en Visual Basic, Visual Basic tiempo de ejecución controla automáticamente la inicialización del objeto.
-   Si la aplicación que crea el objeto persistente Visual Basic se escribe en un lenguaje distinto de Visual Basic, como Microsoft Visual C++, la aplicación debe inicializar explícitamente el componente consultando la interfaz [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) del objeto persistente o llamando al método [**IPersistStreamInit::InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)o [**IPersistStream::Load.**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load)

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Conjuntos de registros de ADO OLE DB conjuntos de filas

Pasar objetos de **conjunto** de registros OLE DB ADO entre componentes permite a un componente procesar los resultados de las consultas ejecutadas por otro componente. Esto resulta útil al implementar una aplicación en varios equipos. **Los objetos** de conjunto de registros y conjuntos de filas se pueden pasar como parámetros de método a componentes en cola, con las restricciones siguientes:

-   Los objetos De conjunto **de registros** del lado servidor no se pueden serializar [**mediante IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Solo los objetos De conjunto de **registros del** lado cliente se pueden pasar como parámetros a una llamada al método de componente en cola.
-   Si trabaja directamente con OLE DB, el conjunto OLE DB conjunto de filas debe definirse como un conjunto de filas del lado cliente.

 

 
