---
description: El servicio eventos COM+ usa un objeto de clase de eventos para administrar la conexión entre el publicador y el suscriptor.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: El objeto de clase de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5650969895cdfa63f07e6ba77e617a962335101d4f56aeb21a5b439b27daaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546157"
---
# <a name="the-com-event-class-object"></a>El objeto de clase de eventos COM+

El servicio eventos COM+ usa un objeto *de clase de eventos* para administrar la conexión entre el publicador y el suscriptor. El objeto de clase de eventos es un componente com+ administrado y almacenado por el sistema de eventos COM+ y contiene las interfaces y los métodos usados por un publicador para los eventos. Es un objeto persistente que indica los eventos que pueden producirse y, opcionalmente, identifica el publicador. Especifique las interfaces y los métodos que desea que contenga una clase de eventos proporcionando una biblioteca de tipos.

Para generar un evento, el publicador crea una instancia del objeto de clase de evento llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o al método **CreateObject** de Microsoft Visual Basic y solicitando que se devuelva la interfaz de eventos. El objeto de clase de eventos con instancias contiene la implementación del sistema de eventos de la interfaz solicitada. Un suscriptor interesado también debe implementar la interfaz de clase de eventos para recibir eventos de un publicador determinado. Cuando se crea una instancia del objeto de clase de eventos, el sistema de eventos lo asocia a los suscriptores adecuados. La lista de suscriptores se mantiene durante la vigencia del objeto de clase de eventos. Un evento se puede entregar a varios suscriptores en serie o en paralelo.

Al implementar un objeto de clase de eventos, debe proporcionar un archivo DLL de registro propio que exporte las funciones [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer.**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) La **función DllRegisterServer** registra una clase COM y la **función DllUnregisterServer** anula el registro del componente. Los objetos de clase de evento se almacenan en el catálogo de COM+, ya sea mediante la herramienta de administración servicios de componentes o mediante programación mediante los métodos de las interfaces [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) o [**ICOMAdminCatalog::InstallMultipleEventClasses.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) Para obtener información detallada sobre el registro de objetos de clase de eventos, vea [Registrar una clase de eventos](registering-an-event-class.md).

Dado que los objetos de clase de eventos son componentes configurados, se pueden configurar otros atributos, como la cola, las transacciones, la seguridad, entre otros, mediante la herramienta de administración servicios de componentes o las funciones del SDK administrativo de COM+.

> [!Note]  
> El servicio eventos COM+ usa la serialización de biblioteca de tipos. Esto coloca algunas restricciones en las interfaces de clase de eventos. Por ejemplo, el serializador de biblioteca de tipos no admite el tamaño de los atributos MIDL [**\_ es**](/windows/desktop/Midl/size-is) y [**la longitud \_ es**](/windows/desktop/Midl/length-is).

 

Un objeto de clase de eventos posee atributos de publicación que determinan la forma en que se publican los eventos, así como las propiedades siguientes:

-   **EventCLSID**. Identificador único que especifica el CLSID del componente.
-   **EventClassName**. Identificador único que especifica el PROGID del componente.
-   **TypeLibrary**. Proporciona una lista de interfaces que ofrece el objeto de clase de eventos. No es necesario implementar las interfaces de activación especificadas en la biblioteca de tipos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicación y entrega de eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[Uso de eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
