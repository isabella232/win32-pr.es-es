---
description: Los comandos diferidos se ponen en cola mediante llamadas a métodos en la interfaz IQueueCommand y se exponen mediante el administrador de gráficos de filtros y algunos filtros.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: CDeferredCommand (clase)
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
ms.openlocfilehash: 3413deb3c606177c937aef72a8437769dc2a97acdcbee97200880c96f36f9fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910054"
---
# <a name="cdeferredcommand-class"></a>CDeferredCommand (clase)

![jerarquía de clases cdeferredcommand](images/cutil13.png)

Los comandos diferidos se ponen en cola mediante llamadas a métodos en la interfaz [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) y se exponen mediante el administrador de gráficos de filtros y algunos filtros. Una llamada correcta a uno de estos métodos devuelve una [**interfaz IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) que representa el comando en cola.

Un objeto representa un único comando diferido y expone la interfaz `CDeferredCommand` [**IDeferredCommand,**](/windows/desktop/api/Control/nn-control-ideferredcommand) así como otros métodos que permiten comprobaciones de tiempo y ejecución real. Un `CDeferredCommand` objeto contiene una referencia al objeto [**CCmdQueue**](ccmdqueue.md) en el que se pone en cola.

Los recuentos de referencias controlan la duración de la `CDeferredCommand` clase. Al llamar a la función miembro [**CDeferredCommand::Invoke,**](cdeferredcommand-invoke.md) la aplicación que realiza la llamada obtiene un puntero de interfaz con recuento de referencias y el objeto [**CCmdQueue**](ccmdqueue.md) también contiene un recuento de referencias en el comando diferido. Al llamar a la función miembro [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) se quita el comando diferido de la cola de comandos y, por tanto, se reduce el recuento de referencias en uno. Una vez que se ha quitado de la cola, el comando no se puede volver a colocar en la cola.



| Miembros de datos protegidos                                        | Descripción                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Marca para el [**tiempo de transmisión o**](stream-time.md) el tiempo de presentación. que se va a pasar al método invocado.                   |
| m \_ Dispatch                                                   | Tiene acceso a **la interfaz ITypeInfo.**                                                                                   |
| m \_ dispidMethod                                               | Método en la interfaz que se ejecutará.                                                                                         |
| m \_ DispParams                                                 | [**Objeto CDispParams**](cdispparams.md) que contiene la **lista de parámetros DIS DISRAMS**                                  |
| m \_ hrResult                                                   | Almacena el valor **HRESULT** devuelto.                                                                                  |
| m \_ iid                                                        | Identificador único global **(GUID)** de la interfaz.                                                                 |
| m \_ pQueue                                                     | Puntero al objeto [**CCmdQueue**](ccmdqueue.md) que expone la [**interfaz IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand) |
| m \_ pUnk                                                       | **Puntero IUnknown** a la interfaz en la que se ejecutará el comando.                                                 |
| m \_ pvarResult                                                 | Información resultante, si existe, del método invocado.                                                                 |
| m \_ time                                                       | Hora en la que se ejecutará el comando.                                                                                  |
| m \_ wFlags                                                     | Marcas que especifican el contexto de la invocación.                                                                         |
| Funciones de miembro                                              | Descripción                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Construye un **objeto CDeferredCommand.**                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Recupera las marcas de contexto asociadas al comando aplazado.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Recupera el identificador de interfaz (IID) de la interfaz en la que se ejecutará el método.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Recupera el identificador de envío del método que se va a ejecutar.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Recupera la lista **de argumentos DIS DIS DIRAMS** en el método .                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Recupera la lista de argumentos resultante, si existe alguna.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Recupera la hora a la que se ejecutará el método.                                                                         |
| [**Invocar**](cdeferredcommand-invoke.md)                     | Proporciona acceso a métodos y propiedades expuestos por un objeto .                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Especifica si el comando se va a ejecutar en tiempo de transmisión o en tiempo de presentación.                                         |
| Métodos IDeferredCommand                                      | Descripción                                                                                                             |
| [**Cancelar**](cdeferredcommand-cancel.md)                     | Cancela una solicitud [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) en cola anterior.                        |
| [**Confianza**](cdeferredcommand-confidence.md)             | No implementado actualmente.                                                                                              |
| [**Posponer**](cdeferredcommand-postpone.md)                 | Especifica un nuevo tiempo de presentación para un comando que se ha puesto en cola anteriormente.                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | Recupera el **valor HRESULT** del método invocado.                                                                  |



 

 

 



