---
title: Usuarios y conexiones de red
description: BITS transfiere archivos solo cuando el propietario del trabajo inicia sesión y se establece una conexión de red.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- BITS de conexiones de red
- transferir BITS de trabajo, propiedad
- transferir BITS de trabajo, propiedad, cuenta de usuario
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7f841e3bf92004b62f3bbb576f71a45ac6b4a6bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149572"
---
# <a name="users-and-network-connections"></a>Usuarios y conexiones de red

BITS transfiere archivos solo cuando el propietario del trabajo inicia sesión y se establece una conexión de red. BITS procesa el trabajo de transferencia mediante el contexto de seguridad del propietario del trabajo. El usuario que creó el trabajo se considera el propietario del trabajo. Sin embargo, un usuario con privilegios de administrador puede [**tomar posesión**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del trabajo de otro usuario.

BITS suspende un trabajo cuando el propietario cierra la sesión o si se pierde la conexión de red (BITS no forzará una conexión de red). BITS reanuda el trabajo cuando el propietario vuelve a iniciar sesión y se establece una conexión de red. Una vez establecida la conexión de red, se puede producir un breve retraso antes de que BITS empiece a transferir datos.

Si se pierde la conexión de red, todos los trabajos cuyo estado es [**Estado de trabajo de BG \_ \_ \_ en cola**](/windows/desktop/api/Bits/ne-bits-bg_job_state) o estado de trabajo de BG que se **\_ \_ \_ transfieren** se mueven al estado de **\_ \_ \_ \_ error transitorio de estado de trabajo de BG** con un código de error de [red BG \_ E \_ \_ desconectado](bits-return-values.md) . Cuando se establece una conexión de red, todos los trabajos en un estado de **\_ \_ \_ \_ error transitorio de estado de trabajo de BG** , que puede incluir cualquier código de error, se mueven al estado de trabajo de BG en **\_ \_ \_ cola** .

Para que BITS detecte que un usuario ha iniciado sesión, el usuario debe usar una de las siguientes opciones de inicio de sesión interactivo:

-   Inicie sesión a través de la pantalla de bienvenida.
-   Inicie sesión en un cliente de [Terminal Services](../termserv/terminal-services-portal.md) .
-   Usar [cambio rápido de usuario](../shell/fast-user-switching.md).
-   A partir de Windows 10, versión 1607, inicie sesión desde otro dispositivo mediante PowerShell remoto. Vea [para administrar sesiones remotas de PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md) para obtener más información.

La ejecución de una aplicación como otro usuario (mediante el comando **runas** ) no es un inicio de sesión interactivo; BITS no ejecutará los trabajos asociados al usuario especificado.

Las cuentas del sistema LocalSystem, LocalService y NetworkService siempre inician sesión. por lo tanto, los trabajos enviados por un servicio mediante estas cuentas siempre se ejecutan. Para obtener información y conocer las limitaciones sobre el uso de cuentas de servicio, vea [Service accounts and bits](service-accounts-and-bits.md).

Los propietarios de los trabajos pueden proporcionar un token auxiliar que se usará en situaciones en las que se necesitan varios tokens para completar una transferencia, por ejemplo, para la autenticación con un host remoto. Consulte [tokens de aplicación auxiliar para trabajos de transferencia de bits](helper-tokens-for-bits-transfer-jobs.md) para más información. En versiones anteriores de Windows, el propietario del trabajo tenía que tener privilegios de administrador para iniciar un trabajo que usaba un token de aplicación auxiliar. En Windows 10, versión 1607, ahora es posible que un propietario del trabajo de BITS establezca tokens auxiliares sin ser un administrador, siempre que el token auxiliar no tenga funciones de administrador. Esto reduce la superficie de vulnerabilidad de las herramientas de descarga o actualización en segundo plano, ya que permite que se ejecuten con la cuenta NetworkService con menos privilegios, en lugar de con una cuenta con privilegios administrativos.

Los usuarios con un [token restringido](../secauthz/restricted-tokens.md) (un token que contenga SID restrictivos) no pueden crear ni modificar trabajos.
 

 