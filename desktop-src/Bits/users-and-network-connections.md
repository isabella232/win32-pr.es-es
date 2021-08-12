---
title: Usuarios y conexiones de red
description: BITS transfiere archivos solo cuando el propietario del trabajo ha iniciado sesión y se establece una conexión de red.
ms.assetid: b31fc04f-8fa8-407f-9380-ca6b09589c46
keywords:
- BITS de conexiones de red
- transfer job BITS , ownership
- transferir bits de trabajo, propiedad, cuenta de usuario
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 54e346590cac90b8d896a9a45c86aee5ae241d7d299bb055cf9ff55db88b8668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679887"
---
# <a name="users-and-network-connections"></a>Usuarios y conexiones de red

BITS transfiere archivos solo cuando el propietario del trabajo ha iniciado sesión y se establece una conexión de red. BITS procesa el trabajo de transferencia mediante el contexto de seguridad del propietario del trabajo. El usuario que creó el trabajo se considera el propietario del trabajo. Sin embargo, un usuario con privilegios de administrador puede [**tomar posesión**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del trabajo de otro usuario.

BITS suspende un trabajo cuando el propietario cierra sesión o si se pierde la conexión de red (BITS no forzará una conexión de red). BITS reanuda el trabajo cuando el propietario vuelve a conectarse y se establece una conexión de red. Una vez establecida la conexión de red, puede producirse un breve retraso antes de que BITS comience a transferir datos.

Si se pierde la conexión de red, todos los trabajos cuyo estado sea [**BG \_ JOB STATE \_ \_ QUEUED**](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **BG JOB STATE \_ \_ \_ TRANSFERRING** se mueven al estado **BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR** con un código de error [BG E NETWORK \_ \_ \_ DISCONNECTED.](bits-return-values.md) Cuando se establece una conexión de red, todos los trabajos en estado BG JOB STATE TRANSIENT ERROR, que puede incluir cualquier código de **\_ \_ \_ \_ error,** se mueven al estado **BG JOB STATE \_ \_ \_ QUEUED.**

Para que BITS detecte que un usuario ha iniciado sesión, debe usar una de las siguientes opciones de inicio de sesión interactivo:

-   Inicie sesión a través del pantalla de inicio de sesión.
-   Inicie sesión en un [cliente de terminal](../termserv/terminal-services-portal.md) service.
-   Use [el cambio rápido de usuario](../shell/fast-user-switching.md).
-   A partir Windows 10, versión 1607, inicie sesión desde otro dispositivo mediante PowerShell remoto. Consulte [Para administrar sesiones remotas de PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md) para obtener más información.

Ejecutar una aplicación como otro usuario (mediante el comando **RunAs)** no es un inicio de sesión interactivo; BITS no ejecutará trabajos asociados al usuario especificado.

Las cuentas del sistema LocalSystem, LocalService y NetworkService siempre se inician sesión; por lo tanto, los trabajos enviados por un servicio que usan estas cuentas siempre se ejecutan. Para obtener información y limitaciones sobre el uso de cuentas de servicio, vea [Cuentas de servicio y BITS.](service-accounts-and-bits.md)

Los propietarios de trabajos pueden proporcionar un token auxiliar que se usará en situaciones en las que se necesitan varios tokens para completar una transferencia, como para la autenticación con un host remoto. Consulte [Tokens auxiliares para trabajos de transferencia de BITS](helper-tokens-for-bits-transfer-jobs.md) para obtener más información. En versiones anteriores de Windows, el propietario del trabajo tenía que tener privilegios de administrador para iniciar un trabajo que usaba un token auxiliar. En Windows 10, versión 1607, ahora es posible que un propietario del trabajo de BITS establezca tokens auxiliares sin ser administrador, siempre y cuando el token auxiliar no tenga funcionalidades de administrador. Esto reduce la superficie de vulnerabilidad de las herramientas de descarga o actualización en segundo plano, ya que permite que se ejecuten con la cuenta NetworkService con menos privilegios, en lugar de con una cuenta con privilegios administrativos.

Los usuarios con [un token restringido](../secauthz/restricted-tokens.md) (un token que contiene SID restricting) no pueden crear ni modificar trabajos.
 

 