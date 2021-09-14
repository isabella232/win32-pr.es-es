---
title: Single-Threaded Hotel
description: Single-Threaded Hotel
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360166"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Hotel

El uso de departamentos de un solo subproceso (el proceso del modelo de apartamento) ofrece un paradigma basado en mensajes para tratar con varios objetos que se ejecutan simultáneamente. Permite escribir código más eficaz al permitir que un subproceso, mientras espera a que se complete alguna operación que lleva mucho tiempo, permita que se ejecute otro subproceso.

Cada subproceso de un proceso que se inicializa como un proceso de modelo de apartamento y que recupera y envía mensajes de ventana, es un subproceso de apartamento de un solo subproceso. Cada subproceso reside dentro de su propio apartamento. Dentro de un apartamento, los punteros de interfaz se pueden pasar sin serializar y, por lo tanto, todos los objetos de un subproceso de apartamento de un solo subproceso se comunican directamente.

Una agrupación lógica de objetos relacionados que se ejecutan en el mismo subproceso y, por tanto, debe tener una ejecución sincrónica, podría estar en el mismo subproceso de contenedor de un solo subproceso. Sin embargo, un objeto de modelo de apartamento no puede residir en más de un subproceso. Las llamadas a objetos de otros subprocesos deben realizarse en el contexto del subproceso propietario, por lo que com distribuido cambia los subprocesos automáticamente cuando se llama a en un proxy.

Los modelos de interproceso e interproceso son similares. Cuando es necesario pasar un puntero de interfaz a un objeto de otro apartamento (en otro subproceso) dentro del mismo proceso, se usa el mismo modelo de serialización que usan los objetos de distintos procesos para pasar punteros a través de los límites del proceso. Al obtener un puntero al objeto de serialización estándar, puede serializar punteros de interfaz a través de los límites de subprocesos (entre los departamentos) de la misma manera que lo hace entre los procesos. (Los punteros de interfaz se deben serializar cuando se pasan entre los departamentos).

Las reglas para los departamentos de un solo subproceso son sencillas, pero es importante seguirlas cuidadosamente:

-   Todos los objetos deben estar en un único subproceso (dentro de un solo subproceso).
-   Inicialice la biblioteca COM para cada subproceso.
-   Serializa todos los punteros a objetos al pasarlos entre los departamentos.
-   Cada apartamento de un solo subproceso debe tener un bucle de mensajes para controlar las llamadas de otros procesos y departamentos dentro del mismo proceso. Los departamentos de un solo subproceso sin objetos (solo cliente) también necesitan un bucle de mensajes para enviar los mensajes de difusión que algunas aplicaciones usan.
-   Los objetos basados en DLL o en proceso no llaman a las funciones de inicialización COM; en su lugar, registran su modelo de subprocesos con **threadingModel** named-value en la [clave InprocServer32](inprocserver32.md) del Registro. Los objetos que tienen en cuenta los apartamentos también deben escribir los puntos de entrada dll cuidadosamente. Hay consideraciones especiales que se aplican a los servidores en proceso de subprocesos. Para obtener más información, vea [In-Process Server Threading Issues](in-process-server-threading-issues.md).

Aunque varios objetos pueden estar en un único subproceso, ningún objeto de modelo de apartamento puede estar en más de un subproceso.

Cada subproceso de un proceso de cliente o servidor fuera de proceso debe llamar a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)o llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) y especificar COINIT APARTMENTTHREADED para el \_ parámetro *dwCoInit.* El apartamento principal es el subproceso que llama primero **a CoInitializeEx.** Para obtener información sobre los servidores en proceso, vea [In-Process Server Threading Issues](in-process-server-threading-issues.md).

Todas las llamadas a un objeto deben realizarse en su subproceso (dentro de su apartamento). Está prohibido llamar a un objeto directamente desde otro subproceso; el uso de objetos de esta manera sin subprocesos podría causar problemas para las aplicaciones. La implicación de esta regla es que todos los punteros a objetos se deben serializar cuando se pasan entre los departamentos. COM proporciona las dos funciones siguientes para este propósito:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) serializa una interfaz en un objeto de secuencia que se devuelve al autor de la llamada.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) desmarshals un puntero de interfaz de un objeto de secuencia y lo libera.

Estas funciones encapsulan las llamadas a las funciones [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y [**CoUnmarshalInterface,**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) que requieren el uso de la marca \_ INPROC MSHCTX.

En general, COM realiza automáticamente la serialización. Por ejemplo, al pasar un puntero de interfaz como parámetro en una llamada de método en un proxy a un objeto de otro apartamento, o al llamar a [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)COM realiza la serialización automáticamente. Sin embargo, en algunos casos especiales, donde el escritor de aplicaciones pasa punteros de interfaz entre los departamentos sin usar los mecanismos COM normales, el escritor debe controlar la serialización manualmente.

Si un apartamento (Apartment 1) de un proceso tiene un puntero de interfaz y otro apartamento (Apartment 2) requiere su uso, Apartment 1 debe llamar a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) para serializar la interfaz. La secuencia creada por esta función es segura para subprocesos y debe almacenarse en una variable a la que Apartment 2 pueda acceder. Apartment 2 debe pasar esta secuencia a [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) para desmarshal la interfaz y recuperará un puntero a un proxy a través del cual puede acceder a la interfaz. El apartamento principal debe permanecer activo hasta que el cliente haya completado todo el trabajo COM (porque algunos objetos en proceso se cargan en el apartamento principal, como se describe en Problemas de subprocesos del servidor en [proceso).](in-process-server-threading-issues.md) Una vez que se ha pasado un objeto entre subprocesos de esta manera, es muy fácil pasar punteros de interfaz como parámetros. De este modo, COM distribuido realiza la serialización y el cambio de subprocesos para la aplicación.

Para controlar las llamadas de otros procesos y departamentos dentro del mismo proceso, cada apartamento de un solo subproceso debe tener un bucle de mensajes. Esto significa que la función de trabajo del subproceso debe tener un bucle GetMessage/DispatchMessage. Si se usan otras primitivas de sincronización para comunicarse entre subprocesos, la función [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) se puede usar para esperar mensajes y eventos de sincronización de subprocesos. La documentación de esta función tiene un ejemplo de este tipo de bucle de combinación.

COM crea una ventana oculta mediante la Windows clase "OleMainThreadWndClass" en cada contenedor de un solo subproceso. Una llamada a un objeto se recibe como un mensaje de ventana a esta ventana oculta. Cuando el apartamento del objeto recupera y envía el mensaje, la ventana oculta lo recibirá. A continuación, el procedimiento de ventana llamará al método de interfaz correspondiente del objeto .

Cuando varios clientes llaman a un objeto, las llamadas se ponen en cola en la cola de mensajes y el objeto recibirá una llamada cada vez que su apartamento recupere y envíe mensajes. Dado que COM sincroniza las llamadas y las llamadas siempre las entrega el subproceso que pertenece al apartamento del objeto, las implementaciones de interfaz del objeto no necesitan proporcionar sincronización. Los departamentos de un solo subproceso pueden implementar [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para permitir que cancelen llamadas o reciban mensajes de ventana cuando sea necesario.

El objeto se puede volver a escribir si una de sus implementaciones de método de interfaz recupera y envía mensajes o realiza una llamada ORPC a otro subproceso, lo que hace que se entregue otra llamada al objeto (por el mismo apartamento). OLE no impide la reenerción en el mismo subproceso, pero puede ayudar a proporcionar seguridad para subprocesos. Esto es idéntico a la manera en que se puede volver a escribir un procedimiento de ventana si recupera y envía mensajes al procesar un mensaje. Sin embargo, llamar a un servidor de apartamento de un solo subproceso fuera de proceso que llama a otro servidor de apartamento de un solo subproceso permitirá que se vuelva a escribir el primer servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elección del modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Departamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 