---
description: Permite que una aplicación de transporte consulte el paquete de [*seguridad*](../secgloss/s-gly.md) NTLM para determinados atributos de un contexto [de seguridad](../secgloss/s-gly.md).
ms.assetid: cfa545e7-c5d9-4ffd-bbba-669d2bd3df2d
title: Función QueryContextAttributes (NTLM, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: dba11bbfb1666a3f47b7ee2820167259319178ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568224"
---
# <a name="querycontextattributes-ntlm-function"></a>Función QueryContextAttributes (NTLM)

La **función QueryContextAttributes (NTLM)** permite a una aplicación de transporte consultar el paquete de seguridad [*NTLM*](../secgloss/s-gly.md) para determinados [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) de un contexto [de seguridad](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phContext* \[ En\]
</dt> <dd>

Identificador del contexto [de seguridad que](../secgloss/s-gly.md) se va a consultar.

</dd> <dt>

*ulAttribute* \[ En\]
</dt> <dd>

Especifica el atributo del contexto que se va a devolver. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ ATTR \_ ACCESS \_ TOKEN**</dt> <dt>18</dt> </dl>                                       | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ AccessToken de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken)<br/> Devuelve un identificador al token de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ ATTR \_ AUTHORITY**</dt> <dt>6</dt> </dl>                                                  | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ Authority.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)<br/> Consulta el nombre de la entidad de autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ DESTINO \_ 27 \_ ESPECIFICADO POR EL \_**</dt> CLIENTE <dt>ATTR</dt> </dl>     | El *parámetro pBuffer* contiene un puntero a una estructura [**\_ ClientSpecifiedTarget de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) que representa el nombre de entidad de seguridad de servicio (SPN) del destino inicial proporcionado por el cliente. <br/> Este valor solo se admite cuando se usan enlaces de canal.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                              | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ ClientCreds de SecPkgContext**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales de cliente. <br/> Si la credencial de cliente es el nombre de usuario y la contraseña, el búfer es una estructura [**KERB \_ INTERACTIVE \_ LOGON**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) empaquetada.<br/> Si la credencial de cliente es el nombre de usuario y el PIN de tarjeta inteligente, el búfer es una estructura DE INICIO DE [**\_ \_ SESIÓN DE CERTIFICADO KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empaquetada.<br/> Si la credencial de cliente es una credencial de identidad en línea, el búfer es una estructura [**SEC \_ \_ WINNT AUTH \_ IDENTITY \_ EX2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) serializada.<br/> Este atributo solo se admite en el servidor CredSSP.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ DCE \_ INFO**</dt> <dt>3</dt> </dl>                                                    | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ DceInfo.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)<br/> Consultas para los datos de autorización utilizados por los servicios DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ MARCAS \_ DE ATTR**</dt> <dt>14</dt> </dl>                                                             | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ Flags.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags)<br/> Devuelve información sobre las marcas de contexto negociadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ ATTR \_ KEY \_ INFO**</dt> <dt>5</dt> </dl>                                                    | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ KeyInfo.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)<br/> Consulta información sobre las claves usadas en un contexto [de seguridad](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LAST_CLIENT_TOKEN_STATUS"></span><span id="secpkg_attr_last_client_token_status"></span><dl> <dt>**SECPKG \_ ATTR \_ LAST CLIENT TOKEN \_ \_ \_ STATUS**</dt> <dt>30</dt> </dl> | El *parámetro pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ LastClientTokenStatus**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lastclienttokenstatus) que especifica si el token de la llamada más reciente a la función [**InitializeSecurityContext**](initializesecuritycontext--general.md) es el último token del cliente.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ ATTR \_ LIFESPAN**</dt> <dt>2</dt> </dl>                                                     | El *parámetro pBuffer* contiene un puntero a una [**estructura De vida de \_ SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)<br/> Consulta el intervalo de vida del contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ ATTR \_ LOCAL \_ CRED**</dt> </dl>                                                                                                     | El *parámetro pBuffer* contiene un puntero a una estructura **SecPkgContext \_ LocalCredentialInfo.** (obsoleto)<br/> Reemplazado por SECPKG \_ ATTR \_ LOCAL CERT \_ \_ CONTEXT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ NOMBRES \_ DE ATTR**</dt> <dt>1</dt> </dl>                                                              | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ Names.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)<br/> Consulta el nombre asociado al contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ NOMBRES \_ NATIVOS \_ DE ATTR**</dt> <dt>13</dt> </dl>                                       | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ NativeNames.**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa)<br/> Devuelve el nombre principal (CNAME) del vale de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ INFORMACIÓN DE \_ NEGOCIACIÓN \_ DE ATTR**</dt> <dt>12</dt> </dl>                           | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ NegotiationInfo de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa)<br/> Devuelve información sobre el [*paquete de seguridad que*](../secgloss/s-gly.md) se va a usar con el proceso de negociación y el estado actual de la negociación para el uso de ese paquete.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ ATTR \_ PACKAGE \_ INFO**</dt> <dt>10</dt> </dl>                                       | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ PackageInfo de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Devuelve información sobre el SSP en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ EXPIRACIÓN \_ DE LA CONTRASEÑA \_ DE ATTR**</dt> <dt>8</dt> </dl>                               | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ PasswordExpiry de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry)<br/> Devuelve la información de expiración de la contraseña.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ AtTR \_ ROOT \_ STORE**</dt> <dt>0x55</dt> </dl>                                           | El *parámetro pBuffer* contiene un puntero a **HCERTCONTEXT.** <br/> Busca un contexto de certificado que contiene un certificado proporcionado por el almacén raíz.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ ATTR \_ SESSION \_ KEY**</dt> <dt>9</dt> </dl>                                           | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ SessionKey de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey)<br/> Devuelve información sobre las claves [*de*](../secgloss/s-gly.md)sesión.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ TAMAÑOS \_ DE ATTR**</dt> <dt>0</dt> </dl>                                                              | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Consulta los tamaños de las estructuras usadas en las funciones por mensaje.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ ATTR \_ TARGET \_ INFORMATION**</dt> <dt>17</dt> </dl>                     | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ TargetInformation.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation)<br/> Devuelve información sobre el nombre del servidor remoto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe los atributos. El tipo de estructura a la que se apunta depende del valor especificado en el *parámetro ulAttribute.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es SEC \_ E \_ OK.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero.

## <a name="remarks"></a>Observaciones

La estructura a la que apunta el *parámetro pBuffer* varía en función del atributo que se está consultando. El autor de la llamada debe asignar la propia estructura *pBuffer,* pero el SSP asigna la memoria necesaria para contener miembros de tamaño variable de la *estructura pBuffer.* La memoria asignada por el SSP se puede liberar llamando a la [**función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Una vez leído el valor SECPKG ATTR REMOTE CERT CONTEXT o \_ \_ \_ \_ SECPKG \_ ATTR LOCAL CERT CONTEXT, el miembro \_ \_ \_ **hCertStore** se establecerá en un identificador para un almacén de certificados que contenga los certificados intermedios, si los hubiera. Además, la aplicación es responsable de llamar a [**CertFreeCertificateContext para**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) liberar la memoria usada por el contexto del certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **QueryContextAttributesW** (Unicode) y **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**CONTEXTO \_ DE CERTIFICADO**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgContext \_ Authority**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**SecPkgContext \_ KeyInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**Duración de \_ SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Nombres de \_ SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Tamaños de \_ SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
