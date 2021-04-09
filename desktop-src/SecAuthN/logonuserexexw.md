---
description: La función LogonUserExExW intenta iniciar una sesión de usuario en el equipo local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Función LogonUserExExW (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083155"
---
# <a name="logonuserexexw-function"></a>LogonUserExExW función)

La función **LogonUserExExW** intenta iniciar una sesión de usuario en el equipo local. El equipo local es el equipo desde el que se llamó a **LogonUserExExW** . No se puede usar **LogonUserExExW** para iniciar sesión en un equipo remoto. Especifique el usuario mediante un nombre de usuario y un dominio y [*autentique*](../secgloss/a-gly.md) al usuario mediante una contraseña de texto sin formato. Si la función se ejecuta correctamente, recibe un identificador de un token que representa al usuario que ha iniciado sesión. Después, puede usar este identificador de token para suplantar al usuario especificado o, en la mayoría de los casos, crear un [*proceso*](../secgloss/p-gly.md) que se ejecute en el contexto del usuario especificado.

Esta función es similar a la función [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , salvo que toma el parámetro adicional, *pTokenGroups*, que es un conjunto de uno o varios [*identificadores de seguridad*](../secgloss/s-gly.md) (SID) que se agregan al token que se devuelve al autor de la llamada cuando el inicio de sesión se realiza correctamente.

Esta función no se declara en un encabezado público y no tiene asociada ninguna biblioteca de importación. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Advapi32.dll.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszUsername* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del usuario. Es el nombre de la cuenta de usuario en la que se va a iniciar sesión. Si usa el formato de [*nombre principal de usuario*](../secgloss/u-gly.md) (UPN), el parámetro *LpszDomain* debe ser **null**.

</dd> <dt>

*lpszDomain* \[ en, opcional\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del dominio o servidor cuya base de datos de cuenta contiene la cuenta *lpszUsername* . Si este parámetro es **null**, el nombre de usuario debe especificarse en formato UPN. Si este parámetro es ".", la función valida la cuenta usando solo la base de datos de la cuenta local.

</dd> <dt>

*lpszPassword* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica la contraseña de texto no cifrado para la cuenta de usuario especificada por *lpszUsername*. Cuando haya terminado de usar la contraseña, borre la contraseña de la memoria mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Para obtener más información sobre cómo proteger las contraseñas, consulte [Administrar contraseñas](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ de\]
</dt> <dd>

Tipo de operación de inicio de sesión que se va a realizar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ Inicio de sesión \_ interactivo**</dt> <dt>2</dt> </dl>                    | Este tipo de inicio de sesión está destinado a usuarios que van a usar el equipo de forma interactiva, como un usuario que inicia sesión en un servidor de [*terminal*](../secgloss/t-gly.md) Server, un shell remoto o un proceso similar. Este tipo de inicio de sesión tiene el gasto adicional de almacenar en caché la información de inicio de sesión para las operaciones desconectadas. por lo tanto, no es apropiado para algunas aplicaciones cliente/servidor, como un servidor de correo.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ \_Red de inicio de sesión**</dt> <dt>3</dt> </dl>                                | Este tipo de inicio de sesión está diseñado para servidores de alto rendimiento para autenticar contraseñas de texto no cifrado. La función **LogonUserExExW** no almacena en caché las credenciales para este tipo de inicio de sesión.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ \_Lote de inicio de sesión**</dt> <dt>4</dt> </dl>                                      | Este tipo de inicio de sesión está pensado para los servidores de batch, donde los procesos se pueden ejecutar en nombre de un usuario sin su intervención directa. Este tipo también es para servidores de mayor rendimiento que procesan muchos intentos de autenticación de texto simple a la vez, como servidores web o de correo. La función **LogonUserExExW** no almacena en caché las credenciales para este tipo de inicio de sesión.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ \_Servicio de inicio de sesión**</dt> <dt>5</dt> </dl>                                | Indica un inicio de sesión de tipo de servicio. La cuenta proporcionada debe tener habilitado el privilegio de servicio.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ \_Desbloqueo de inicio de sesión**</dt> <dt>7</dt> </dl>                                   | Este tipo de inicio de sesión es para los archivos dll de [*Gina*](../secgloss/g-gly.md) que inician sesión en los usuarios que van a usar el equipo de forma interactiva. Este tipo de inicio de sesión puede generar un registro de auditoría único que muestra Cuándo se desbloqueó la estación de trabajo.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ Red de inicio de sesión \_ \_ ClearText**</dt> <dt>8</dt> </dl> | Este tipo de inicio de sesión conserva el nombre y la contraseña en el [*paquete de autenticación*](../secgloss/a-gly.md), lo que permite que el servidor realice conexiones a otros servidores de red durante la suplantación del cliente. Un servidor puede aceptar credenciales de texto simple de un cliente, llamar a **LogonUserExExW**, comprobar que el usuario puede tener acceso al sistema a través de la red y seguir comunicándose con otros servidores. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ \_ \_ Credenciales nuevas de inicio de sesión**</dt> <dt>9</dt> </dl>       | Este tipo de inicio de sesión permite que el autor de la llamada Clone su token actual y especifique nuevas credenciales para las conexiones salientes. La nueva sesión de inicio de sesión tiene el mismo identificador local, pero usa credenciales diferentes para otras conexiones de red.<br/> Este tipo de inicio de sesión solo es compatible con el proveedor de inicio de sesión **\_ \_ WINNT50 del proveedor LOGON32** .<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ de\]
</dt> <dd>

Proveedor de inicio de sesión. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**\_Valor predeterminado del proveedor LOGON32 \_**</dt> </dl> | Use el proveedor de inicio de sesión estándar para el sistema. El [*proveedor de seguridad*](../secgloss/s-gly.md) predeterminado es NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**Proveedor de LOGON32 \_ \_ WINNT50**</dt> </dl> | Use el proveedor de inicio de sesión Negotiate. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**Proveedor de LOGON32 \_ \_ WINNT40**</dt> </dl> | Use el proveedor de inicio de sesión de NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ en, opcional\]
</dt> <dd>

Un puntero a una estructura de [**\_ grupos de tokens**](/windows/win32/api/winnt/ns-winnt-token_groups) que especifica una lista de SID de grupo que se agregan al token que esta función recibe cuando el inicio de sesión se realiza correctamente. Cualquier SID agregado al token también afecta a la expansión de grupos. Por ejemplo, si los SID agregados son miembros de grupos locales, esos grupos también se agregan al token de acceso recibido.

Si este parámetro no es **null**, el autor de la llamada de esta función debe tener concedidos y habilitados los privilegios de **\_ \_ privilegio** de la TCB.

</dd> <dt>

*phToken* \[ out, opcional\]
</dt> <dd>

Un puntero a una variable de identificador que recibe un identificador a un token que representa el usuario especificado.

Puede usar el identificador devuelto en las llamadas a la función [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

En la mayoría de los casos, el identificador devuelto es un [*token primario*](../secgloss/p-gly.md) que puede usar en las llamadas a la función [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Sin embargo, si especifica la marca de red de inicio de sesión de LOGON32 \_ \_ , **LogonUserExExW** devuelve un [*token de suplantación*](../secgloss/i-gly.md) que no se puede usar en **CreateProcessAsUser** a menos que llame a [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token de suplantación en un token primario.

Cuando ya no necesite este identificador, ciérrelo llamando a la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

</dd> <dt>

*ppLogonSid* \[ out, opcional\]
</dt> <dd>

Un puntero a un puntero a un SID que recibe el SID del usuario que inició sesión.

Cuando haya terminado de usar el SID, liberelo llamando a la función [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .

</dd> <dt>

*ppProfileBuffer* \[ out, opcional\]
</dt> <dd>

Un puntero a un puntero que recibe la dirección de un búfer que contiene el perfil del usuario que ha iniciado sesión.

</dd> <dt>

*pdwProfileLength* \[ out, opcional\]
</dt> <dd>

Un puntero a un **valor DWORD** que recibe la longitud del búfer de perfil.

</dd> <dt>

*pQuotaLimits* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura [**de \_ límites de cuota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) que recibe información acerca de las cuotas del usuario que ha iniciado sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve un valor distinto de cero.

Si se produce un error en la función, devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

El tipo de inicio de sesión de **\_ \_ red de LOGON32 Logon** es más rápido, pero tiene las siguientes limitaciones:

-   La función devuelve un [*token de suplantación*](../secgloss/i-gly.md), no un token primario. Este token no se puede usar directamente en la función [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Sin embargo, puede llamar a la función [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para convertir el token en un token primario y, a continuación, usarlo en **CreateProcessAsUser**.
-   Si convierte el token en un token principal y lo usa en [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar un proceso, el nuevo proceso no puede tener acceso a otros recursos de red, como servidores o impresoras remotos, a través del redirector. Una excepción es que si no se controla el acceso al recurso de red, el nuevo proceso podrá tener acceso a él.

La cuenta especificada por *lpszUsername* debe tener los derechos de cuenta necesarios. Por ejemplo, para iniciar la sesión de un usuario con el indicador **\_ \_ interactivo de inicio de sesión de LOGON32** , el usuario (o un grupo al que pertenezca el usuario) debe tener el derecho de cuenta de **\_ \_ \_ nombre de inicio de sesión** de es interactivo. Para obtener una lista de los derechos de cuenta que afectan a las distintas operaciones de inicio de sesión, consulte [derechos de acceso a objetos de cuenta](../secmgmt/account-object-access-rights.md).

Se considera que un usuario ha iniciado sesión si existe al menos un token. Si llama a [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) y, a continuación, cierra el token, el usuario seguirá iniciando sesión hasta que finalice el proceso (y todos los procesos secundarios).

Si se proporciona el parámetro opcional *pTokenGroups* , LSA no agregará el SID local ni el SID de inicio de sesión automáticamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                  |
| Versión<br/>                  | LogonUserExExW también está disponible en Windows Server 2003 o Windows XPwith la versión de distribución general.<br/> |
| Encabezado<br/>                   | <dl> <dt>Winbasep. h</dt> </dl>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Access Control cliente/servidor](../secauthz/client-server-access-control.md)
</dt> <dt>

[Funciones de Access Control cliente/servidor](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**límites de cuota \_**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
