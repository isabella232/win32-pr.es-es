---
description: Los objetos con nombre proporcionan una manera sencilla de que los procesos compartan identificadores de objetos.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Nombres de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d794871ef3f55a930a06a6cfc4cfc09451635d4883d97e128104b49998589229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886274"
---
# <a name="object-names"></a>Nombres de objeto

Los objetos con nombre proporcionan una manera sencilla de que los procesos compartan identificadores de objetos. Una vez que un proceso ha creado un evento con nombre, una exclusión mutua, un semáforo o un objeto de temporizador, otros procesos pueden usar el nombre para llamar a la función adecuada [**(OpenEvent,**](/windows/win32/api/synchapi/nf-synchapi-openeventa) [**OpenMutex,**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)o [**OpenWaitableTimer)**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)para abrir un identificador para el objeto. La comparación de nombres distingue mayúsculas de minúsculas.

Los nombres de los objetos event, semaphore, mutex, waitable timer, file-mapping y job comparten el mismo espacio de nombres. Si intenta crear un objeto con un nombre que está en uso por un objeto de otro tipo, se produce un error en la función y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR INVALID \_ \_ HANDLE**. Por lo tanto, al crear objetos con nombre, use nombres únicos y asegúrese de comprobar los valores devueltos de la función para los errores de nombre duplicado.

Si intenta crear un objeto con un nombre que está en uso por un objeto del mismo tipo, la función se realiza correctamente, devolviendo un identificador al objeto existente y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR ALREADY \_ \_ EXISTS**. Por ejemplo, si el nombre especificado en una llamada a la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) coincide con el nombre de un objeto mutex existente, la función devuelve un identificador al objeto existente. En este caso, la llamada a **CreateMutex es** equivalente a una llamada a la [**función OpenMutex.**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) Por lo tanto, hacer que varios procesos usen **CreateMutex** para la misma exclusión mutua es equivalente a tener un proceso que llama a **CreateMutex** mientras que los demás procesos llaman a **OpenMutex,** salvo que elimina la necesidad de asegurarse de que el proceso de creación se inicia primero. Sin embargo, cuando se usa esta técnica para objetos de exclusión mutua, ninguno de los procesos de llamada debe solicitar la propiedad inmediata de la exclusión mutua. Si varios procesos solicitan la propiedad inmediata, puede ser difícil predecir qué proceso obtiene realmente la propiedad inicial.

Un entorno de Terminal Services tiene un espacio de nombres global para eventos, semáforos, exclusiones mutuas, temporizadores que se pueden esperar, objetos de asignación de archivos y objetos de trabajo. Además, cada sesión de cliente de Terminal Services tiene su propio espacio de nombres independiente para estos objetos. Los procesos de cliente de Terminal Services pueden usar nombres de objeto con un prefijo "Global" o "Local" para crear explícitamente un objeto en el espacio de nombres \\ \\ global o de sesión. Para obtener más información, vea [Kernel Object Namespaces](../termserv/kernel-object-namespaces.md). El cambio rápido de usuarios se implementa mediante sesiones de Terminal Services (cada usuario inicia sesión en una sesión diferente). Los nombres de objeto de kernel deben seguir las instrucciones descritas para Terminal Services para que las aplicaciones puedan admitir varios usuarios.

Los objetos de sincronización se pueden crear en un espacio de nombres privado. Para obtener más información, vea [Espacios de nombres de objeto](object-namespaces.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos con nombre](using-named-objects.md)
</dt> </dl>

 

 
