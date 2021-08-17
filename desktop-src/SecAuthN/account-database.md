---
description: Active Directory proporciona la base de datos de cuenta que el Centro de distribución de claves (KDC) usa para obtener información sobre las entidades de seguridad del dominio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Base de datos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141598"
---
# <a name="account-database"></a>Base de datos de cuenta

Active Directory proporciona la base de datos de cuenta que el [*Centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) usa para obtener información sobre las entidades de [*seguridad*](/windows/desktop/SecGloss/s-gly) del dominio. Cada entidad de seguridad se representa mediante un objeto de cuenta en el directorio . La [*clave*](/windows/desktop/SecGloss/e-gly) de cifrado utilizada para comunicarse con un usuario, equipo o servicio se almacena como un atributo del objeto de cuenta de esa entidad de seguridad.

Solo los controladores de dominio Active Directory servidores. Cada controlador de dominio mantiene una copia grabable del directorio, por lo que se pueden crear cuentas, restablecer contraseñas y modificar la pertenencia a grupos en cualquier controlador de dominio. Los cambios realizados en una réplica del directorio se propagan automáticamente a todas las demás réplicas. Windows replica el almacén de información para el Active Directory mediante un protocolo de replicación de varios maestros propietario que usa una conexión de llamada a procedimiento remoto seguro entre asociados de replicación. La conexión usa el protocolo [*de autenticación Kerberos para*](/windows/desktop/SecGloss/k-gly) proporcionar [*autenticación mutua*](/windows/desktop/SecGloss/a-gly) y cifrado.

El agente del sistema de directorio administra el almacenamiento físico de los datos de la [cuenta,](/windows/desktop/AD/directory-system-agent)un proceso protegido integrado con la autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) en el controlador de dominio. A los clientes del servicio de directorio nunca se les proporciona acceso directo al almacén de datos. Cualquier cliente que desee acceder a la información del directorio debe conectarse al Agente de sistema de directorios y, a continuación, buscar, leer y escribir objetos de directorio y sus atributos.

Las solicitudes de acceso a un objeto o atributo en el directorio están sujetas a validación mediante Windows de control de acceso. Al igual que los objetos de archivos y carpetas del sistema de archivos NTFS, los objetos del Active Directory están protegidos por listas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) que especifican quién puede acceder al objeto y de qué manera. Sin embargo, a diferencia de los archivos y carpetas, Active Directory objetos tienen una ACL para cada uno de sus atributos. Por lo tanto, los atributos de información confidencial de la cuenta se pueden proteger con permisos más restrictivos que los concedidos para otros atributos de la cuenta.

La información más confidencial sobre una cuenta es, por supuesto, su contraseña. Aunque el atributo password de un objeto de cuenta almacena una clave de cifrado derivada de una contraseña, no la propia contraseña, esta clave es igual de útil para un intrusista. Por lo tanto, el acceso al atributo password de un objeto de cuenta solo se concede al titular de la cuenta, nunca a nadie, ni siquiera a los administradores. Solo los procesos con privilegios de base [](/windows/desktop/SecGloss/c-gly) de informática de confianza (procesos que se ejecutan en el contexto de seguridad del LSA) pueden leer o cambiar la información de contraseña.

Para impedir un ataque sin conexión por parte de alguien con acceso a la cinta de copia de seguridad de un controlador de dominio, el atributo de contraseña de un objeto de cuenta se protege aún más mediante un segundo cifrado mediante una clave del sistema. Esta clave de cifrado se puede almacenar en medios extraíbles para que se pueda proteger por separado, o se puede almacenar en el controlador de dominio, pero protegida por un mecanismo de dispersión. Los administradores tienen la opción de elegir dónde se almacena la clave del sistema y cuál de varios algoritmos se usa para cifrar los atributos de contraseña.

 

 
