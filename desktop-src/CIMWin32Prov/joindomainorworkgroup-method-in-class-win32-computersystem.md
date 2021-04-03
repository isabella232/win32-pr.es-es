---
description: Une un equipo a un dominio o grupo de trabajo.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Método JoinDomainOrWorkgroup de la clase Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907429"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método JoinDomainOrWorkgroup de la clase de Win32 \_ ComputerSystem

El método **JoinDomainOrWorkgroup** une un equipo a un dominio o grupo de trabajo.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Especifica el dominio o grupo de trabajo al que se va a unir. No puede ser **null**.

</dd> <dt>

*Contraseña* \[ de de\]
</dt> <dd>

Si el parámetro *username* especifica un nombre de cuenta, el parámetro *password* debe apuntar a la contraseña que se va a usar al conectarse al controlador de dominio. De lo contrario, este parámetro debe ser **null**.

</dd> <dt>

*Nombre de usuario* \[ de\]
</dt> <dd>

Puntero a una cadena de caracteres terminada en **null** que especifica el nombre de la cuenta que se va a usar al conectarse al controlador de dominio. Debe especificar un nombre NetBIOS de dominio y una cuenta de usuario, por ejemplo, usuario de dominio \\ . Si este parámetro es **null**, se utiliza la información del llamador.

También puede usar el nombre principal de usuario (UPPED) en el formulario user@domain .

</dd> <dt>

*AccountOU* \[ de\]
</dt> <dd>

Especifica el puntero a una cadena de caracteres terminada en **null** que contiene el nombre de formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) de la unidad organizativa (OU) de la cuenta de equipo. Si especifica este parámetro, la cadena debe contener una ruta de acceso completa; de lo contrario, *acento* debe ser **null**.

Ejemplo: "OU = testOU; DC = dominio; DC = dominio; DC = com "

</dd> <dt>

*FJoinOptions* \[ de\]
</dt> <dd>

Conjunto de marcadores de bits que definen las opciones de combinación.

<dt>



  (0)


</dt> <dd>

Predeterminada. No hay opciones de combinación.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_ UNIRSE a \_ dominio** (0x00000001)


</dt> <dd>

Une el equipo a un dominio. Si no se especifica este valor, une el equipo a un grupo de trabajo.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_ \_Creación de cuentas** (0x00000002)


</dt> <dd>

Crea la cuenta en el dominio.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ \_Actualización de Win9x** (0x00000010)


</dt> <dd>

La operación de Unión se está produciendo como parte de una actualización.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_ Unión al dominio \_ \_ si está \_ Unido** (0x00000020)


</dt> <dd>

Permite una combinación con un nuevo dominio, incluso si el equipo ya está unido a un dominio.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_ Unión no \_ segura** (0x00000040)


</dt> <dd>

realiza una unión no segura.

Esta opción solicita una Unión de dominio a una cuenta creada previamente sin autenticarse con las credenciales de usuario de dominio. Esta opción se puede usar junto con la opción de la **\_ máquina pwd de NETSETUP \_ \_ pasada** . En este caso, *password* es la contraseña de la cuenta de equipo creada previamente.

Antes de Windows Vista con SP1 y Windows Server 2008, una Unión no segura no se autenticaba en el controlador de dominio. Toda la comunicación se realizó mediante una sesión nula (sin autenticar). A partir de Windows Vista con SP1 y Windows Server 2008, se usan el nombre y la contraseña de la cuenta de equipo para autenticarse en el controlador de dominio.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_ \_ \_ Se pasó la pwd del equipo** (0x00000080)


</dt> <dd>

Indica que el parámetro de *contraseña* especifica una contraseña de cuenta de equipo local en lugar de una contraseña de usuario. Esta marca solo es válida para las combinaciones no seguras, que debe indicar estableciendo también la \_ \_ marca NETSETUP unsecure.

Si establece esta marca, después de que la operación de Unión se realice correctamente, la contraseña del equipo se establecerá en el valor de *contraseña*, si ese valor es una contraseña de equipo válida.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_ APLAZAr el \_ \_ conjunto de SPN** (0x00000100)


</dt> <dd>

Indica que el nombre de entidad de seguridad de servicio (SPN) y las propiedades de DnsHostName en el objeto de equipo no deben actualizarse en este momento.

Normalmente, estas propiedades se actualizan durante la operación de combinación. En su lugar, estas propiedades se deben actualizar durante una llamada subsiguiente al método [**Rename**](rename-method-in-class-win32-computersystem.md) . Estas propiedades siempre se actualizan durante la operación de cambio de nombre.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_ Unirse a una \_ \_ cuenta de controlador de dominio** (0x00000200)


</dt> <dd>

Permitir la Unión al dominio si la cuenta existente es un controlador de dominio.

> [!Note]  
> Esta marca es compatible con Windows Vista y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_ \_DC ambiguo** (0x00001000)


</dt> <dd>

Al unirse al dominio, no intente establecer el controlador de dominio preferido en el registro.

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_ NO \_ hay \_ caché de Netlogon** (0x00002000)


</dt> <dd>

Al unirse al dominio, no cree la memoria caché de netlogon.

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_ No \_ controlar \_ servicios** (0x00004000)


</dt> <dd>

Al unirse al dominio, no fuerce el inicio del servicio NetLogon.

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_ ESTABLECER \_ \_ el nombre** de la máquina (0x00008000)


</dt> <dd>

Al unirse al dominio solo para la combinación sin conexión, establezca el nombre de host y el nombre de NetBIOS del equipo de destino.

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_ FORZAr el \_ \_ conjunto de SPN** (0x00010000)


</dt> <dd>

Al unirse al dominio, invalide otras opciones durante la Unión al dominio y establezca el nombre de la entidad de seguridad de servicio (SPN).

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_ NO \_ \_ reutilización de cuentas** (0x00020000)


</dt> <dd>

Al unirse al dominio, no vuelva a usar una cuenta existente.

> [!Note]  
> Esta marca es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_ OMITIr \_ \_ marcas no admitidas** (0x10000000)


</dt> <dd>

Si se establece este bit, se omitirán las marcas no reconocidas por la función **JoinDomainOrWorkgroup** y [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comportará como si no se hubieran establecido las marcas.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [código de error del sistema](/windows/desktop/Debug/system-error-codes), que puede incluir uno de los siguientes valores numéricos. Cualquier otro número indica que hubo un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

Acceso denegado.

</dd> <dt>

**87**
</dt> <dd>

El parámetro no es correcto.

</dd> <dt>

**110**
</dt> <dd>

el sistema no puede abrir el objeto especificado.

</dd> <dt>

**1323**
</dt> <dd>

No se puede actualizar la contraseña.

</dd> <dt>

**1326**
</dt> <dd>

Error de inicio de sesión: nombre de usuario desconocido o contraseña incorrecta.

</dd> <dt>

**1355**
</dt> <dd>

El dominio especificado no existe o no se pudo establecer contacto con él.

</dd> <dt>

**2224**
</dt> <dd>

La cuenta ya existe.

</dd> <dt>

**2691**
</dt> <dd>

El equipo ya está unido al dominio.

</dd> <dt>

**2692**
</dt> <dd>

El equipo no está unido actualmente a un dominio.

</dd> <dt>

**se \_ \_ requiere la \_ conexión cifrada WBEM E \_**
</dt> <dd>

0x80041087

Se especifican la *contraseña* y el *nombre de usuario* , pero el nivel de autenticación no es **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C. Por Visual Basic, se devuelve **wbemErrEncryptedConnectionRequired** .

</dd> <dt>

**Otros**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al mover un equipo de un dominio a un grupo de trabajo, debe quitar el equipo del dominio (con una llamada a [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) antes de llamar a este método para unirse a un grupo de trabajo (con una llamada a **JoinDomainOrWorkgroup**). Después de llamar a este método, reinicie el equipo afectado para aplicar los cambios.

El *nombre de usuario* y la *contraseña* pueden dejarse en **blanco.** Sin embargo, la autenticación de la conexión a WMI debe ser 6 en el script o **WbemAuthenticationLevelPktPrivacy** en Visual Basic y otros idiomas que pueden usar la biblioteca de [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) . Para obtener más información, vea [establecer el nivel de seguridad de proceso predeterminado con VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

En C++, establezca la autenticación de **nivel de autenticación RPC \_ C de \_ \_ nivel \_ \_** de autenticación en [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), para todo el proceso o en [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), para una conexión al proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Para obtener más información, vea [establecer la autenticación con C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) y [establecer la seguridad en IWbemServices y en otros servidores proxy](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Ejemplos

El ejemplo [unir un equipo a un dominio](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) de PowerShell une un equipo a un dominio.

El siguiente ejemplo de código de VBScript une un equipo a un dominio y crea la cuenta del equipo en Active Directory.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ComputerSystem de Win32 \_**](win32-computersystem.md)
</dt> <dt>

[**Método UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

