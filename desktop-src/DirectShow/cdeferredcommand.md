---
description: Los comandos diferidos se ponen en cola mediante llamadas a métodos en la interfaz IQueueCommand y se exponen mediante el administrador de gráficos de filtro y algunos filtros.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: Clase CDeferredCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152596"
---
# <a name="cdeferredcommand-class"></a>Clase CDeferredCommand

![jerarquía de clases cdeferredcommand](images/cutil13.png)

Los comandos diferidos se ponen en cola mediante llamadas a métodos en la interfaz [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) y se exponen mediante el administrador de gráficos de filtro y algunos filtros. Una llamada correcta a uno de estos métodos devuelve una interfaz [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) que representa el comando en cola.

Un `CDeferredCommand` objeto representa un único comando diferido y expone la interfaz [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) así como otros métodos que permiten las comprobaciones de tiempo y la ejecución real. Un `CDeferredCommand` objeto contiene una referencia al objeto [**CCmdQueue**](ccmdqueue.md) en el que se pone en cola.

Los recuentos de referencias controlan la duración de la `CDeferredCommand` clase. Cuando se llama a la función miembro [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) , la aplicación que realiza la llamada obtiene un puntero de interfaz que se cuenta como referencia y el objeto [**CCmdQueue**](ccmdqueue.md) también contiene un recuento de referencias en el comando diferido. La llamada a la función miembro [**IDeferredCommand:: CANCEL**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) toma el comando diferido de la cola de comandos y, por tanto, reduce el recuento de referencias en uno. Una vez desaprovechada la cola, el comando no se puede volver a colocar en la cola.



| Miembros de datos protegidos                                        | Descripción                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Marca de [**tiempo de secuencia**](stream-time.md) o tiempo de presentación. que se va a pasar al método invocado.                   |
| envío de m \_                                                   | Obtiene acceso a la interfaz **ITypeInfo** .                                                                                   |
| m \_ dispidMethod                                               | Método de la interfaz que se va a ejecutar.                                                                                         |
| m \_ DispParams                                                 | Objeto [**CDispParams**](cdispparams.md) que contiene la lista de parámetros **DISPPARAMS**                                  |
| m \_ hrResult                                                   | Almacena el valor **HRESULT** devuelto.                                                                                  |
| \_IID m                                                        | Identificador único global (**GUID**) de la interfaz.                                                                 |
| m \_ pQueue                                                     | Puntero al objeto [**CCmdQueue**](ccmdqueue.md) que expone la interfaz [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . |
| m \_ pUnk                                                       | **IUnknown** puntero a la interfaz en la que se ejecutará el comando.                                                 |
| m \_ pvarResult                                                 | Información resultante, si existe, del método invocado.                                                                 |
| m \_ hora                                                       | Hora a la que se ejecutará el comando.                                                                                  |
| m \_ wFlags                                                     | Marcas que especifican el contexto de la invocación.                                                                         |
| Funciones de miembro                                              | Descripción                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Construye un objeto **CDeferredCommand** .                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Recupera las marcas de contexto asociadas al comando aplazado.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Recupera el identificador de interfaz (IID) de la interfaz en la que se ejecutará el método.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Recupera el identificador de envío del método que se va a ejecutar.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Recupera la lista de argumentos **DISPPARAMS** para el método.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Recupera la lista de argumentos resultante, si existe.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Recupera la hora a la que se ejecutará el método.                                                                         |
| [**Invocar**](cdeferredcommand-invoke.md)                     | Proporciona acceso a los métodos y propiedades expuestos por un objeto.                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Especifica si el comando se va a ejecutar en el momento de la secuencia o en el tiempo de presentación.                                         |
| Métodos IDeferredCommand                                      | Descripción                                                                                                             |
| [**Cancelar**](cdeferredcommand-cancel.md)                     | Cancela una solicitud [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) previamente puesta en cola.                        |
| [**Confianza**](cdeferredcommand-confidence.md)             | No implementado actualmente.                                                                                              |
| [**Posponer**](cdeferredcommand-postpone.md)                 | Especifica un nuevo tiempo de presentación para un comando en cola previamente.                                                      |
| [**Gethresult (**](cdeferredcommand-gethresult.md)             | Recupera el valor **HRESULT** del método invocado.                                                                  |



 

 

 



