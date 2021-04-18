---
description: El modelo de seguridad de Windows permite controlar el acceso a los objetos de evento, exclusión mutua, semáforo y temporizador que se puede esperar. No se pueden proteger las colas de temporizador, las variables de interbloqueos y los objetos de sección crítica. Para obtener más información, vea modelo de Access-Control.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Derechos de acceso y seguridad de objetos de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c4bfdb17a6e1c4d99a3e9722e67a3b48a3c788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667513"
---
# <a name="synchronization-object-security-and-access-rights"></a>Derechos de acceso y seguridad de objetos de sincronización

El modelo de seguridad de Windows permite controlar el acceso a los objetos de evento, exclusión mutua, semáforo y temporizador que se puede esperar. No se pueden proteger las colas de temporizador, las variables de interbloqueos y los objetos de sección crítica. Para obtener más información, vea [modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un [descriptor de seguridad](../secauthz/security-descriptors.md) para un objeto de sincronización entre procesos cuando se llama a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore (**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Si especifica **null**, el objeto obtiene un descriptor de seguridad predeterminado. Las [listas de control de acceso (ACL)](../secauthz/access-control-lists.md) del descriptor de seguridad predeterminado para un objeto de sincronización proceden del token principal o de suplantación del creador.

Para obtener o establecer el descriptor de seguridad de un objeto Event, mutex, Semaphore o waitable Timer, llame a las funciones [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Los identificadores devueltos por [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore (**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)y [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) tienen acceso total al nuevo objeto. Cuando se llama a las funciones [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)y [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.

Los derechos de acceso válidos para los objetos de sincronización entre procesos incluyen los [derechos de acceso estándar](../secauthz/standard-access-rights.md) y algunos derechos de acceso específicos del objeto. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Value                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eliminar** (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                           |
| **Leer \_ CONTROL** (0x00020000L) | Necesario para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho de acceso de **\_ \_ seguridad del sistema de acceso** . Para obtener más información, consulte [derechos de acceso de SACL](../secauthz/sacl-access-right.md). |
| **Sincronizar** (0x00100000L)   | Derecho a utilizar el objeto para la sincronización. Esto permite a un subproceso esperar hasta que el objeto se encuentra en el estado señalado.                                                                                                                                                                |
| **Escribir \_ DAC** (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad para el objeto.                                                                                                                                                                                                                   |
| **Escribir \_ PROPIETARIO** (0x00080000L)  | Necesario para cambiar el propietario del descriptor de seguridad para el objeto.                                                                                                                                                                                                                  |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de evento. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de TODO el \_ acceso** (0x1F0003) | Todos los derechos de acceso posibles para un objeto de evento. Use este derecho solo si la aplicación requiere acceso más allá del que conceden los derechos de acceso estándar y el **\_ \_ Estado de modificación de eventos**. El uso de este derecho de acceso aumenta la posibilidad de que un administrador deba ejecutar la aplicación. |
| **Evento \_ de MODIFICAR \_ Estado** (0x0002) | Modifique el acceso de estado, que es necesario para las funciones [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) y [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) .                                                                                                                                    |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos mutex. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Exclusión mutua \_ TODO el \_ acceso** (0x1F0001) | Todos los derechos de acceso posibles para un objeto mutex. Use este derecho solo si la aplicación requiere acceso más allá de los concedidos por los derechos de acceso estándar. El uso de este derecho de acceso aumenta la posibilidad de que un administrador deba ejecutar la aplicación. |
| **Exclusión mutua \_ MODIFICAR \_ Estado** (0x0001) | Reservado para uso futuro.                                                                                                                                                                                                                                           |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de semáforo. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                                 | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Semáforo \_ TODO el \_ acceso** (0x1F0003) | Todos los derechos de acceso posibles para un objeto de semáforo. Use este derecho solo si la aplicación requiere acceso más allá del que conceden los derechos de acceso estándar y el **\_ \_ Estado de modificación del semáforo**. El uso de este derecho de acceso aumenta la posibilidad de que un administrador deba ejecutar la aplicación. |
| **Semáforo \_ MODIFICAR \_ Estado** (0x0002) | Modifique el acceso de estado, que es necesario para la función [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) .                                                                                                                                                                                                   |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de temporizador que se puede esperar. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Temporizador \_ de TODO el \_ acceso** (0x1F0003) | Todos los derechos de acceso posibles para un objeto de temporizador que se puede esperar. Use este derecho solo si la aplicación requiere acceso más allá del que conceden los derechos de acceso estándar y el **\_ \_ Estado de modificación del temporizador**. El uso de este derecho de acceso aumenta la posibilidad de que un administrador deba ejecutar la aplicación. |
| **Temporizador \_ de MODIFICAR \_ Estado** (0x0002) | Modifique el acceso de estado, que es necesario para las funciones [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) y [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) .                                                                                                                                            |
| **Temporizador \_ de \_Estado** de la consulta (0x0001)  | Reservado para uso futuro.                                                                                                                                                                                                                                                                                 |



 

Para leer o escribir la SACL de un objeto de sincronización entre procesos, debe solicitar el derecho de acceso de **\_ \_ seguridad del sistema de acceso** . Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y [SACL](../secauthz/sacl-access-right.md).

 

 
