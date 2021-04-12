---
title: Constantes de autenticación (WSManDisp. h)
description: Especifique el método de autenticación y cómo controlar los servidores de certificados para el transporte HTTPS de solicitudes.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535158"
---
# <a name="authentication-constants"></a>Constantes de autenticación

Las constantes de autenticación son constantes en la enumeración **\_ \_ WSManSessionFlags** que especifican el método de autenticación y cómo controlar los servidores de certificados para el transporte https de las solicitudes.

Una o varias de las constantes enumeradas en la lista siguiente son necesarias en el parámetro *Flags* en las llamadas a [**WSMan. createSession**](wsman-createsession.md) o en [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) llamadas que se conectan a un equipo remoto.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Use el nombre de usuario y la contraseña como credenciales. Establezca esta marca cuando cree un objeto [**ConnectionOptions**](connectionoptions.md) y proporcione el [**nombre de usuario**](connectionoptions-username.md) y la [**contraseña**](connectionoptions-password.md). Las credenciales pueden ser una cuenta de dominio o una cuenta en el equipo local. De forma predeterminada, la cuenta debe ser miembro del grupo Administradores local en el equipo local o remoto. Sin embargo, el servicio WinRM se puede configurar para permitir a otros usuarios. Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md). Puede establecer esta marca cuando especifique las credenciales para negociar la autenticación (también conocida como [*autenticación integrada de Windows*](windows-remote-management-glossary.md)) o para la [*autenticación básica*](windows-remote-management-glossary.md).

El método de scripting asociado es [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)y el método de C++ es [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Al conectarse a través de HTTPS, el cliente no valida que el certificado de servidor está firmado por una entidad de certificación (CA) de confianza. Use este valor solo si el equipo remoto es de confianza por otros medios, por ejemplo, si el equipo remoto forma parte de una red que es físicamente segura y está aislada, o el equipo remoto aparece como un host de confianza en la configuración de WinRM.

El método de scripting asociado es [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)y el método de C++ es [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Al conectarse a través de HTTPS, el cliente no validará que el nombre común (CN) del certificado de servidor coincida con el nombre del equipo en la cadena de conexión. Use solo cuando el equipo remoto sea de confianza por otros medios, por ejemplo, si el equipo remoto forma parte de una red que es físicamente segura y aislada, o el equipo remoto aparece como un host de confianza en la configuración de WinRM.

El método de scripting asociado es [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)y el método de C++ es [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



No usar autenticación. Especifique esta constante al probar una conexión a un equipo remoto para determinar si un servicio que implementa el protocolo WS-Management está configurado para escuchar solicitudes de datos. **WSManFlagUseNoAuthentication** no se puede combinar con ninguna otra constante de [**sesión**](session.md) . El método de scripting asociado es [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)y el método de C++ es [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Usar autenticación implícita. Solo el equipo cliente puede iniciar una solicitud de autenticación Implícita. El cliente envía una solicitud al servidor para autenticar y recibe una cadena de token del servidor. Después, el cliente envía la solicitud de recurso, incluido el nombre de usuario y un hash criptográfico de la contraseña combinada con la cadena de token. La autenticación implícita es compatible con HTTP y HTTPS. Las aplicaciones y scripts de cliente de WinRM pueden especificar la autenticación implícita, pero no el servicio.

El método de scripting asociado es [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)y el método de C++ es [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Use negociar autenticación. El cliente envía una solicitud al servidor para realizar la autenticación. El servidor determina si se usa Kerberos o NTLM. Kerberos está seleccionado para autenticar una cuenta de dominio y se ha seleccionado NTLM para las cuentas de equipo local. El nombre de usuario debe especificarse con el formato dominio \\ nombreDeUsuario para un usuario de dominio o \\ nombre de usuario ServerName para un usuario local en un equipo servidor.

[Control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afecta al acceso al servicio WinRM. Cuando se usa Negotiate Authentication en un grupo de trabajo o un dominio, solo la cuenta de administrador integrada puede tener acceso al servicio. Para permitir que todas las cuentas del grupo administradores tengan acceso al servicio, establezca la siguiente clave del registro en 1: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.

El método de scripting asociado es [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)y el método de C++ es [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Use la autenticación básica. El cliente presenta las credenciales en forma de nombre de usuario y contraseña, que se transmiten directamente en el mensaje de solicitud. Solo puede especificar credenciales que identifiquen una cuenta de administrador local en el equipo remoto.

El método de scripting asociado es [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)y el método de C++ es [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Utilice la autenticación Kerberos. El cliente y el servidor se autentican mutuamente mediante vales Kerberos.

El método de scripting asociado es [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)y el método de C++ es [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



No usar cifrado. No se permite el tráfico no cifrado de forma predeterminada y debe habilitarse tanto en el cliente como en el servidor.

El método de scripting asociado es [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)y el método de C++ es [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Use la autenticación basada en certificados de cliente.

El método de scripting asociado es [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)y el método de C++ es [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Use la autenticación del proveedor de compatibilidad para seguridad de credenciales (CredSSP).

El método de scripting asociado es [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)y el método de C++ es [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



No Compruebe la revocación de certificados durante la autenticación.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Permitir credenciales implícitas.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



Usar capa de sockets seguros, habilita HTTPS.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de sesión](session-constants.md)
</dt> </dl>

 

 





