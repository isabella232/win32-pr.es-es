---
title: AppIDFlags
description: Conjunto de marcas que controlan el comportamiento de activación de un servidor COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valor del Registro AppIDFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ecf7d0d112d2ceff913f3de6250c130e16455c1810cc6234db63a6aaf463fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048873"
---
# <a name="appidflags"></a>AppIDFlags

Conjunto de marcas que controlan el comportamiento de activación de un servidor COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor de marca | Constante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND |
| 0x4        | APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP Description

Si la marca **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** está desactivada en **AppIDFlags** o si **AppIDFlags** no está presente, el cliente de una sesión de terminal Server que realiza una solicitud de activación para un servidor [COM](interactive-user.md) de usuario interactivo se enlazará al servidor COM o se iniciará y enlazará al servidor COM en el escritorio "predeterminado" de la estación de ventana "winsta0" [](/windows/desktop/winstation/window-stations) de la sesión en la solicitud de activación. Por ejemplo, si el cliente ejecuta "winsta0 desktop1" de la sesión 3, la solicitud de activación de la sesión 3 se enlazará o iniciará y enlazará al servidor COM en "winsta0 default" de la sesión 3, incluso si una instancia del servidor COM ya se está ejecutando en \\ \\ "winsta0 desktop1" de la sesión \\ 3.

Si la marca **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** está establecida en el valor **AppIDFlags,** COM enlazará o iniciará y enlazará al proceso de servidor que se ejecuta en el escritorio del cliente y la sesión en la solicitud de activación. Por ejemplo, si el cliente ejecuta "winsta0 desktop1" en la sesión 3, la solicitud de activación de la sesión 3 se enlazará al servidor COM en "winsta0 desktop1" en la sesión 3, o se iniciará y enlazará al servidor COM en la sesión 3, incluso si una instancia del servidor COM ya se está ejecutando en \\ "winsta0 default" en la sesión \\ \\ 3.

El cliente puede usar el [moniker de](/windows/desktop/TermServ/session-monikers) sesión para especificar una sesión diferente de la sesión del cliente cuando realiza la solicitud de activación.

La **marca APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** solo se aplica a los servidores COM configurados como RunAs "[Interactive User](interactive-user.md)".

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND Description

Si la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** está establecida en **AppIDFlags,** los servidores COM configurados para RunAs "Activator" se iniciarán con un descriptor de seguridad de proceso que permita EL ACCESO DE [PROCESS \_ ALL \_](/windows/desktop/ProcThread/process-security-and-access-rights) al SID logonID del token de proceso. Además, el propietario del descriptor de seguridad se establecerá en el SID logonID del token de proceso.

Si la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** está establecida en **AppIDFlags,** los servidores COM configurados para RunAs "This User" se iniciarán con un descriptor de seguridad de proceso que permita EL ACCESO A PROCESS [ \_ ALL \_](/windows/desktop/ProcThread/process-security-and-access-rights) en el SID logonID del token de proceso. Además, el propietario del descriptor de seguridad se establecerá en el SID logonID del token de proceso. Además, el Administrador de control de servicios COM (SCM) modifica el token del proceso del servidor COM como se indica a continuación:

-   Agrega un SID de APPID al token. Concede al SID de APPID acceso completo en la lista de control de acceso discrecional (DACL) predeterminada del token. En Windows Vista y versiones posteriores de Windows, concede el permiso OWNERRights SID READ CONTROL en la \_ DACL predeterminada del token. En versiones anteriores Windows Vista de Windows, establece el propietario del token en el SID de APPID.

Las siguientes consideraciones de seguridad deben tenerse en cuenta al usar la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND:**

-   La marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** está diseñada para establecerse mediante servidores COM que se inician en uno de los contextos de seguridad del servicio integrados; ya sea las cuentas NetworkService o LocalService. Si los servidores suplantan a clientes con privilegios y no se establece la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND,** el código malintencionado que se ejecuta en otros procesos con el mismo contexto de seguridad puede elevar los privilegios mediante el secuestro de los tokens de suplantación de los clientes con privilegios del proceso del servidor COM.
-   Cuando se establece la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND,** COM protege el descriptor de seguridad del objeto de proceso en el caso de los servidores COM RunAs "Activator". Para estos servidores, se espera que el cliente COM resalte el token que usa para la activación COM.
-   Cuando se establece la marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND,** COM protege el descriptor de seguridad del objeto de proceso en el caso de los servidores COM RunAs "This User". También se resalte el token de proceso del servidor COM, ya que el SCM COM es la entidad que crea el token.

La marca **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** solo se admite en Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008 cuando se aplica la revisión MSRC8322 (boletín de seguridad [MS09-012).](https://support.microsoft.com/kb/959454) Se admite de forma nativa en Windows 7 y versiones posteriores de Windows.

La **marca APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** solo se aplica a los servidores COM configurados para RunAs "Activator" o "This User". No se aplica a los servidores COM que son servicios NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY Description

Si la marca **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** está establecida en **AppIDFlags,** el SCM COM emitirá solicitudes de activación de objetos al proceso del servidor COM mediante un nivel de suplantación [de RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY](impersonation-levels.md).

Si no se establece la marca **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY,** el SCM com emitirá solicitudes de activación de objetos a los procesos del servidor COM mediante un nivel de suplantación de [RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE](impersonation-levels.md).

Se deben tener en cuenta las siguientes consideraciones de seguridad al usar la marca **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY:**

-   La **marca APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** está pensada para que la usen los servidores COM que no realizan el trabajo en nombre de los clientes en las solicitudes de activación de objetos. En el caso de estos servidores, si el SCM COM emite solicitudes de activación de objetos en [RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY,](impersonation-levels.md) se minimizan las posibilidades de que aparezcan tokens con privilegios con SE nivel [**\_ IMPERSONATE \_ NAME**](/windows/desktop/SecAuthZ/privilege-constants) en el proceso.

La **marca APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** se admite en Windows 7 y versiones posteriores de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritorios](/windows/desktop/winstation/desktops)
</dt> <dt>

[Niveles de suplantación](impersonation-levels.md)
</dt> <dt>

[Usuario interactivo](interactive-user.md)
</dt> <dt>

[Monikers de sesión](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Estaciones de ventana](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 