---
title: Bloqueo de comandos
description: Para conservar la integridad de las operaciones, el software no puede ejecutar determinados comandos de TPM en la plataforma.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243819"
---
# <a name="command-blocking"></a>Bloqueo de comandos

Para conservar la integridad de las operaciones, el software no puede ejecutar determinados comandos de TPM en la plataforma. Por ejemplo, algunos comandos solo los ejecuta el software del sistema. Cuando el TBS bloquea un comando, se devuelve un error según corresponda. De forma predeterminada, TBS bloquea los comandos que podrían afectar a la privacidad, la seguridad y la estabilidad del sistema. El TBS también supone que otras partes de la pila de software pueden restringir el acceso a determinados comandos a entidades autorizadas.

Para los comandos de la versión 1.2 de TPM, hay tres listas de comandos bloqueados: una lista controlada por la directiva de grupo, una lista controlada por administradores locales y una lista predeterminada. Un comando tpm se bloquea si se encuentra en cualquiera de las listas. Sin embargo, hay marcas de directiva de grupo para permitir que el TBS ignore la lista local y la lista predeterminada. Las marcas de directiva de grupo se pueden editar directamente o tener acceso a través del Editor de objetos de directiva de grupo.

> [!Note]  
> La lista de comandos bloqueados localmente no se conserva después de una actualización al sistema operativo. Se conservan los comandos que están bloqueados en directiva de grupo lista de comandos.

 

En el caso de los comandos de la versión 2.0 de TPM, se invierte la lógica para el bloqueo; usa una lista de comandos permitidos. Esta lógica bloqueará automáticamente los comandos que no se conocían cuando se hizo la lista por primera vez. Cuando se agregan comandos a la especificación de TPM después de que se haya enviado una versión de Windows, estos nuevos comandos se bloquean automáticamente. Solo una actualización del Registro agregará estos nuevos comandos a la lista de comandos permitidos.

A partir de Windows 10 1809 (Windows Server 2019), los comandos TPM 2.0 permitidos ya no se pueden manipular mediante la configuración del Registro. Para estas Windows 10, los comandos TPM 2.0 permitidos se fijan en el controlador TPM. Los comandos de TPM 1.2 todavía se pueden bloquear y desbloquear mediante cambios en el Registro. 

## <a name="direct-registry-access"></a>Acceso directo al registro

Las directiva de grupo están en la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Tpm** \\ **BlockedCommands**.

Para determinar qué listas se deben usar para bloquear comandos TPM, hay dos valores **DWORD** que se usan como marcas booleanas:

-   "IgnoreDefaultList"

    Si se establece (el valor existe y es distinto de cero), el TBS omite la lista predeterminada de comandos bloqueados.

-   "IgnoreLocalList"

    Si se establece (el valor existe y es distinto de cero), el TBS omite la lista local blocked-commands.

## <a name="group-policy-object-editor"></a>Editor de objetos de directiva de grupo

**Para acceder al editor directiva de grupo objetos**

1.  Haga clic en **Iniciar**.
2.  Haga clic en **Ejecutar**.
3.  En el cuadro **Abrir** , escriba **gpedit.msc**. Haga clic en **OK**. Se abre directiva de grupo editor de objetos.
4.  Expanda **Configuración del equipo.**
5.  Expanda **Plantillas administrativas**.
6.  Expanda **Sistema**.
7.  Expanda **Módulo de plataforma segura Services**.

Las listas de comandos TPM1.2 bloqueados específicos se pueden editar directamente en las siguientes ubicaciones.

-   Lista de directivas de grupo:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   Lista local:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   Lista predeterminada:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

En cada una de estas claves del Registro, hay una lista de valores del Registro de tipo REG \_ SZ. Cada valor representa un comando TPM bloqueado. Cada clave del Registro tiene un campo "Nombre de valor" y un campo "Datos de valor". Ambos campos ("Nombre de valor" y "Datos de valor"), deben coincidir exactamente con el valor decimal del ordinal del comando TPM que se va a bloquear.

La lista de comandos de TPM 2.0 permitidos específicos se puede editar directamente en la siguiente ubicación. En la clave del Registro, hay una lista de valores del Registro de tipo REG \_ DWORD. Cada valor representa un comando TPM 2.0 permitido. Cada valor del Registro tiene **un nombre** y un **campo de** valor. El **nombre** coincide con el ordinal de comandos de TPM 2.0 hexadecimal que se debe permitir. El **valor** tiene un valor de 1 si se permite el comando. Si un ordinal de comando no está presente o tiene un valor de 0, el comando se bloqueará.

-   Lista predeterminada:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Por Windows 8, Windows Server 2012 y posteriores, las claves del Registro **BlockedCommands** y **AllowedW8Commands** determinan respectivamente los comandos TPM bloqueados o permitidos para las cuentas de administrador. Las cuentas de usuario tienen una lista de comandos TPM bloqueados o permitidos en las claves del Registro **BlockedUserCommands** y **AllowedW8UserCommands,** respectivamente. En Windows 10, versión 1607, se han introducido nuevas claves del Registro para las aplicaciones AppContainer: **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands**.

 

 




