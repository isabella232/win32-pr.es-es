---
description: Puede especificar un descriptor de seguridad para una canalización con nombre al llamar a la función CreateNamedPipe. El descriptor de seguridad controla el acceso a los extremos de cliente y servidor de la canalización con nombre.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Derechos de acceso y seguridad de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556987cf35845de249bf0e19f3a0b481aab18e891c3b6211f26eb51571704d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451215"
---
# <a name="named-pipe-security-and-access-rights"></a>Derechos de acceso y seguridad de canalización con nombre

Windows seguridad le permite controlar el acceso a las canalizaciones con nombre. Para obtener más información sobre la seguridad, vea [Modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad para](/windows/desktop/SecAuthZ/security-descriptors) una canalización con nombre al llamar a la función [**CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) El descriptor de seguridad controla el acceso a los extremos de cliente y servidor de la canalización con nombre. Si especifica **NULL,** la canalización con nombre obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para una canalización con nombre conceden control total a la cuenta LocalSystem, a los administradores y al propietario del creador. También conceden acceso de lectura a los miembros del grupo Todos y la cuenta anónima.

Para recuperar el descriptor de seguridad de una canalización con nombre, llame a la [**función GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Para cambiar el descriptor de seguridad de una canalización con nombre, llame a la [**función SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Cuando un subproceso llama a [**CreateNamedPipe para**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) abrir un identificador al final del servidor de una canalización con nombre existente, el sistema realiza una comprobación de acceso antes de devolver el identificador. La comprobación de acceso compara el token [](/windows/desktop/SecAuthZ/access-rights-and-access-masks) de acceso del subproceso y los derechos de acceso solicitados con la DACL del descriptor de seguridad de la canalización con nombre. Además de los derechos de acceso solicitados, la DACL debe permitir que el subproceso de llamada FILE \_ CREATE PIPE INSTANCE acceda a la canalización con \_ \_ nombre.

Del mismo modo, cuando un cliente llama a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para conectarse al extremo del cliente de una canalización con nombre, el sistema realiza una comprobación de acceso antes de conceder acceso al cliente.

El identificador devuelto por [**la función CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) siempre tiene acceso SYNCHRONIZE. También tiene LECTURA \_ GENÉRICA, ESCRITURA \_ GENÉRICA o ambas, dependiendo del modo abierto de la canalización. Estos son los derechos de acceso para cada modo abierto.



| Modo abierto                           | Derechos de acceso                                              |
|-------------------------------------|------------------------------------------------------------|
| DÚPLEX \_ DE ACCESO A CANALIZACIÓN \_ (0x00000003)   | FILE \_ GENERIC \_ READ, FILE GENERIC WRITE y \_ \_ SYNCHRONIZE |
| ACCESO \_ DE CANALIZACIÓN ENTRANTE \_ (0x00000001)  | FILE \_ GENERIC READ y \_ SYNCHRONIZE                        |
| SALIDA \_ DE ACCESO DE CANALIZACIÓN \_ (0x00000002) | FILE \_ GENERIC WRITE y \_ SYNCHRONIZE                       |



 

El acceso DE LECTURA GENÉRICO DE ARCHIVO para una canalización con nombre combina los derechos para leer datos de la canalización, leer atributos de canalización, leer atributos extendidos y leer la DACL de la \_ \_ canalización.

El acceso FILE GENERIC WRITE para una canalización con nombre combina los derechos para escribir datos en la canalización, anexar datos a ella, escribir atributos de canalización, escribir atributos extendidos y leer la DACL de la \_ \_ canalización. Dado que FILE \_ APPEND DATA y FILE CREATE PIPE INSTANCE tienen la misma \_ \_ \_ \_ definición, FILE GENERIC \_ WRITE \_ permite el permiso para crear la canalización. Para evitar este problema, use los derechos individuales en lugar de usar FILE \_ GENERIC \_ WRITE.

Puede solicitar el derecho de acceso ACCESS SYSTEM SECURITY a un objeto de canalización con nombre si desea leer o escribir la \_ \_ SACL del objeto. Para obtener más información, vea [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y Derecho de acceso [sacl](/windows/desktop/SecAuthZ/sacl-access-right).

Para evitar que usuarios remotos o usuarios de una sesión de terminal Services diferente accedan a una canalización con nombre, use el SID de inicio de sesión en la DACL para la canalización. El SID de inicio de sesión también se usa en los inicios de sesión de ejecución; es el SID que se usa para proteger el espacio de nombres del objeto por sesión. Para obtener más información, vea [Obtener el SID de inicio de sesión en C++.](/previous-versions//aa446670(v=vs.85))

 

 
