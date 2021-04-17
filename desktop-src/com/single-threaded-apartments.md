---
title: Single-Threaded apartamentos
description: Single-Threaded apartamentos
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421450"
---
# <a name="single-threaded-apartments"></a>Single-Threaded apartamentos

El uso de apartamentos de un solo subproceso (el proceso del modelo de apartamento) ofrece un paradigma basado en mensaje para tratar varios objetos que se ejecutan simultáneamente. Permite escribir código más eficaz permitiendo que un subproceso, mientras espera que se complete una operación que consume mucho tiempo, para permitir la ejecución de otro subproceso.

Cada subproceso de un proceso que se inicializa como un proceso de modelo de apartamento, y que recupera y envía mensajes de ventana, es un subproceso de apartamento de un solo subproceso. Cada subproceso reside en su propio apartamento. Dentro de un contenedor, los punteros de interfaz se pueden pasar sin serialización y, por tanto, todos los objetos de un subproceso de apartamento de un solo subproceso se comunican directamente.

Una agrupación lógica de objetos relacionados que todos se ejecutan en el mismo subproceso y, por tanto, debe tener una ejecución sincrónica, puede residir en el mismo subproceso de apartamento de un solo subproceso. Sin embargo, un objeto de modelo de apartamento no puede residir en más de un subproceso. Las llamadas a objetos de otros subprocesos deben realizarse en el contexto del subproceso propietario, por lo que los subprocesos COM distribuidos automáticamente cambian automáticamente cuando se llama a en un proxy.

Los modelos de interproceso e interthread son similares. Cuando es necesario pasar un puntero de interfaz a un objeto de otro apartamento (en otro subproceso) dentro del mismo proceso, se usa el mismo modelo de serialización que los objetos de diferentes procesos utilizan para pasar punteros a través de los límites del proceso. Al obtener un puntero al objeto de serialización estándar, puede calcular las referencias de los punteros de interfaz a través de los límites de subprocesos (entre apartamentos) de la misma manera que lo hace entre los procesos. (Se deben calcular las referencias de los punteros de interfaz cuando se pasan entre apartamentos).

Las reglas para apartamentos de un solo subproceso son sencillas, pero es importante seguirlos con cuidado:

-   Cada objeto debe residir en un único subproceso (dentro de un contenedor uniproceso).
-   Inicialice la biblioteca COM para cada subproceso.
-   Calcular las referencias de todos los punteros a objetos al pasarlos entre apartamentos.
-   Cada apartamento de un solo subproceso debe tener un bucle de mensajes para controlar las llamadas de otros procesos y apartamentos dentro del mismo proceso. Los apartamentos de un solo subproceso sin objetos (solo cliente) también necesitan un bucle de mensajes para enviar los mensajes de difusión que usan algunas aplicaciones.
-   Los objetos basados en DLL o en proceso no llaman a las funciones de inicialización de COM; en su lugar, registran su modelo de subprocesos con el valor de **ThreadingModel** denominado-Value bajo la clave [InProcServer32](inprocserver32.md) en el registro. Los objetos que reconocen el apartamento también deben escribir cuidadosamente puntos de entrada de DLL. Existen consideraciones especiales que se aplican a los subprocesos de los servidores en proceso. Para obtener más información, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).

Mientras que varios objetos pueden residir en un único subproceso, ningún objeto de modelo de apartamento puede residir en más de un subproceso.

Cada subproceso de un proceso de cliente o servidor fuera de proceso debe llamar a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize), o llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) y especificar coinit \_ APARTMENTTHREADED para el parámetro *dwCoInit* . El apartamento principal es el subproceso que llama a **CoInitializeEx** en primer lugar. Para obtener información sobre los servidores en proceso, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).

Todas las llamadas a un objeto deben realizarse en su subproceso (dentro de su apartamento). Está prohibido llamar a un objeto directamente desde otro subproceso. el uso de objetos en este modo de subprocesamiento libre podría causar problemas en las aplicaciones. La implicación de esta regla es que se deben calcular las referencias de todos los punteros a objetos cuando se pasan entre apartamentos. COM proporciona las dos funciones siguientes para este propósito:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) calcula las referencias de una interfaz en un objeto de flujo que se devuelve al autor de la llamada.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) no calcula las referencias de un puntero de interfaz desde un objeto de flujo y lo libera.

Estas funciones ajustan las llamadas a las funciones [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , que requieren el uso de la \_ marca INPROC MSHCTX.

En general, COM realiza automáticamente el cálculo de referencias. Por ejemplo, cuando se pasa un puntero de interfaz como un parámetro en una llamada de método en un proxy a un objeto de otro apartamento, o cuando se llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), com realiza el cálculo de referencias automáticamente. Sin embargo, en algunos casos especiales, en los que el escritor de la aplicación está pasando punteros de interfaz entre apartamentos sin usar los mecanismos COM normales, el escritor debe controlar manualmente el cálculo de referencias.

Si un contenedor (Apartamento 1) de un proceso tiene un puntero de interfaz y otro apartamento (Apartamento 2) requiere su uso, el apartamento 1 debe llamar a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) para calcular las referencias de la interfaz. La secuencia que se crea mediante esta función es segura para subprocesos y debe almacenarse en una variable a la que pueda acceder el apartamento 2. El Apartamento 2 debe pasar esta secuencia a [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) para anular la serialización de la interfaz y devolverá un puntero a un proxy a través del cual puede acceder a la interfaz. El apartamento principal debe permanecer activo hasta que el cliente haya completado todo el trabajo COM (porque algunos objetos en curso se cargan en el apartamento principal, como se describe en [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)). Una vez que se ha pasado un objeto entre subprocesos de esta manera, es muy fácil pasar punteros de interfaz como parámetros. De este modo, COM distribuido realiza las referencias y el cambio de subprocesos de la aplicación.

Para controlar las llamadas de otros procesos y apartamentos dentro del mismo proceso, cada apartamento de un solo subproceso debe tener un bucle de mensajes. Esto significa que la función de trabajo del subproceso debe tener un bucle GetMessage/DispatchMessage. Si se usan otras primitivas de sincronización para la comunicación entre subprocesos, la función [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) se puede usar para esperar tanto los mensajes como los eventos de sincronización de subprocesos. La documentación de esta función tiene un ejemplo de este tipo de bucle de combinación.

COM crea una ventana oculta mediante la clase de Windows "OleMainThreadWndClass" en cada apartamento de un solo subproceso. Se recibe una llamada a un objeto como un mensaje de ventana en esta ventana oculta. Cuando el apartamento del objeto recupera y envía el mensaje, la ventana oculta lo recibirá. A continuación, el procedimiento de ventana llamará al método de interfaz correspondiente del objeto.

Cuando varios clientes llaman a un objeto, las llamadas se ponen en cola en la cola de mensajes y el objeto recibirá una llamada cada vez que su apartamento recupere y envíe mensajes. Dado que COM sincroniza las llamadas y las llamadas siempre se entregan mediante el subproceso que pertenece al apartamento del objeto, las implementaciones de interfaz del objeto no necesitan realizar la sincronización. Los apartamentos de un solo subproceso pueden implementar [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para permitirles cancelar llamadas o recibir mensajes de ventana cuando sea necesario.

El objeto se puede volver a escribir si una de sus implementaciones de método de interfaz recupera y envía mensajes o realiza una llamada ORPC a otro subproceso, lo que provoca que se entregue otra llamada al objeto (por el mismo apartamento). OLE no impide la reentrada en el mismo subproceso, pero puede ayudar a proporcionar seguridad para subprocesos. Es idéntico a la forma en que se puede volver a escribir un procedimiento de ventana si recupera y envía mensajes mientras procesa un mensaje. Sin embargo, si se llama a un servidor de apartamento de un solo subproceso fuera de proceso que llama a otro servidor de apartamento de un solo subproceso, permitirá que se vuelva a escribir el primer servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elegir el modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Apartamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 