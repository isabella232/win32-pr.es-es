---
title: Espacios de nombres de objeto kernel
description: Servicios de Escritorio remoto varios espacios de nombres para objetos de kernel; un espacio de nombres global lo usan principalmente los servicios en aplicaciones cliente/servidor.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e1064638844039091dbe93aa1fedc75cb93f4aa1d012f8864e0154673c6cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989094"
---
# <a name="kernel-object-namespaces"></a>Espacios de nombres de objeto kernel

Un servidor Servicios de Escritorio remoto tiene varios espacios de nombres para los siguientes objetos de kernel con nombre: eventos, semáforos, exclusiones mutuas, temporizadores que se pueden esperar, objetos de asignación de archivos y objetos de trabajo. Hay un espacio de nombres global que usan principalmente los servicios en las aplicaciones cliente/servidor. Además, cada sesión de cliente tiene un espacio de nombres independiente para estos objetos, como en Windows Vista.

Los espacios de nombres de sesión de cliente independientes permiten que varios clientes ejecuten las mismas aplicaciones sin interferir entre sí. Para los procesos iniciados en una sesión de cliente, el sistema usa el espacio de nombres de sesión de forma predeterminada. Sin embargo, estos procesos pueden usar el espacio de nombres global anteponer el prefijo \\ "Global" al nombre del objeto. Por ejemplo, el código siguiente llama a [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) y crea un objeto de evento denominado CSAPP en el espacio de nombres global:

> [!Note]  
> El espacio de nombres global no está disponible para las Windows Store.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Las aplicaciones de servicio de un Servicios de Escritorio remoto usan el espacio de nombres global de forma predeterminada.

La sesión cero solo se usa para hospedar servicios y no hay ninguna sesión de consola, a diferencia de las versiones anteriores de Windows.

El espacio de nombres global permite que los procesos de varias sesiones de cliente se comuniquen con una aplicación de servicio. Por ejemplo, una aplicación cliente/servidor podría usar un objeto mutex para la sincronización. El módulo de servidor puede crear el objeto mutex en el espacio de nombres global. A continuación, una sesión de cliente puede usar el prefijo \\ "Global" para abrir el objeto mutex.

Otro uso del espacio de nombres global es que las aplicaciones que usan objetos con nombre detecten que ya hay una instancia de la aplicación que se ejecuta en el sistema en todas las sesiones. Este objeto con nombre debe crearse o abrirse en el espacio de nombres global en lugar del espacio de nombres por sesión. El caso más común de ejecutar la aplicación una vez por sesión es compatible de forma predeterminada porque el objeto con nombre se crea en un espacio de nombres por sesión.

Además del prefijo "Global", los procesos de cliente pueden usar el prefijo "Local" para crear explícitamente un objeto en \\ su espacio de nombres de \\ sesión. Estas palabras clave distinguen mayúsculas de minúsculas.

El prefijo "Sesión" está reservado para uso del sistema y no debe \\ usarlo en nombres de objetos de kernel.

La conmutación rápida de usuarios se implementa mediante Servicios de Escritorio remoto sesión. El primer usuario que inicia sesión usa la sesión uno, el siguiente usuario que inicia sesión usa la sesión dos, y así sucesivamente. Los nombres de objeto de kernel deben seguir las directrices descritas Servicios de Escritorio remoto para que las aplicaciones puedan admitir varios usuarios.

La creación de un objeto de asignación de archivos en el espacio de nombres global, mediante [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), desde una sesión que no sea la sesión cero es una operación con privilegios. Por este problema, una aplicación que se ejecuta en una sesión arbitraria de servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) debe tener [seCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) habilitado para crear correctamente un objeto de asignación de archivos en el espacio de nombres global. La comprobación de privilegios se limita a la creación de objetos de asignación de archivos y no se aplica a la apertura de los existentes. Por ejemplo, si un servicio o el sistema crea un objeto de asignación de archivos, cualquier proceso que se ejecute en cualquier sesión puede tener acceso a ese objeto de asignación de archivos siempre que el usuario tenga el acceso necesario.

 

 