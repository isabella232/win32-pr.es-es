---
title: Bloqueo de comandos
description: Para conservar la integridad de las operaciones, el software de la plataforma no puede ejecutar determinados comandos de TPM.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104420496"
---
# <a name="command-blocking"></a>Bloqueo de comandos

Para conservar la integridad de las operaciones, el software de la plataforma no puede ejecutar determinados comandos de TPM. Por ejemplo, algunos comandos solo se ejecutan mediante software del sistema. Cuando el TBS bloquea un comando, se devuelve un error según corresponda. De forma predeterminada, TBS bloquea los comandos que podrían afectar a la privacidad, la seguridad y la estabilidad del sistema. TBS también presupone que otras partes de la pila de software pueden restringir el acceso a determinados comandos a las entidades autorizadas.

En el caso de los comandos de la versión 1,2 de TPM, hay tres listas de comandos bloqueados: una lista controlada por la Directiva de grupo, una lista controlada por administradores locales y una lista predeterminada. Un comando de TPM se bloquea si está en cualquiera de las listas. Sin embargo, hay marcas de directiva de grupo que permiten a TBS omitir la lista local y la lista predeterminada. Las marcas de directiva de grupo se pueden editar directamente o se puede obtener acceso a ellas mediante el Editor de objetos de directiva de grupo.

> [!Note]  
> La lista de comandos bloqueados localmente no se conserva después de una actualización al sistema operativo. Se conservan los comandos bloqueados en la lista de directiva de grupo.

 

En el caso de los comandos de la versión 2,0 de TPM, se invierte la lógica para el bloqueo; usa una lista de comandos permitidos. Esta lógica bloqueará automáticamente los comandos que no se conocían cuando la lista se realizó por primera vez. Cuando se agregan comandos a la especificación de TPM después de que se haya enviado una versión de Windows, estos nuevos comandos se bloquean automáticamente. Solo una actualización del registro agregará estos nuevos comandos a la lista de comandos permitidos.

A partir de Windows 10 1809 (Windows Server 2019), los comandos de TPM 2,0 permitidos ya no se pueden manipular a través de la configuración del registro. Para estas versiones de Windows 10, los comandos de TPM 2,0 permitidos se han corregido en el controlador de TPM. Los comandos de TPM 1,2 se pueden bloquear y desbloquear a través de los cambios del registro. 

## <a name="direct-registry-access"></a>Acceso directo al registro

Las marcas de directiva de grupo se encuentran en la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.

Para determinar qué listas deben usarse para bloquear comandos de TPM, hay dos valores **DWORD** que se usan como marcas booleanas:

-   "IgnoreDefaultList"

    Si se establece (el valor existe y es distinto de cero), TBS omite la lista de comandos bloqueados predeterminada.

-   "IgnoreLocalList"

    Si se establece (el valor existe y es distinto de cero), TBS omite la lista local de comandos bloqueados.

## <a name="group-policy-object-editor"></a>Editor de objetos de directiva de grupo

**Para tener acceso al editor de objetos de directiva de grupo**

1.  Haga clic en **Iniciar**.
2.  Haga clic en **Ejecutar**.
3.  En el cuadro **Abrir** , escriba **gpedit.msc**. Haga clic en **OK**. Se abre el editor de objetos de directiva de grupo.
4.  Expanda **configuración del equipo**.
5.  Expanda **plantillas administrativas**.
6.  Expanda **sistema**.
7.  Expanda **módulo de plataforma segura Services**.

Las listas de comandos de TPM 1.2 bloqueados específicos se pueden editar directamente en las siguientes ubicaciones.

-   Lista de directivas de Grupo:

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

En cada una de estas claves del registro hay una lista de valores de registro de \_ tipo REG SZ. Cada valor representa un comando de TPM bloqueado. Cada clave del registro tiene un campo "nombre del valor" y un campo "datos del valor". Ambos campos ("nombre del valor" y "datos del valor"), deben coincidir exactamente con el valor decimal del ordinal del comando TPM que se va a bloquear.

La lista de comandos de TPM 2,0 específicos permitidos se puede editar directamente en la siguiente ubicación. En la clave del registro hay una lista de valores de registro de \_ tipo REG DWORD. Cada valor representa un comando de TPM 2,0 permitido. Cada valor del registro tiene un **nombre** y un campo de **valor** . El **nombre** coincide con el ordinal del comando TPM 2,0 hexadecimal que se debe permitir. El **valor** tiene un valor de 1 si se permite el comando. Si el ordinal de un comando no está presente o tiene un valor de 0, se bloqueará el comando.

-   Lista predeterminada:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

En Windows 8, Windows Server 2012 y versiones posteriores, las claves del registro **BlockedCommands** y **AllowedW8Commands** determinan respectivamente los comandos de TPM bloqueados o permitidos para las cuentas de administrador. Las cuentas de usuario tienen una lista de comandos de TPM bloqueados o permitidos en las claves del registro **BlockedUserCommands** y **AllowedW8UserCommands** , respectivamente. En Windows 10, versión 1607, se han incorporado nuevas claves del registro para las aplicaciones AppContainer: **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands**.

 

 




