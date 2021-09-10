---
title: Asistentes de implementación del servidor fuera de proceso
description: Asistentes de implementación del servidor fuera de proceso
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369496"
---
# <a name="out-of-process-server-implementation-helpers"></a>Asistentes de implementación del servidor fuera de proceso

Hay cuatro funciones auxiliares a las que pueden llamar los servidores fuera de proceso para simplificar el trabajo de escritura del código del servidor. Los clientes COM y los servidores en proceso COM normalmente no los llamarían. Estas funciones están diseñadas para ayudar a evitar condiciones de carrera en la activación del servidor cuando los servidores tienen varios departamentos o varios objetos de clase. Sin embargo, también se pueden usar fácilmente para servidores de objetos de una sola clase y de un solo subproceso. Las funciones son las siguientes:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Para apagar correctamente, un servidor COM debe realizar un seguimiento de cuántas instancias de objeto ha instancias y cuántas veces se ha llamado a su método [**IClassFactory::LockServer.**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) Solo cuando ambos recuentos alcanzan cero se puede apagar un servidor. En los servidores COM de un solo subproceso, la decisión de cerrar se coordine con las solicitudes de activación entrantes, serializadas por la cola de mensajes. El servidor, tras recibir una versión en su instancia de objeto final y decidir apagarse, revocaría sus objetos de clase antes de enviar más solicitudes de activación. Si se produjo una solicitud de activación después de este punto, COM reconocería que se revocaron los objetos de clase y devolvería un error al Administrador de control de servicios (SCM), lo que provocaría que se ejecutara una nueva instancia del proceso de servidor local.

Sin embargo, en un servidor de modelo de contenedor, en el que se registran objetos de clase diferentes en diferentes departamentos y en todos los servidores de subprocesos libres, esta decisión de apagar debe coordinarse con las solicitudes de activación en varios subprocesos para que un subproceso del servidor no decida apagarse mientras otro subproceso del servidor está ocupado entregando objetos de clase o instancias de objeto. Un enfoque clásico pero complicado para resolver esto es hacer que el servidor, después de revocar sus objetos de clase, vuelva a comprobar su recuento de instancias y permanezca activo hasta que se hayan liberado todas las instancias.

Para facilitar a los escritores de servidores el control de estos tipos de condiciones de carrera, COM proporciona dos funciones de recuento de referencias:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) incrementa un recuento global de referencias por proceso.
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) disminuye el recuento global de referencias por proceso.

Cuando el recuento global de referencias por proceso alcanza cero, COM llama automáticamente a [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects), lo que impide que lleguen nuevas solicitudes de activación. A continuación, el servidor puede anular el registro de sus distintos objetos de clase de sus distintos subprocesos sin preocuparse de que pueda entrar otra solicitud de activación. Por lo tanto, todas las nuevas solicitudes de activación se controlan mediante el SCM que inicia una nueva instancia del proceso de servidor local.

La manera más sencilla de que una aplicación de servidor local use estas funciones es llamar a [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) en el constructor para cada uno de sus objetos de instancia y en cada uno de sus métodos [**IClassFactory::LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) cuando el parámetro *fLock* es **TRUE.** La aplicación de servidor también debe llamar [**a CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) en el destructor de cada uno de sus objetos de instancia y en cada uno de sus métodos IClassFactory::**LockServer** cuando el parámetro *fLock* es **FALSE.**

Por último, la aplicación de servidor debe prestar atención al código de retorno de [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)y, si devuelve 0, la aplicación de servidor debe iniciar su limpieza, lo que, para un servidor con varios subprocesos, normalmente significa que debe indicar a sus distintos subprocesos que cierren sus bucles de mensajes y llamen a [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) y [**CoReleaseServerProcess.**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) Si se usan las funciones de administración de la duración del proceso del servidor, deben usarse tanto en las instancias de objeto como en el [**método LockServer.**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) De lo contrario, la aplicación de servidor puede apagarse prematuramente.

Cuando se realiza una solicitud [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) COM se pone en contacto con el servidor, serializa la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) del objeto de clase, vuelve al proceso de cliente, desmarshals la interfaz **IClassFactory** y la devuelve al cliente. En este momento, los clientes normalmente llaman [**a LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) con **TRUE** para evitar que se cierre el proceso del servidor. Sin embargo, hay un período de tiempo entre el momento en que se serializa el objeto de clase y cuando el cliente llama a **LockServer** en el que otro cliente podría conectarse al mismo servidor, obtener una instancia de y liberar esa instancia, lo que hace que el servidor se apague y dejar el primer cliente en alto y sin conexión con un puntero **IClassFactory desconectado.** Para evitar esta condición de carrera, COM agrega una llamada implícita a **LockServer** con **TRUE** al objeto de clase cuando serializa la interfaz **IClassFactory** y una llamada implícita a **LockServer** con **FALSE** cuando el cliente libera la interfaz **IClassFactory.** Por lo tanto, no es necesario volver a llamar a **LockServer** remotamente al servidor y el proxy para **LockServer** simplemente devuelve S OK sin tener que realizar realmente la \_ llamada remota.

Hay otra condición de carrera relacionada con la activación durante la inicialización de un proceso de servidor fuera de proceso. Un servidor COM que registra varias clases normalmente llama a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con REGCLS \_ LOCAL SERVER para cada \_ CLSID que admite. Una vez hecho esto para todas las clases, el servidor entra en su bucle de mensajes. Para un servidor COM de un solo subproceso, todas las solicitudes de activación se bloquean hasta que el servidor entra en el bucle de mensajes. Sin embargo, para un servidor de modelo de apartamento que registra objetos de clase diferentes en diferentes departamentos y para todos los servidores de subproceso libre, las solicitudes de activación pueden llegar antes que esto. En el caso de los servidores de modelos de apartamento, las solicitudes de activación podrían llegar en cuanto un subproceso haya entrado en su bucle de mensajes. En el caso de los servidores de subproceso libre, podría llegar una solicitud de activación en cuanto se registra el primer objeto de clase. Puesto que una activación puede producirse tan pronto, también es posible que se produzca la versión final (y, por tanto, que el servidor comience a apagarse) antes de que el resto del servidor haya tenido la oportunidad de terminar de inicializarse.

Para eliminar estas condiciones de carrera y simplificar el trabajo del escritor de servidores, cualquier servidor que quiera registrar varios objetos de clase con COM debe llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con \_ REGCLS LOCAL SERVER REGCLS SUSPENDED para cada \_ \| CLSID diferente que admita el \_ servidor. Una vez que se han registrado todas las clases y el proceso del servidor está listo para aceptar solicitudes de activación entrantes, el servidor debe realizar una llamada a [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects). Esta función indica a COM que informe al SCM sobre todas las clases registradas y comienza a permitir que las solicitudes de activación entren en el proceso del servidor. El uso de estas funciones proporciona las siguientes ventajas:

-   Solo se realiza una llamada al SCM, independientemente del número de CLID registrados, lo que reduce el tiempo de registro general (y, por tanto, el tiempo de inicio de la aplicación de servidor).
-   Si el servidor tiene varios departamentos y diferentes CLSID están registrados en diferentes departamentos, o si el servidor es un servidor de subproceso libre, no se recibirá ninguna solicitud de activación hasta que el servidor llame a [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects), lo que da al servidor la oportunidad de registrar todos sus CLID y configurarse correctamente antes de tener que tratar con las solicitudes de activación y las posibles solicitudes de cierre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 