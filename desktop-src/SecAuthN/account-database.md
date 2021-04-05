---
description: Active Directory proporciona la base de datos de cuentas que utiliza el Centro de distribución de claves (KDC) para obtener información acerca de las entidades de seguridad del dominio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Base de datos de cuentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0713d8f7b4336f43172fcd5cda18aa9d25c702fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002135"
---
# <a name="account-database"></a>Base de datos de cuentas

Active Directory proporciona la base de datos de cuentas que utiliza el [*centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) para obtener información acerca de las [*entidades de seguridad*](/windows/desktop/SecGloss/s-gly) del dominio. Cada entidad de seguridad se representa mediante un objeto de cuenta en el directorio. La clave de [*cifrado*](/windows/desktop/SecGloss/e-gly) que se usa para comunicarse con un usuario, un equipo o un servicio se almacena como un atributo del objeto de cuenta de esa entidad de seguridad.

Solo los controladores de dominio son servidores de Active Directory. Cada controlador de dominio mantiene una copia de escritura del directorio, por lo que se pueden crear cuentas, restablecer contraseñas y pertenencia a grupos modificadas en cualquier controlador de dominio. Los cambios realizados en una réplica del directorio se propagan automáticamente a las demás réplicas. Windows replica el almacén de información para el Active Directory mediante un protocolo de replicación de varios maestros propietario que usa una conexión de llamada a procedimiento remoto segura entre los asociados de replicación. La conexión utiliza el [*Protocolo de autenticación Kerberos*](/windows/desktop/SecGloss/k-gly) para proporcionar [*autenticación*](/windows/desktop/SecGloss/a-gly) y cifrado mutuos.

El [agente de sistema de directorio](/windows/desktop/AD/directory-system-agent)administra el almacenamiento físico de los datos de la cuenta, un proceso protegido integrado con la autoridad de [*seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) en el controlador de dominio. Los clientes del servicio de directorio nunca reciben acceso directo al almacén de datos. Cualquier cliente que desee tener acceso a información de directorio debe conectarse al agente de sistema de directorio y, a continuación, buscar, leer y escribir objetos de directorio y sus atributos.

Las solicitudes para tener acceso a un objeto o atributo en el directorio están sujetas a la validación mediante mecanismos de control de acceso de Windows. Al igual que los objetos de archivo y carpeta en el sistema de archivos NTFS, los objetos del Active Directory están protegidos mediante [*listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) que especifican quién puede tener acceso al objeto y de qué manera. Sin embargo, a diferencia de los archivos y las carpetas, Active Directory objetos tienen una ACL para cada uno de sus atributos. Por lo tanto, los atributos de información confidencial de la cuenta se pueden proteger mediante permisos más restrictivos que los concedidos a otros atributos de la cuenta.

La información más confidencial sobre una cuenta es, por supuesto, su contraseña. Aunque el atributo de contraseña de un objeto de cuenta almacena una clave de cifrado derivada de una contraseña, no la propia contraseña, esta clave es tan útil para un intruso. Por lo tanto, el acceso al atributo de contraseña de un objeto de cuenta solo se concede al titular de la cuenta, nunca a nadie más, ni a los administradores. Solo los procesos con privilegio base de computación de confianza (procesos que se ejecutan en el [*contexto*](/windows/desktop/SecGloss/c-gly) de seguridad de LSA) pueden leer o cambiar la información de contraseña.

Para entorpecer un ataque sin conexión por parte de alguien con acceso a la cinta de copia de seguridad de un controlador de dominio, el atributo de contraseña de un objeto de cuenta se protege más mediante un segundo cifrado mediante una clave del sistema. Esta clave de cifrado se puede almacenar en un medio extraíble para que se pueda proteger por separado o puede almacenarse en el controlador de dominio, pero protegido por un mecanismo disperso. A los administradores se les ofrece la opción de elegir dónde se almacena la clave del sistema y cuál de los diversos algoritmos se usa para cifrar los atributos de contraseña.

 

 
