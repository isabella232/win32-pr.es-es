---
title: Acerca de las cuentas de inicio de sesión de servicio
description: Cuando se inicia un servicio basado en Win32, inicia sesión en el equipo local.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ba72ffca4362f42c6a5ad6ee494e36e9698d7883c19e3fe2a157e153ce556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841025"
---
# <a name="about-service-logon-accounts"></a>Acerca de las cuentas de inicio de sesión de servicio

Cuando se inicia un servicio basado en Win32, inicia sesión en el equipo local. Puede iniciar sesión como:

-   Una cuenta de usuario local o de dominio.
-   La cuenta LocalSystem.

La cuenta de inicio de sesión determina la identidad de seguridad del servicio en tiempo de ejecución, es decir, el contexto de seguridad principal del servicio. El contexto de seguridad determina la capacidad del servicio para acceder a los recursos locales y de red. Por ejemplo, un servicio que se ejecuta en el contexto de seguridad de una cuenta de usuario local no puede acceder a los recursos de red. Por el contrario, un servicio que se ejecuta en el contexto de seguridad de la cuenta LocalSystem en un controlador de dominio (DC) de Windows 2000 tendría acceso sin restricciones al controlador de dominio. Para obtener más información y una explicación de las ventajas y limitaciones entre las cuentas de usuario y LocalSystem, vea [Contextos](security-contexts-and-active-directory-domain-services.md)de seguridad y Active Directory Domain Services .

En última instancia, los administradores del sistema donde está instalado el servicio tienen control sobre la cuenta de inicio de sesión del servicio. Por motivos de seguridad, es posible que algunos administradores no le permitan instalar el servicio en la cuenta LocalSystem. El servicio debe poder ejecutarse en una cuenta de usuario de dominio. Como programador, puede ejercer cierto control sobre la cuenta de inicio de sesión del servicio. El instalador de servicio especifica la cuenta de inicio de sesión del servicio cuando llama a la [**función CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar el servicio en un equipo host. El instalador puede sugerir una cuenta de inicio de sesión predeterminada, pero debe permitir que un administrador especifique la cuenta real.

El instalador también puede realizar las siguientes tareas relacionadas con la cuenta de inicio de sesión del servicio:

-   Instalación. Si instala el servicio para que se ejecute en una cuenta de usuario, la cuenta debe existir antes de llamar a [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Puede usar una cuenta existente o crear una como parte de installrt del equipo host. Para obtener más información, [consulte Configuración de la cuenta de usuario de un servicio.](setting-up-a-serviceampaposs-user-account.md)
-   Autenticación. Si desea que los clientes usen la autenticación mutua de Kerberos, registre los SPN en la cuenta de inicio de sesión del servicio. Si el servicio se ejecuta en la cuenta LocalSystem, la cuenta de inicio de sesión del servicio es la cuenta de equipo del equipo host. Para obtener más información, consulte [Service Principal Names](service-principal-names.md) (Nombres de entidad de seguridad de servicio).
-   Conceder acceso. Asegúrese de que el servicio en tiempo de ejecución tiene los derechos de acceso y privilegios que necesita para realizar sus tareas. Esto puede requerir establecer entradas de control de acceso (ACE) en los descriptores de seguridad de varios recursos, es decir, objetos de directorio, recursos compartidos de archivos, entre otros, para permitir los derechos de acceso necesarios a la cuenta de usuario o equipo. Para obtener más información, vea [Conceder derechos de acceso a la cuenta de inicio de sesión de servicio](granting-access-rights-to-the-service-logon-account.md).
-   Establecer privilegios. Asigne privilegios a la cuenta de inicio de sesión especificada, como el derecho para iniciar sesión como servicio en el equipo host. Para obtener más información, vea [Conceder inicio de sesión como derecho de servicio en el equipo host.](granting-logon-as-service-right-on-the-host-computer.md)

Una vez instalado un servicio, hay tareas de mantenimiento relacionadas con la cuenta de inicio de sesión del servicio. Para obtener más información, vea [Tareas de mantenimiento de cuentas de inicio de sesión](logon-account-maintenance-tasks.md).

-   Mantenimiento de contraseñas. Para un servicio que se ejecuta con una cuenta de usuario, debe cambiar periódicamente la contraseña y mantener la contraseña sincronizada con la contraseña usada por uno o varios administradores de control de servicios locales para iniciar el servicio.
-   Mantenimiento de SPN. Si cambia una cuenta de inicio de sesión de servicio, quite los SPN registrados en la cuenta anterior y regístrelos en la nueva cuenta. Tenga en cuenta que cuando se instala un servicio, un administrador de dominio puede cambiar la cuenta con la que se ejecuta el servicio. use funciones Win32 o la interfaz de usuario de la herramienta administrativa Administración de equipos.
-   Mantenimiento de ACE. Si cambia una cuenta de inicio de sesión de servicio, debe actualizar las AEE y las pertenencias a grupos para asegurarse de que el servicio puede seguir teniendo acceso a los recursos necesarios.

 

 