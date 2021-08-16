---
title: Cuentas de servicio y BITS
description: Puede usar BITS para transferir archivos desde un servicio. El servicio debe usar la cuenta del sistema LocalSystem, LocalService o NetworkService. Estas cuentas siempre han iniciado sesión; Por lo tanto, los trabajos enviados por un servicio que usan estas cuentas siempre se ejecutan.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- BITS de cuentas de servicio
- transferir bits de trabajo, propiedad, cuenta de servicio
- proxy BITS, cuentas de servicio
- credenciales para transferir bits de trabajo
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: a996471afefb00b0dea87b07f477f5cab2fd29352c567dc9182fcf28fa5b168a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679907"
---
# <a name="service-accounts-and-bits"></a>Cuentas de servicio y BITS

Puede usar BITS para transferir archivos desde un servicio. El servicio debe usar la cuenta del sistema LocalSystem, LocalService o NetworkService. Estas cuentas siempre han iniciado sesión; Por lo tanto, los trabajos enviados por un servicio que usan estas cuentas siempre se ejecutan.

Si un servicio que se ejecuta con una cuenta del sistema suplanta al usuario antes de llamar a BITS, BITS responde como lo haría con cualquier cuenta de usuario (por ejemplo, el usuario debe iniciar sesión en el equipo para que se produzca la transferencia). El servicio también debe usar el arroba dinámico con los punteros de interfaz BITS al suplantar al usuario. La ocultación no se hereda, por lo que debe llamar a la función [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en cada puntero de interfaz que reciba de BITS (por ejemplo, el puntero de trabajo devuelto al llamar al método [**IBackgroundCopyManager::CreateJob);**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) no basta con establecer el arroba en el puntero de la interfaz de administrador. También puede llamar a la [**función CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para el proceso en lugar de llamar a la **función CoSetProxyBlanket** en cada puntero de interfaz.

Sin embargo, si el servicio no suplanta al usuario, se aplican los comportamientos siguientes:

- Los trabajos creados por la cuenta de servicio son propiedad de esa cuenta. Dado que las cuentas del sistema siempre han iniciado sesión, BITS transfiere los archivos siempre que el equipo se esté ejecutando y haya una conexión de red.
- Las cuentas del sistema no deben usar letras de unidad de red asignadas porque las letras de unidad son específicas de una sesión y la asignación puede perderse después de reiniciar el equipo.
- En ausencia de un [token](helper-tokens-for-bits-transfer-jobs.md)auxiliar, la autenticación de red usa credenciales de equipo para las cuentas LocalSystem y NetworkService y credenciales anónimas para la cuenta LocalService. BITS devuelve "acceso denegado" si la lista de control de acceso (ACL) del archivo de origen limita el acceso a una cuenta de usuario.
- Para obtener más información sobre cómo funciona la autenticación en presencia de un [token auxiliar,](helper-tokens-for-bits-transfer-jobs.md)vea [Autenticación](authentication.md).
- La configuración Internet Explorer proxy de Microsoft se almacena por usuario y no se establece para las cuentas del sistema. Considere la posibilidad de configurar un token auxiliar en los trabajos de BITS o establecer explícitamente la configuración de proxy correcta mediante una llamada a [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG JOB PROXY USAGE \_ \_ \_ \_ OVERRIDE**. Como alternativa, puede usar los modificadores **/Util /SetIEProxy** de BitsAdmin.exe Internet Explorer para establecer una configuración de proxy para la cuenta del sistema LocalSystem, LocalService o NetworkService. Para obtener más información, [vea BitsAdmin Tool](bitsadmin-tool.md).

Tenga en cuenta que BITS no reconoce la configuración de proxy que se establece mediante Proxycfg.exe archivo.