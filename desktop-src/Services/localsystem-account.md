---
description: La cuenta LocalSystem es una cuenta local predefinida utilizada por el administrador de control de servicios.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Cuenta LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001032"
---
# <a name="localsystem-account"></a>Cuenta LocalSystem

La cuenta LocalSystem es una cuenta local predefinida utilizada por el administrador de control de servicios. El subsistema de seguridad no reconoce esta cuenta, por lo que no puede especificar su nombre en una llamada a la función [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Tiene muchos privilegios en el equipo local y actúa como el equipo de la red. Su token incluye el sistema de autoridad NT \\ y los \\ SID de administradores integrados; estas cuentas tienen acceso a la mayoría de los objetos del sistema. El nombre de la cuenta en todas las configuraciones regionales es. \\ LocalSystem. También se puede usar el nombre, LocalSystem o *ComputerName* \\ LocalSystem. Esta cuenta no tiene contraseña. Si especifica la cuenta LocalSystem en una llamada a la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , se omitirá cualquier información de contraseña que proporcione.

Un servicio que se ejecuta en el contexto de la cuenta LocalSystem hereda el contexto de seguridad del SCM. El SID de usuario se crea a partir del valor de **\_ \_ \_ RID del sistema local de seguridad** . La cuenta no está asociada a ninguna cuenta de usuario que haya iniciado sesión. Esto implica lo siguiente:

-   La clave del registro **HKEY \_ Current \_ User** está asociada al usuario predeterminado, no al usuario actual. Para tener acceso a otro perfil de usuario, suplantar al usuario y después acceder a **HKEY \_ Current \_ User**.
-   El servicio puede abrir la clave del registro **HKEY \_ local \_ Machine \\ Security**.
-   El servicio presenta las credenciales del equipo a los servidores remotos.
-   Si el servicio abre una ventana de comandos y ejecuta un archivo por lotes, el usuario podría presionar CTRL + C para finalizar el archivo por lotes y obtener acceso a una ventana de comandos con permisos de LocalSystem.

La cuenta LocalSystem tiene los siguientes privilegios:

-   **Se \_ \_Nombre de ASSIGNPRIMARYTOKEN** (deshabilitado)
-   **Se \_ \_Nombre de auditoría** (habilitado)
-   **Se \_ \_Nombre de copia de seguridad** (deshabilitado)
-   **Se \_ CAMBIAR \_ \_ el nombre** de la notificación (habilitado)
-   **Se \_ CREAR \_ \_ nombre global** (habilitado)
-   **Se \_ CREAR \_ \_ nombre** de archivo de paginación (habilitado)
-   **Se \_ CREAR \_ \_ nombre permanente** (habilitado)
-   **Se \_ CREAR \_ \_ nombre de token** (deshabilitado)
-   **Se \_ \_Nombre de DEpuración** (habilitado)
-   **Se \_ \_Nombre de SUplantación** (habilitado)
-   **Se \_ \_Nombre de \_ prioridad \_ base de Inc** (habilitado)
-   **Se \_ AUMENTAR \_ \_ el nombre** de la cuota (deshabilitado)
-   **Se \_ CARGAR \_ \_ el nombre del controlador** (deshabilitado)
-   **Se \_ \_ \_ Nombre de memoria de bloqueo** (habilitado)
-   **Se \_ ADMINISTRAR \_ \_ el nombre del volumen** (deshabilitado)
-   **Se \_ \_Nombre de \_ proceso \_ único de Prof** (habilitado)
-   **Se \_ \_Nombre de restauración** (deshabilitado)
-   **Se \_ \_Nombre de seguridad** (deshabilitado)
-   **Se \_ \_Nombre de apagado** (deshabilitado)
-   **Se \_ \_ \_ Nombre del entorno del sistema** (deshabilitado)
-   **Se \_ \_Nombre de SYSTEMTIME** (deshabilitado)
-   **Se \_ TOMAR \_ \_ el nombre** de la propiedad (deshabilitado)
-   **Se \_ \_Nombre de TCB** (habilitado)
-   **Se \_ \_Nombre de desacoplamiento** (deshabilitado)

La mayoría de los servicios no necesitan un nivel de privilegios elevado. Si el servicio no necesita estos privilegios y no es un servicio interactivo, considere la posibilidad de usar la [cuenta LocalService](localservice-account.md) o la [cuenta NetworkService](networkservice-account.md). Para obtener más información, consulte [seguridad del servicio y derechos de acceso](service-security-and-access-rights.md).

 

 
