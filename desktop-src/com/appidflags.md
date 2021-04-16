---
title: AppIDFlags
description: Un conjunto de marcas que controlan el comportamiento de activación de un servidor COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valor del registro AppIDFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714481"
---
# <a name="appidflags"></a>AppIDFlags

Un conjunto de marcas que controlan el comportamiento de activación de un servidor COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Valor de marca | Constante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ activar \_ IUSERVER \_ indesktop          |
| 0x2        | APPIDREGFLAGS \_ \_ \_ de proceso de servidor seguro \_ SD \_ y \_ BIND |
| 0x4        | APPIDREGFLAGS \_ emitir \_ \_ RPC \_ de activación a la \_ identificación   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ activar \_ la \_ Descripción de indesktop de IUSERVER

Si la marca **APPIDREGFLAGS \_ Activar IUSERVER de \_ \_ escritorio** está desactivada en **AppIDFlags** o si **AppIDFlags** no está presente, el cliente de una sesión de Terminal Server que realiza una solicitud de activación para un servidor com de [usuario interactivo](interactive-user.md) enlazará o iniciará el servidor com en el escritorio "predeterminado" de la [estación de ventana](/windows/desktop/winstation/window-stations) "winsta0" de la sesión en la solicitud de activación. Por ejemplo, si el cliente ejecuta "winsta0 \\ desktop1" de la sesión 3, la solicitud de activación de la sesión 3 enlazará o iniciará el servidor com en "winsta0 \\ default" de la sesión 3, aunque ya se esté ejecutando una instancia del servidor com en "winsta0 \\ desktop1" de la sesión 3.

Si la marca **APPIDREGFLAGS \_ Activar IUSERVER de \_ \_ escritorio** está establecida en el valor **AppIDFlags** , com se enlazará con el proceso de servidor que se ejecuta en el escritorio del cliente, o se iniciará y enlazará con él, y la sesión en la solicitud de activación. Por ejemplo, si el cliente ejecuta "winsta0 \\ desktop1" en la sesión 3, la solicitud de activación de la sesión 3 enlazará o iniciará el servidor com en "winsta0 \\ desktop1" en la sesión 3, incluso si ya se está ejecutando una instancia del servidor com en "winsta0 \\ default" en la sesión 3.

El cliente puede utilizar el [moniker](/windows/desktop/TermServ/session-monikers) de la sesión para especificar una sesión diferente a la sesión del cliente cuando realiza la solicitud de activación.

La marca **APPIDREGFLAGS \_ Activar IUSERVER de \_ \_ escritorio** solo se aplica a los servidores com que están configurados para runas "[usuario interactivo](interactive-user.md)".

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>\_ \_ \_ \_ \_ Descripción de enlace y SD de APPIDREGFLAGS Secure Server Process \_

Si se establece la marca de **\_ \_ \_ \_ \_ \_ enlace y SD de APPIDREGFLAGS Secure Server Process** en **AppIDFlags**, los servidores com que estén configurados para runas "Activator" se iniciarán con un descriptor de seguridad de proceso que permita [procesar \_ todo el \_ acceso](/windows/desktop/ProcThread/process-security-and-access-rights) al SID de LogonID del token de proceso. Además, el propietario del descriptor de seguridad se establecerá en el SID de LogonID del token de proceso.

Si la marca de **\_ \_ \_ \_ \_ enlace SD and \_ BIND del proceso de servidor seguro APPIDREGFLAGS** se establece en **AppIDFlags**, los servidores com configurados para runas "este usuario" se iniciarán con un descriptor de seguridad de proceso que permita [procesar todo el \_ \_ acceso](/windows/desktop/ProcThread/process-security-and-access-rights) en el SID de LogonID del token de proceso. Además, el propietario del descriptor de seguridad se establecerá en el SID de LogonID del token de proceso. Además, el administrador de control de servicios (SCM) COM modifica el token del proceso de servidor COM de la siguiente manera:

-   Agrega un SID de APPID al token. Concede el acceso completo del SID de APPID en la lista de control de acceso discrecional (DACL) predeterminada del token. En Windows Vista y versiones posteriores de Windows, concede el permiso OwnerRights SID READ \_ control en la DACL predeterminada del token. En versiones anteriores a Windows Vista de Windows, establece el propietario del token en el SID de APPID.

Se deben tener en cuenta las siguientes consideraciones de seguridad al usar la marca de **\_ \_ \_ \_ \_ \_ enlace y SD de proceso de servidor seguro APPIDREGFLAGS** :

-   La marca de **\_ \_ \_ \_ \_ \_ enlace y SD de proceso de servidor seguro APPIDREGFLAGS** está pensada para que la establezcan los servidores com que se inician en uno de los contextos de seguridad de servicio integrados; las cuentas NetworkService o LocalService. Si los servidores suplantan a los clientes con privilegios y si no se establece la marca de **\_ \_ \_ \_ \_ \_ enlace y el procesamiento de servidor seguro APPIDREGFLAGS** , el código malintencionado que se ejecuta en otros procesos con el mismo contexto de seguridad puede elevar el privilegio mediante la apropiación de los tokens de suplantación de los clientes con privilegios del proceso de servidor com.
-   Cuando se establece la marca de **\_ \_ \_ \_ \_ enlace SD and \_ BIND del proceso de servidor seguro APPIDREGFLAGS** , com protege el descriptor de seguridad del objeto de proceso en el caso de los servidores com "Activator" de runas. Para estos servidores, se espera que el cliente COM proteja el token que usa para la activación COM.
-   Cuando se establece la marca de **\_ \_ \_ \_ \_ enlace SD and \_ BIND del proceso de servidor seguro APPIDREGFLAGS** , com protege el descriptor de seguridad del objeto de proceso en el caso de los servidores com "este usuario" de runas. También dificulta el token de proceso del servidor COM, ya que el SCM de COM es la entidad que crea el token.

La marca de **\_ \_ \_ \_ \_ \_ enlace y SD de proceso de servidor seguro APPIDREGFLAGS** se admite en Windows XP, Windows server 2003, Windows Vista y Windows Server 2008 solo cuando se aplica la revisión MSRC8322 ([boletín de seguridad MS09-012](https://support.microsoft.com/kb/959454)). Se admite de forma nativa en Windows 7 y versiones posteriores de Windows.

La marca **APPIDREGFLAGS \_ Secure \_ Server \_ Process \_ SD \_ and \_ BIND** solo se aplica a los servidores com que están configurados para runas "Activator" o "este usuario". No se aplica a los servidores COM que son servicios NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ problema \_ \_ de activación RPC \_ en la descripción de la \_ identificación

Si la marca **APPIDREGFLAGS \_ Issue \_ Activation \_ RPC \_ at \_ Identify** está establecida en **AppIDFlags**, el SCM de com emitirá solicitudes de activación de objetos al proceso de servidor com mediante un nivel de suplantación de la [ \_ \_ \_ \_ identidad de nivel Imp de RPC C](impersonation-levels.md).

Si no se establece la marca **APPIDREGFLAGS \_ Issue \_ Activation \_ RPC \_ at \_ Identify** , el SCM de com emitirá solicitudes de activación de objetos a los procesos de servidor com mediante un nivel de suplantación de la [ \_ \_ \_ \_ suplantación del nivel Imp de RPC C](impersonation-levels.md).

Se deben tener en cuenta las siguientes consideraciones de seguridad al usar el **RPC de activación de APPIDREGFLAGS issue en la marca \_ \_ \_ \_ de \_ identificación** :

-   La **marca \_ \_ RPC de activación de APPIDREGFLAGS Issue \_ en la \_ \_ identificación** está pensada para que la usen los servidores com que no realizan el trabajo en nombre de los clientes en solicitudes de activación de objetos. En el caso de estos servidores, tener el problema de COM SCM solicitudes de activación de objeto en el [ \_ nivel Imp de RPC C \_ \_ \_ identifica](impersonation-levels.md) las posibilidades de que los tokens con privilegios con el nivel de [**\_ suplantación \_ de se**](/windows/desktop/SecAuthZ/privilege-constants) muestren en el proceso.

Windows 7 y versiones posteriores de Windows admiten la marca **RPC de activación de APPIDREGFLAGS issue en la \_ \_ \_ \_ \_ identificación** .

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

 

 