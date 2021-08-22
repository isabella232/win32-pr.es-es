---
description: La cuenta LocalSystem es una cuenta local predefinida que usa el administrador de control de servicios.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Cuenta de LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d4dca5655402b3b4f400d3c1941ccf3978a7d385363567fac01a1d3024f1dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889446"
---
# <a name="localsystem-account"></a>Cuenta de LocalSystem

La cuenta LocalSystem es una cuenta local predefinida que usa el administrador de control de servicios. El subsistema de seguridad no reconoce esta cuenta, por lo que no puede especificar su nombre en una llamada a la [**función LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) Tiene amplios privilegios en el equipo local y actúa como el equipo en la red. Su token incluye los SID NT AUTHORITY SYSTEM y \\ BUILTIN Administrators; estas cuentas tienen acceso a la mayoría \\ de los objetos del sistema. El nombre de la cuenta en todas las configuraciones regionales es . \\ Localsystem. También se puede usar el nombre, LocalSystem o *NombreDeEquipo* \\ LocalSystem. Esta cuenta no tiene una contraseña. Si especifica la cuenta LocalSystem en una llamada a la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig,**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) se omite cualquier información de contraseña que proporcione.

Un servicio que se ejecuta en el contexto de la cuenta LocalSystem hereda el contexto de seguridad del SCM. El SID del usuario se crea a partir del valor **DE RID DEL SISTEMA LOCAL DE \_ \_ \_ SEGURIDAD.** La cuenta no está asociada a ninguna cuenta de usuario que haya iniciado sesión. Esto implica lo siguiente:

-   La clave del **Registro HKEY \_ CURRENT \_ USER** está asociada al usuario predeterminado, no al usuario actual. Para acceder al perfil de otro usuario, suplante al usuario y, a continuación, acceda **a HKEY \_ CURRENT \_ USER**.
-   El servicio puede abrir la clave del Registro **HKEY \_ LOCAL MACHINE \_ \\ SECURITY**.
-   El servicio presenta las credenciales del equipo a los servidores remotos.
-   Si el servicio abre una ventana de comandos y ejecuta un archivo por lotes, el usuario podría presionar CTRL+C para finalizar el archivo por lotes y obtener acceso a una ventana de comandos con permisos LocalSystem.

La cuenta LocalSystem tiene los siguientes privilegios:

-   **SE \_ ASSIGNPRIMARYTOKEN \_ NAME** (deshabilitado)
-   **SE \_ AUDIT \_ NAME** (habilitado)
-   **SE \_ BACKUP \_ NAME** (deshabilitado)
-   **SE \_ CAMBIAR \_ NOMBRE \_ DE NOTIFICACIÓN** (habilitado)
-   **SE \_ CREATE \_ GLOBAL \_ NAME** (habilitado)
-   **SE \_ CREATE \_ PAGEFILE \_ NAME** (habilitado)
-   **SE \_ CREATE \_ PERMANENT \_ NAME** (habilitado)
-   **SE \_ CREATE \_ TOKEN \_ NAME** (deshabilitado)
-   **SE \_ NOMBRE \_ DE DEPURACIÓN** (habilitado)
-   **SE \_ IMPERSONATE \_ NAME** (habilitado)
-   **SE \_ INC \_ BASE \_ PRIORITY \_ NAME** (habilitado)
-   **SE \_ INCREASE \_ QUOTA \_ NAME (deshabilitado)**
-   **SE \_ LOAD \_ DRIVER \_ NAME (deshabilitado)**
-   **SE \_ LOCK \_ MEMORY \_ NAME** (habilitado)
-   **SE \_ MANAGE \_ VOLUME \_ NAME** (deshabilitado)
-   **SE \_ NOMBRE \_ DE PROCESO ÚNICO \_ \_ DE PROF** (habilitado)
-   **SE \_ RESTORE \_ NAME** (deshabilitado)
-   **SE \_ NOMBRE \_ DE SEGURIDAD** (deshabilitado)
-   **SE \_ SHUTDOWN \_ NAME (deshabilitado)**
-   **SE \_ NOMBRE \_ DEL ENTORNO DEL \_ SISTEMA** (deshabilitado)
-   **SE \_ SYSTEMTIME \_ NAME** (deshabilitado)
-   **SE \_ TAKE \_ OWNERSHIP \_ NAME (deshabilitado)**
-   **SE \_ TCB \_ NAME** (habilitado)
-   **SE \_ UNDOCK \_ NAME (deshabilitado)**

La mayoría de los servicios no necesitan un nivel de privilegio tan alto. Si el servicio no necesita estos privilegios y no es un servicio interactivo, considere la posibilidad de usar la cuenta [LocalService](localservice-account.md) o [la cuenta networkService](networkservice-account.md). Para obtener más información, vea [Service Security and Access Rights](service-security-and-access-rights.md).

 

 
