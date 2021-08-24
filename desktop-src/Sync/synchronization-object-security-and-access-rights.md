---
description: El Windows de seguridad le permite controlar el acceso a objetos de evento, exclusión mutua, semáforo y temporizador que se pueden esperar. Las colas de temporizador, las variables entrelazados y los objetos de sección críticos no son protegibles. Para obtener más información, vea Access-Control modelo.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Derechos de acceso y seguridad de objetos de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85ca76002a92e305983ab97d46dfde2f36f9ae49a779e091a072d3090ceb976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739295"
---
# <a name="synchronization-object-security-and-access-rights"></a>Derechos de acceso y seguridad de objetos de sincronización

El Windows de seguridad le permite controlar el acceso a objetos de evento, exclusión mutua, semáforo y temporizador que se pueden esperar. Las colas de temporizador, las variables entrelazados y los objetos de sección críticos no son protegibles. Para obtener más información, vea [Modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un descriptor de [seguridad](../secauthz/security-descriptors.md) para un objeto de sincronización entre procesos al llamar a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Si especifica **NULL,** el objeto obtiene un descriptor de seguridad predeterminado. Las listas de control de [acceso (ACL)](../secauthz/access-control-lists.md) del descriptor de seguridad predeterminado para un objeto de sincronización proceden del token principal o de suplantación del creador.

Para obtener o establecer el descriptor de seguridad de un evento, exclusión mutua, semáforo o objeto de temporizador que se puede esperar, llame a las funciones [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo)

Los identificadores devueltos por [**CreateEvent,**](/windows/win32/api/synchapi/nf-synchapi-createeventa) [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)y [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) tienen acceso completo al nuevo objeto. Al llamar a las funciones [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex,**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)y [**OpenWaitableTimer,**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.

Los derechos de acceso válidos para los objetos de sincronización entre procesos incluyen los [derechos de acceso estándar](../secauthz/standard-access-rights.md) y algunos derechos de acceso específicos del objeto. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Value                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DELETE** (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                           |
| **READ \_ CONTROL** (0x00020000L) | Necesario para leer información en el descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho **de acceso ACCESS SYSTEM \_ \_ SECURITY.** Para obtener más información, vea [SACL Access Right](../secauthz/sacl-access-right.md). |
| **SYNCHRONIZE** (0x00100000L)   | Derecho a utilizar el objeto para la sincronización. Esto permite que un subproceso espere hasta que el objeto esté en estado señalado.                                                                                                                                                                |
| **ESCRITURA \_ DAC** (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad del objeto .                                                                                                                                                                                                                   |
| **ESCRITURA \_ OWNER** (0x00080000L)  | Necesario para cambiar el propietario en el descriptor de seguridad del objeto .                                                                                                                                                                                                                  |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de evento. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ ALL \_ ACCESS** (0x1F0003) | Todos los derechos de acceso posibles para un objeto de evento. Use este derecho solo si la aplicación requiere acceso más allá del concedido por los derechos de acceso estándar y **EVENT \_ MODIFY \_ STATE**. El uso de este derecho de acceso aumenta la posibilidad de que la aplicación la ejecute un administrador. |
| **EVENT \_ MODIFY \_ STATE** (0x0002) | Modifique el acceso de estado, que es necesario para las [**funciones SetEvent,**](/windows/win32/api/synchapi/nf-synchapi-setevent) [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) [**y PulseEvent.**](/windows/desktop/api/WinBase/nf-winbase-pulseevent)                                                                                                                                    |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de exclusión mutua. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_ ALL \_ ACCESS** (0x1F0001) | Todos los derechos de acceso posibles para un objeto de exclusión mutua. Use este derecho solo si la aplicación requiere acceso más allá del concedido por los derechos de acceso estándar. El uso de este derecho de acceso aumenta la posibilidad de que la aplicación la ejecute un administrador. |
| **MUTEX \_ MODIFY \_ STATE** (0x0001) | Reservado para uso futuro.                                                                                                                                                                                                                                           |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de semáforo. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                                 | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEMAPHORE \_ ALL \_ ACCESS** (0x1F0003) | Todos los derechos de acceso posibles para un objeto semáforo. Use este derecho solo si la aplicación requiere acceso más allá del concedido por los derechos de acceso estándar y **SEMAPHORE \_ MODIFY \_ STATE**. El uso de este derecho de acceso aumenta la posibilidad de que la aplicación la ejecute un administrador. |
| **SEMAPHORE \_ MODIFY \_ STATE** (0x0002) | Modifique el acceso de estado, que es necesario para la [**función ReleaseSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore)                                                                                                                                                                                                   |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto para los objetos de temporizador que se pueden esperar. Estos derechos se admiten además de los derechos de acceso estándar.



| Value                             | Significado                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TEMPORIZADOR \_ ALL \_ ACCESS** (0x1F0003) | Todos los derechos de acceso posibles para un objeto de temporizador que se puede esperar. Use este derecho solo si la aplicación requiere acceso más allá del concedido por los derechos de acceso estándar y **TIMER \_ MODIFY \_ STATE**. El uso de este derecho de acceso aumenta la posibilidad de que la aplicación la ejecute un administrador. |
| **TEMPORIZADOR \_ MODIFY \_ STATE** (0x0002) | Modifique el acceso de estado, que es necesario para las [**funciones SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) [**y CancelWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer)                                                                                                                                            |
| **TEMPORIZADOR \_ ESTADO \_ DE CONSULTA** (0x0001)  | Reservado para uso futuro.                                                                                                                                                                                                                                                                                 |



 

Para leer o escribir la SACL de un objeto de sincronización entre procesos, debe solicitar el derecho de acceso **ACCESS \_ SYSTEM \_ SECURITY.** Para obtener más información, vea [Listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y Derecho de acceso [sacl](../secauthz/sacl-access-right.md).

 

 
