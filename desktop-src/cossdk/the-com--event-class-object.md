---
description: El servicio de eventos COM+ utiliza un objeto de clase de eventos para administrar la conexión entre el publicador y el suscriptor.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Objeto de la clase de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae397f647354ac24395fa073365160829a687a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000566"
---
# <a name="the-com-event-class-object"></a>Objeto de la clase de eventos COM+

El servicio de eventos COM+ utiliza un *objeto de clase de eventos* para administrar la conexión entre el publicador y el suscriptor. El objeto de clase de eventos es un componente COM+ administrado y almacenado por el sistema de eventos COM+ y contiene las interfaces y los métodos utilizados por un publicador para activar eventos. Es un objeto persistente que indica los eventos que pueden producirse y, opcionalmente, identifica al publicador. Especifique las interfaces y los métodos que desea que contenga una clase de eventos proporcionando una biblioteca de tipos.

Para desencadenar un evento, el publicador crea instancias del objeto de la clase de evento llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o el método **CreateObject** de Microsoft Visual Basic y solicitando la interfaz de eventos que se va a devolver. El objeto de clase de eventos con instancias contiene la implementación del sistema de eventos de la interfaz solicitada. Un suscriptor interesado también debe implementar la interfaz de clase de eventos para recibir eventos de un publicador determinado. Cuando se crea una instancia del objeto de la clase de evento, el sistema de eventos lo asocia a los suscriptores correspondientes. La lista de suscriptores se mantiene durante la vigencia del objeto de la clase de evento. Un evento se puede entregar a varios suscriptores, ya sea en serie o en paralelo.

Al implementar un objeto de clase de eventos, debe proporcionar un archivo DLL de registro automático que exporte las funciones [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) . La función **DllRegisterServer** registra una clase com y la función **DllUnregisterServer** anula el registro del componente. Los objetos de la clase de eventos se almacenan en el catálogo de COM+, ya sea mediante la herramienta de administración de servicios de componentes o mediante programación con los métodos de las interfaces [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) o [**ICOMAdminCatalog:: InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) . Para obtener información detallada sobre el registro de objetos de clase de eventos, vea [registrar una clase de eventos](registering-an-event-class.md).

Dado que los objetos de la clase de eventos son componentes configurados, otros atributos, como la puesta en cola, las transacciones, la seguridad, etc., se pueden configurar para ellos mediante la herramienta de administración de servicios de componentes o las funciones del SDK administrativo de COM+.

> [!Note]  
> El servicio de eventos COM+ utiliza el cálculo de referencias de la biblioteca de tipos. Esto coloca algunas restricciones en las interfaces de clase de eventos. Por ejemplo, el contador de referencias de la biblioteca de tipos no admite el tamaño de los atributos MIDL y la [**longitud \_ es**](/windows/desktop/Midl/length-is). [**\_**](/windows/desktop/Midl/size-is)

 

Un objeto de clase de eventos posee atributos de publicación que determinan la manera en que se publican los eventos, así como las propiedades siguientes:

-   **EventCLSID**. Identificador único que especifica el CLSID del componente.
-   **EventClassName**. Identificador único que especifica el PROGID del componente.
-   **Biblioteca**. Proporciona una lista de interfaces ofrecidas por el objeto de la clase de evento. No es necesario implementar las interfaces de activación especificadas en la biblioteca de tipos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad de eventos COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[Usar eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
