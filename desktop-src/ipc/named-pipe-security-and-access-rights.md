---
description: Se puede especificar un descriptor de seguridad para una canalización con nombre cuando se llama a la función CreateNamedPipe. El descriptor de seguridad controla el acceso a los extremos de cliente y de servidor de la canalización con nombre.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Seguridad y derechos de acceso de la canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cada606d8197ac2f64943aa742bbfd614fa4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648421"
---
# <a name="named-pipe-security-and-access-rights"></a>Seguridad y derechos de acceso de la canalización con nombre

La seguridad de Windows le permite controlar el acceso a las canalizaciones con nombre. Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Se puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para una canalización con nombre cuando se llama a la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . El descriptor de seguridad controla el acceso a los extremos de cliente y de servidor de la canalización con nombre. Si especifica **null**, la canalización con nombre obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para una canalización con nombre concedan control total a la cuenta LocalSystem, a los administradores y al propietario del creador. También conceden acceso de lectura a los miembros del grupo todos y a la cuenta anónima.

Para recuperar el descriptor de seguridad de una canalización con nombre, llame a la función [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para cambiar el descriptor de seguridad de una canalización con nombre, llame a la función [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Cuando un subproceso llama a [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para abrir un identificador del extremo del servidor de una canalización con nombre existente, el sistema realiza una comprobación de acceso antes de devolver el identificador. La comprobación de acceso compara el token de acceso del subproceso y los [derechos de acceso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) solicitados con la DACL en el descriptor de seguridad de la canalización con nombre. Además de los derechos de acceso solicitados, la DACL debe permitir que el archivo de subproceso que realiza la llamada \_ cree una \_ instancia de canalización \_ con nombre.

Del mismo modo, cuando un cliente llama a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para conectarse al extremo de cliente de una canalización con nombre, el sistema realiza una comprobación de acceso antes de conceder acceso al cliente.

El identificador devuelto por la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) siempre tiene acceso de sincronización. También tiene lectura genérica \_ , escritura genérica \_ o ambas, dependiendo del modo de apertura de la canalización. A continuación se muestran los derechos de acceso para cada modo abierto.



| Modo abierto                           | Derechos de acceso                                              |
|-------------------------------------|------------------------------------------------------------|
| Dúplex de acceso de CANALización \_ \_ (0x00000003)   | ARCHIVO \_ genérico de \_ lectura, \_ escritura genérica de archivo \_ y sincronización |
| ENTRADA de acceso de CANALización \_ \_ (0x00000001)  | \_ \_ Lectura y sincronización de archivos genéricos                        |
| Acceso de CANALización de \_ \_ salida (0x00000002) | \_ \_ Escritura y sincronización de archivos genéricos                       |



 

\_ \_ El acceso de lectura genérico de un archivo para una canalización con nombre combina los derechos para leer los datos de la canalización, leer los atributos de la canalización, leer atributos extendidos y leer la DACL de la canalización.

\_ \_ El acceso de escritura genérico de un archivo para una canalización con nombre combina los derechos para escribir datos en la canalización, anexar datos a él, escribir atributos de canalización, escribir atributos extendidos y leer la DACL de la canalización. Dado que \_ el archivo anexar \_ datos y \_ \_ \_ la instancia de la canalización de creación de archivo tienen la misma definición, por lo que la \_ escritura genérica de archivo habilita el \_ permiso para crear la canalización. Para evitar este problema, use los derechos individuales en lugar de usar FILE \_ Generic \_ Write.

Puede solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ a un objeto de canalización con nombre si desea leer o escribir la SACL del objeto. Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Para evitar que usuarios remotos o usuarios de una sesión de Terminal Services diferente tengan acceso a una canalización con nombre, use el SID de inicio de sesión en la DACL de la canalización. El SID de inicio de sesión se usa también en los inicios de sesión de ejecución. es el SID que se usa para proteger el espacio de nombres de objeto por sesión. Para obtener más información, vea [obtener el SID de inicio de sesión en C++](/previous-versions//aa446670(v=vs.85)).

 

 
