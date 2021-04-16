---
title: Espacios de nombres de objetos de kernel
description: Servicios de Escritorio remoto utiliza varios espacios de nombres para los objetos de kernel; un espacio de nombres global se usa principalmente en los servicios de las aplicaciones cliente/servidor.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20680a32c8b35e3fa2f1ab15c732683d424550f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685790"
---
# <a name="kernel-object-namespaces"></a>Espacios de nombres de objetos de kernel

Un servidor de Servicios de Escritorio remoto tiene varios espacios de nombres para los siguientes objetos de kernel con nombre: eventos, semáforos, exclusiones mutuas, temporizadores que se esperan, objetos de asignación de archivos y objetos de trabajo. Hay un espacio de nombres global utilizado principalmente por los servicios de las aplicaciones cliente/servidor. Además, cada sesión de cliente tiene un espacio de nombres independiente para estos objetos, como en Windows Vista.

Los espacios de nombres de sesión de cliente independientes permiten que varios clientes ejecuten las mismas aplicaciones sin interferir entre sí. En el caso de los procesos iniciados en una sesión de cliente, el sistema utiliza el espacio de nombres de sesión de forma predeterminada. Sin embargo, estos procesos pueden usar el espacio de nombres global anteponiendo el \\ prefijo "global" al nombre del objeto. Por ejemplo, el código siguiente llama a [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) y crea un objeto de evento denominado CSAPP en el espacio de nombres global:

> [!Note]  
> El espacio de nombres global no está disponible para las aplicaciones de la tienda Windows.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Las aplicaciones de servicio en un entorno de Servicios de Escritorio remoto usan el espacio de nombres global de forma predeterminada.

La sesión cero solo se usa para hospedar servicios y no hay ninguna sesión de consola, a diferencia de las versiones anteriores de Windows.

El espacio de nombres global permite que los procesos de varias sesiones de cliente se comuniquen con una aplicación de servicio. Por ejemplo, una aplicación cliente/servidor podría usar un objeto de exclusión mutua para la sincronización. El módulo de servidor puede crear el objeto mutex en el espacio de nombres global. Después, una sesión de cliente puede usar el \\ prefijo "global" para abrir el objeto de exclusión mutua.

Otro uso del espacio de nombres global es para las aplicaciones que utilizan objetos con nombre para detectar que ya existe una instancia de la aplicación que se ejecuta en el sistema en todas las sesiones. Este objeto con nombre debe crearse o abrirse en el espacio de nombres global en lugar de en el espacio de nombres por sesión. El caso más común de ejecutar la aplicación una vez por sesión es compatible de forma predeterminada porque el objeto con nombre se crea en un espacio de nombres por sesión.

Además del prefijo "global \\ ", los procesos de cliente pueden usar el \\ prefijo "local" para crear explícitamente un objeto en su espacio de nombres de sesión. Estas palabras clave distinguen mayúsculas de minúsculas.

El \\ prefijo "session" está reservado para el uso del sistema y no se debe utilizar en los nombres de los objetos de kernel.

El cambio rápido de usuario se implementa mediante el uso de sesiones de Servicios de Escritorio remoto. El primer usuario que inicia sesión usa la sesión uno, el siguiente usuario que inicia sesión usa la sesión dos, y así sucesivamente. Los nombres de objeto de kernel deben seguir las instrucciones descritas para Servicios de Escritorio remoto para que las aplicaciones puedan admitir varios usuarios.

La creación de un objeto de asignación de archivos en el espacio de nombres global, mediante [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), desde una sesión que no sea la sesión cero es una operación con privilegios. Por este motivo, una aplicación que se ejecuta en una sesión de servidor de host de sesión de Escritorio remoto de escritorio remoto debe tener habilitada la opción [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) para poder crear correctamente un objeto de asignación de archivos en el espacio de nombres global. La comprobación de privilegios se limita a la creación de objetos de asignación de archivos y no se aplica a la apertura de los existentes. Por ejemplo, si un servicio o el sistema crean un objeto de asignación de archivos, cualquier proceso que se ejecute en cualquier sesión podrá tener acceso a ese objeto de asignación de archivos siempre que el usuario tenga el acceso necesario.

 

 