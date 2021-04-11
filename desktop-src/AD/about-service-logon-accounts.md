---
title: Acerca de las cuentas de inicio de sesión de servicio
description: Cuando se inicia un servicio basado en Win32, inicia sesión en el equipo local.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328b33d5dab36ccc5a803eb7c43ca3112e96ecf8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149155"
---
# <a name="about-service-logon-accounts"></a>Acerca de las cuentas de inicio de sesión de servicio

Cuando se inicia un servicio basado en Win32, inicia sesión en el equipo local. Puede iniciar sesión como:

-   Una cuenta de usuario local o de dominio.
-   La cuenta LocalSystem.

La cuenta de inicio de sesión determina la identidad de seguridad del servicio en tiempo de ejecución, es decir, el contexto de seguridad principal del servicio. El contexto de seguridad determina la capacidad del servicio de tener acceso a los recursos locales y de red. Por ejemplo, un servicio que se ejecuta en el contexto de seguridad de una cuenta de usuario local no puede tener acceso a los recursos de red. Por el contrario, un servicio que se ejecuta en el contexto de seguridad de la cuenta LocalSystem en un controlador de dominio (DC) de Windows 2000 tendría acceso sin restricciones al controlador de dominio. Para obtener más información y una explicación de las ventajas y las limitaciones entre las cuentas de usuario y LocalSystem, vea [contextos de seguridad y Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

En última instancia, los administradores del sistema donde está instalado el servicio tienen control sobre la cuenta de inicio de sesión del servicio. Por motivos de seguridad, es posible que algunos administradores no le permitan instalar el servicio con la cuenta LocalSystem. El servicio debe ser capaz de ejecutarse en una cuenta de usuario de dominio. Como programador, puede ejercer algún control sobre la cuenta de inicio de sesión del servicio. El instalador de servicio especifica la cuenta de inicio de sesión del servicio cuando llama a la función [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar el servicio en un equipo host. El instalador puede sugerir una cuenta de inicio de sesión predeterminada, pero debe permitir que un administrador especifique la cuenta real.

El instalador también puede realizar las siguientes tareas relacionadas con la cuenta de inicio de sesión del servicio:

-   Instalación. Si instala el servicio para que se ejecute en una cuenta de usuario, la cuenta debe existir antes de llamar a [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Puede usar una cuenta existente o crear una como parte de la installrt del equipo host. Para obtener más información, consulte [configuración de la cuenta de usuario de un servicio](setting-up-a-serviceampaposs-user-account.md).
-   Autenticación. Si desea que los clientes usen la autenticación mutua de Kerberos, registre los SPN en la cuenta de inicio de sesión del servicio. Si el servicio se ejecuta bajo la cuenta LocalSystem, la cuenta de inicio de sesión del servicio es la cuenta de equipo del equipo host. Para obtener más información, consulte [Service Principal Names](service-principal-names.md) (Nombres de entidad de seguridad de servicio).
-   Conceder acceso. Asegúrese de que el servicio en tiempo de ejecución tenga los derechos de acceso y los privilegios necesarios para realizar sus tareas. Esto puede requerir la configuración de entradas de control de acceso (ACE) en los descriptores de seguridad de varios recursos, que son objetos de directorio, recursos compartidos de archivos, etc., para permitir los derechos de acceso necesarios para la cuenta de usuario o equipo. Para obtener más información, consulte [conceder derechos de acceso a la cuenta de inicio de sesión del servicio](granting-access-rights-to-the-service-logon-account.md).
-   Establezca los privilegios. Asignar privilegios a la cuenta de inicio de sesión especificada, como el derecho de inicio de sesión como servicio en el equipo host. Para obtener más información, vea [conceder el derecho de inicio de sesión como servicio en el equipo host](granting-logon-as-service-right-on-the-host-computer.md).

Una vez instalado un servicio, hay tareas de mantenimiento relacionadas con la cuenta de inicio de sesión del servicio. Para obtener más información, consulte tareas de mantenimiento de la [cuenta de inicio de sesión](logon-account-maintenance-tasks.md).

-   Mantenimiento de contraseñas. Para un servicio que se ejecuta en una cuenta de usuario, debe cambiar periódicamente la contraseña y mantener la contraseña sincronizada con la contraseña usada por uno o más administradores de control de servicios locales para iniciar el servicio.
-   Mantenimiento de SPN. Si cambia una cuenta de inicio de sesión de servicio, quite los SPN registrados en la cuenta anterior y regístrelo en la nueva cuenta. Tenga en cuenta que cuando se instala un servicio, un administrador de dominio puede cambiar la cuenta en la que se ejecuta el servicio; Utilice las funciones de Win32 o la interfaz de usuario de la herramienta administrativa administración de equipos.
-   Mantenimiento de ACE. Si una cuenta de inicio de sesión de servicio cambia, debe actualizar las ACE y las pertenencias a grupos para asegurarse de que el servicio aún puede tener acceso a los recursos necesarios.

 

 