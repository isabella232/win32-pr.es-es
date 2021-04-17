---
description: Los objetos con nombre proporcionan una manera sencilla de que los procesos compartan los identificadores de objetos.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Nombres de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667975"
---
# <a name="object-names"></a>Nombres de objeto

Los objetos con nombre proporcionan una manera sencilla de que los procesos compartan los identificadores de objetos. Después de que un proceso haya creado un objeto con nombre, una exclusión mutua, un semáforo o un objeto de temporizador, otros procesos pueden usar el nombre para llamar a la función adecuada ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)o [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) para abrir un identificador para el objeto. La comparación de nombres distingue mayúsculas de minúsculas.

Los nombres de evento, semáforo, exclusión mutua, temporizador que se pueden esperar, asignación de archivos y objetos de trabajo comparten el mismo espacio de nombres. Si intenta crear un objeto con un nombre que está en uso por un objeto de otro tipo, se produce un error en la función y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **\_ \_ identificador no válido**. Por lo tanto, al crear objetos con nombre, use nombres únicos y asegúrese de comprobar los valores devueltos de la función en busca de errores de nombre duplicado.

Si intenta crear un objeto con un nombre que está siendo utilizado por un objeto del mismo tipo, la función se ejecuta correctamente, devuelve un identificador al objeto existente y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error \_ ya \_ existe**. Por ejemplo, si el nombre especificado en una llamada a la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) coincide con el nombre de un objeto mutex existente, la función devuelve un identificador al objeto existente. En este caso, la llamada a **CreateMutex** es equivalente a una llamada a la función [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . La existencia de varios procesos usa **CreateMutex** para la misma exclusión mutua, por lo tanto, es equivalente a tener un proceso que llama a **CreateMutex** mientras que los demás procesos llaman a **OpenMutex**, salvo que elimina la necesidad de asegurarse de que el proceso de creación se inicia en primer lugar. Sin embargo, cuando se usa esta técnica para objetos mutex, ninguno de los procesos de llamada debe solicitar la propiedad inmediata de la exclusión mutua. Si varios procesos solicitan la propiedad inmediata, puede ser difícil predecir qué proceso obtiene realmente la propiedad inicial.

Un entorno de Terminal Services tiene un espacio de nombres global para eventos, semáforos, exclusiones mutuas, temporizadores que se esperan, objetos de asignación de archivos y objetos de trabajo. Además, cada Terminal Services sesión de cliente tiene su propio espacio de nombres independiente para estos objetos. Terminal Services procesos de cliente pueden utilizar nombres de objeto con un \\ prefijo "global" o "local \\ " para crear explícitamente un objeto en el espacio de nombres global o de sesión. Para obtener más información, vea [espacios de nombres de objetos de kernel](../termserv/kernel-object-namespaces.md). El cambio rápido de usuario se implementa mediante Terminal Services sesiones (cada usuario inicia sesión en una sesión diferente). Los nombres de objeto de kernel deben seguir las instrucciones descritas para Terminal Services para que las aplicaciones puedan admitir varios usuarios.

Los objetos de sincronización se pueden crear en un espacio de nombres privado. Para obtener más información, vea [espacios de nombres de objetos](object-namespaces.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos con nombre](using-named-objects.md)
</dt> </dl>

 

 
