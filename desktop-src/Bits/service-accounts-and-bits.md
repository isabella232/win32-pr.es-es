---
title: Cuentas de servicio y BITS
description: Puede usar BITS para transferir archivos desde un servicio. El servicio debe usar la cuenta de sistema LocalSystem, LocalService o NetworkService. Estas cuentas siempre inician sesión; por lo tanto, los trabajos enviados por un servicio mediante estas cuentas siempre se ejecutan.
ms.assetid: 43fb58d6-3a99-488f-ab43-dbb4a794fc2f
keywords:
- BITS de cuentas de servicio
- transferir BITS de trabajo, propiedad, cuenta de servicio
- BITS de proxy, cuentas de servicio
- credenciales para transferir BITS de trabajo
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 475a623e6b105d3ef2bdc6586db613c010fe8923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149357"
---
# <a name="service-accounts-and-bits"></a>Cuentas de servicio y BITS

Puede usar BITS para transferir archivos desde un servicio. El servicio debe usar la cuenta de sistema LocalSystem, LocalService o NetworkService. Estas cuentas siempre inician sesión; por lo tanto, los trabajos enviados por un servicio mediante estas cuentas siempre se ejecutan.

Si un servicio que se ejecuta bajo una cuenta del sistema suplanta al usuario antes de llamar a BITS, BITS responde como lo haría con cualquier cuenta de usuario (por ejemplo, el usuario debe haber iniciado sesión en el equipo para que se produzca la transferencia). El servicio también debe utilizar la ocultación dinámica con los punteros de interfaz de BITS al suplantar al usuario. No se hereda el Cloaking, por lo que debe llamar a la función [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en cada puntero de interfaz que reciba desde bits (por ejemplo, el puntero de trabajo devuelto por la llamada al método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) ); no basta con establecer la ocultación en el puntero de la interfaz del administrador. También puede llamar a la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para el proceso en lugar de llamar a la función **CoSetProxyBlanket** en cada puntero de interfaz.

Sin embargo, si el servicio no suplanta al usuario, se aplican los comportamientos siguientes:

- Los trabajos creados por la cuenta de servicio pertenecen a esa cuenta. Dado que las cuentas del sistema siempre inician sesión, BITS transfiere los archivos siempre que el equipo se esté ejecutando y haya una conexión de red.
- Las cuentas del sistema no deben usar letras de unidad de red asignadas porque las letras de unidad son específicas de una sesión y la asignación puede perderse después de reiniciar el equipo.
- En ausencia de un [token auxiliar](helper-tokens-for-bits-transfer-jobs.md), la autenticación de red usa las credenciales de equipo para las cuentas LocalSystem y NetworkService y las credenciales anónimas para la cuenta LocalService. BITS devuelve "acceso denegado" si la lista de control de acceso (ACL) para el archivo de origen limita el acceso a una cuenta de usuario.
- Para obtener más información sobre cómo funciona la autenticación en presencia de un [token auxiliar](helper-tokens-for-bits-transfer-jobs.md), vea [autenticación](authentication.md).
- La configuración de proxy de Microsoft Internet Explorer se almacena por usuario y no se establece para las cuentas del sistema. Considere la posibilidad de configurar un token auxiliar en los trabajos de BITS o establecer explícitamente la configuración de proxy correcta mediante una llamada a [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la **\_ \_ \_ \_ invalidación del uso del proxy del trabajo de BG**. Como alternativa, puede usar los modificadores de **/util/SetIEProxy** de BitsAdmin.exe para establecer la configuración de proxy de Internet Explorer para la cuenta de sistema LocalSystem, LocalService o NetworkService. Para obtener más información, consulte la [herramienta BitsAdmin](bitsadmin-tool.md).

Tenga en cuenta que BITS no reconoce la configuración de proxy que se establece mediante el archivo de Proxycfg.exe.