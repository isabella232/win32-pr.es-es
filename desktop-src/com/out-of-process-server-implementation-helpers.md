---
title: Aplicaciones auxiliares de implementación de servidor fuera de proceso
description: Aplicaciones auxiliares de implementación de servidor fuera de proceso
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421469"
---
# <a name="out-of-process-server-implementation-helpers"></a>Aplicaciones auxiliares de implementación de servidor fuera de proceso

Hay cuatro funciones auxiliares a las que pueden llamar los servidores fuera de proceso para simplificar el trabajo de escritura de código de servidor. Los clientes COM y los servidores en proceso COM normalmente no los llamarán. Estas funciones están diseñadas para ayudar a evitar condiciones de carrera en la activación del servidor cuando los servidores tienen varios apartamentos o varios objetos de clase. Sin embargo, también se pueden usar con facilidad para servidores de objetos de un solo subproceso y de una sola clase. Las funciones son las siguientes:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Para cerrar correctamente, un servidor COM debe realizar un seguimiento del número de instancias de objeto de las que se ha creado una instancia y el número de veces que se ha llamado al método [**IClassFactory:: lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) . Solo cuando ambos recuentos llegan a cero, se puede apagar un servidor. En los servidores COM de un solo subproceso, la decisión de apagarse se coordinaba con las solicitudes de activación entrantes, que se serializaron en la cola de mensajes. El servidor, al recibir una versión en su instancia de objeto final y decidir cerrarse, revocaría sus objetos de clase antes de que se envíen más solicitudes de activación. Si una solicitud de activación se realizó después de este punto, COM reconocía que los objetos de clase se revocaron y devolvería un error al administrador de control de servicios (SCM), lo que provocaría la ejecución de una nueva instancia del proceso del servidor local.

Sin embargo, en un servidor de modelo de apartamento, en el que los distintos objetos de clase se registran en distintos apartamentos y en todos los servidores de subprocesos libres, esta decisión de apagarse debe coordinarse con solicitudes de activación entre varios subprocesos, de modo que un subproceso del servidor no decida cerrarse mientras otro subproceso del servidor esté ocupado entregando objetos de clase u Un enfoque clásico pero engorroso para solucionar este error consiste en tener el servidor, una vez que haya revocado sus objetos de clase, debe volver a comprobar su recuento de instancias y permanecer activo hasta que se liberen todas las instancias.

Para facilitar a los escritores de servidor la administración de estos tipos de condiciones de carrera, COM proporciona dos funciones de recuento de referencias:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) incrementa un recuento de referencias por proceso global.
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) disminuye el recuento de referencias por proceso global.

Cuando el recuento de referencias por proceso globales llega a cero, COM llama automáticamente a [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects), lo que impide que se produzcan nuevas solicitudes de activación. Después, el servidor puede anular el registro de los distintos objetos de clase de sus distintos subprocesos en tiempo de ocio sin preocuparse de que se pueda entrar en otra solicitud de activación. El SCM administra todas las nuevas solicitudes de activación iniciando una nueva instancia del proceso del servidor local.

La manera más sencilla de que una aplicación de servidor local haga uso de estas funciones es llamar a [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) en el constructor para cada uno de sus objetos de instancia y en cada uno de sus métodos [**IClassFactory:: lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) cuando el parámetro de *rebaño* sea **true**. La aplicación de servidor también debe llamar a [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) en el destructor de cada uno de sus objetos de instancia y en cada uno de sus métodos IClassFactory::**lockserver (** cuando el parámetro de *rebaño* es **false**.

Por último, la aplicación de servidor debe prestar atención al código de retorno de [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)y, si devuelve 0, la aplicación de servidor debe iniciar su limpieza, que, para un servidor con varios subprocesos, normalmente significa que debe señalar sus distintos subprocesos para salir de los bucles de mensajes y llamar a [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) y [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess). Si se usan las funciones de administración de la duración del proceso del servidor, se deben usar tanto en las instancias de objeto como en el método [**lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) . de lo contrario, la aplicación de servidor se puede cerrar prematuramente.

Cuando se realiza una solicitud [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) , com se pone en contacto con el servidor, calcula las referencias de la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) del objeto de clase, vuelve al proceso del cliente, anula la serialización de la interfaz **IClassFactory** y lo devuelve al cliente. En este momento, los clientes suelen llamar a [**lockserver (**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) con **true** para evitar que el proceso del servidor se cierre. Sin embargo, hay una ventana de tiempo entre el momento en el que se calculan las referencias del objeto de clase y el momento en el que el cliente llama a **lockserver (** en el que otro cliente podría conectarse al mismo servidor, obtener una instancia de y liberar esa instancia, lo que provoca que el servidor se apague y deje el primer cliente alto y seco con un puntero **IClassFactory** desconectado. Para evitar esta condición de carrera, COM agrega una llamada implícita a **lockserver (** con **true** al objeto de clase cuando calcula las referencias de la interfaz **IClassFactory** y una llamada implícita a **lockserver (** con **false** cuando el cliente libera la interfaz **IClassFactory** . Por lo tanto, no es necesario volver a **lockserver (** las llamadas remotas al servidor, y el proxy de **Lockserver (** simplemente devuelve S \_ OK sin realmente la comunicación remota de la llamada.

Hay otra condición de carrera relacionada con la activación durante la inicialización de un proceso de servidor fuera de proceso. Un servidor COM que registra varias clases normalmente llama a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con el \_ servidor local REGCLS \_ para cada CLSID que admite. Una vez hecho esto para todas las clases, el servidor entra en su bucle de mensajes. Para un servidor COM de un solo subproceso, todas las solicitudes de activación se bloquean hasta que el servidor entra en el bucle de mensajes. Sin embargo, para un servidor de modelo de apartamento que registra diferentes objetos de clase en distintos apartamentos y para todos los servidores de subprocesamiento libre, las solicitudes de activación pueden llegar antes que esta. En el caso de los servidores de modelo de apartamento, las solicitudes de activación podrían llegar en cuanto cualquier subproceso haya entrado en su bucle de mensajes. En el caso de los servidores de subprocesamiento libre, una solicitud de activación podría llegar en cuanto se registre el primer objeto de clase. Dado que una activación puede producirse esta vez, también es posible que se produzca la versión final (y, por tanto, que el servidor comience a cerrarse) antes de que el resto del servidor haya tenido la oportunidad de finalizar la inicialización.

Para eliminar estas condiciones de carrera y simplificar el trabajo del escritor de servidor, cualquier servidor que desee registrar varios objetos de clase con COM debe llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con el \_ servidor local REGCLS \_ \| REGCLS \_ suspendido para cada CLSID diferente que el servidor admita. Una vez que todas las clases se han registrado y el proceso del servidor está listo para aceptar solicitudes de activación entrantes, el servidor debe realizar una llamada a [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects). Esta función indica a COM que informe al SCM acerca de todas las clases registradas y comienza a permitir las solicitudes de activación en el proceso del servidor. El uso de estas funciones proporciona las siguientes ventajas:

-   Solo se realiza una llamada al SCM, independientemente de cuántos CLSID estén registrados, lo que reduce el tiempo de registro global (y, por tanto, el tiempo de inicio de la aplicación de servidor).
-   Si el servidor tiene varios apartamentos y los distintos CLSID se registran en distintos apartamentos, o si el servidor es un servidor de subprocesamiento libre, no habrá ninguna solicitud de activación hasta que el servidor llame a [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects), lo que proporciona al servidor una oportunidad de registrar todos sus CLSID y establecerla correctamente antes de tener que tratar con las solicitudes de activación y las posibles solicitudes de cierre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 