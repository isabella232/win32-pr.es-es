---
description: Pasar objetos como parámetros
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Pasar objetos como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a58e012138bc65cec481f714ac216bb8227fb924
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539184"
---
# <a name="passing-objects-as-parameters"></a>Pasar objetos como parámetros

El servicio de componentes en cola COM+ no habilita la puesta en cola para todos los componentes COM existentes. Existen restricciones en los tipos de métodos que se pueden poner en cola. Debido a las restricciones de mensajería, los métodos deben cumplir las siguientes reglas:

-   Solo deben contener parámetros de entrada.
-   No deben devolver ningún resultado específico de la aplicación.

Además, existen restricciones en los tipos de parámetros de entrada que se pueden pasar a un componente en cola. En tiempo de ejecución, el servicio de componentes en cola empaqueta los argumentos en el cliente y los pasa al componente de servidor mediante [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). Los tipos simples, como enteros y booleanos, se pueden serializar fácilmente; no se pueden calcular las referencias de tipos más complejos sin ayuda.

En el caso de pasar un objeto a través de una llamada al método de un componente en cola como parámetro, el cliente pasa el objeto a la grabadora. La grabadora calcula las referencias del objeto en un mensaje de Message Queuing y lo pasa al agente de escucha. Una vez que el agente de escucha recoge el mensaje y lo pasa al reproductor, el reproductor debe crear una instancia del objeto para enviarlo a la llamada al método especificada por el cliente. En función de la duración del cliente y del servidor en un entorno en cola, la implicación es que estos objetos deben ser capaces de calcular las referencias por valor. Dado que COM+ no proporciona la semántica de paso por valor para los objetos COM estándar, la grabadora y el reproductor necesitan ayuda del componente para calcular las referencias del objeto y no calcular las referencias del mismo.

Las referencias de objeto que admiten [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) se pueden usar como parámetros para llamadas a métodos en componentes en cola. El objeto no puede realizar suposiciones sobre cuándo se va a crear una instancia. Por ejemplo, puede que el servidor no esté disponible o que el componente del servidor no se inicie hasta más tarde en el día. Los objetos que no admiten **IPersistStream** devolverán un error.

## <a name="visual-basic-persistable-objects"></a>Visual Basic objetos que se conservan

Microsoft Visual Basic 6 permite crear objetos con persistencia. Estos objetos admiten [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) y se pueden pasar como parámetros a las llamadas a métodos de componentes en cola. Antes de que un objeto de Visual Basic se pueda pasar a un componente en cola, se debe inicializar el objeto que se puede guardar. Esto puede realizarse de una de las dos maneras siguientes:

-   Si la aplicación que crea el objeto persistente se escribe en Visual Basic, el motor en tiempo de ejecución de Visual Basic controla la inicialización del objeto automáticamente.
-   Si la aplicación que crea el Visual Basic objeto con persistencia se escribe en un lenguaje distinto de Visual Basic, como Microsoft Visual C++, la aplicación debe inicializar explícitamente el componente consultando la interfaz [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) del objeto persistente o llamando al método [**IPersistStreamInit:: InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)o [**IPersistStream:: Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) .

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Conjuntos de registros ADO y conjuntos de filas de OLE DB

Pasar objetos de **conjunto** de filas de ADO o OLE DB entre componentes permite que un componente procese los resultados de las consultas ejecutadas por otro componente. Esto resulta útil cuando se implementa una aplicación en varios equipos. Los objetos **Recordset** y Rowset se pueden pasar como parámetros de método a los componentes en cola, con las restricciones siguientes:

-   No se pueden calcular las referencias de los objetos de **conjunto de registros** del lado servidor mediante [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Solo los objetos de **conjunto de registros** del lado cliente se pueden pasar como parámetros a una llamada de método de componente en cola.
-   Si trabaja directamente con OLE DB, el conjunto de filas OLE DB debe definirse como un conjunto de filas del lado cliente.

 

 
