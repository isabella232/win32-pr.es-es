---
description: Permite que una aplicación de transporte consulte el [*paquete de seguridad*](../secgloss/s-gly.md) de síntesis para determinados atributos de un [*contexto de seguridad*](../secgloss/s-gly.md).
ms.assetid: d4cd2cc4-77a2-42ba-9029-f4d92706c5c2
title: Función QueryContextAttributes (Digest, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1e26e81d190f031479633fe96fbc49496b661302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541158"
---
# <a name="querycontextattributes-digest-function"></a>QueryContextAttributes (síntesis) (función)

La función **QueryContextAttributes (síntesis)** permite que una aplicación de transporte consulte el [*paquete de seguridad*](../secgloss/s-gly.md) de síntesis para determinados [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) de un [*contexto de seguridad*](../secgloss/s-gly.md).

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

*phContext* \[ de\]
</dt> <dd>

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a consultar.

</dd> <dt>

*ulAttribute* \[ de\]
</dt> <dd>

Especifica el atributo del contexto que se va a devolver. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ \_ \_ Token de acceso de ATTR**</dt> <dt>18</dt> </dl>                                   | El parámetro *pBuffer* contiene un puntero a una [**estructura \_ AccessToken de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) .<br/> Devuelve un identificador para el token de acceso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ ATTR ( \_ entidad**</dt> ) <dt>6</dt> </dl>                                              | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ autoridad SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya) .<br/> Consulta el nombre de la entidad de autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ \_ \_ \_ Destino especificado del cliente ATTR**</dt> <dt>27</dt> </dl> | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ ClientSpecifiedTarget**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) que representa el nombre de la entidad de seguridad de servicio (SPN) del destino inicial proporcionado por el cliente. <br/> Este valor solo se admite cuando se usan enlaces de canal.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ credenciales \_ 2**</dt> <dt>0x80000086</dt> </dl>                                          | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales del cliente. <br/> Si la credencial del cliente es el nombre de usuario y la contraseña, el búfer es una estructura de [**\_ Inicio de \_ sesión interactiva Kerb**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) empaquetada.<br/> Si la credencial del cliente es el nombre de usuario y el PIN de la tarjeta inteligente, el búfer es una estructura de [**\_ Inicio de \_ sesión de certificado Kerb**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empaquetada.<br/> Si la credencial del cliente es una credencial de identidad en línea, el búfer es una estructura de [**EX2 de identidad de \_ autenticación de WinNT \_ \_ \_ de seg**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) .<br/> Este atributo solo se admite en el servidor CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ DCE \_ info**</dt> <dt>3</dt> </dl>                                                | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo) .<br/> Consulta los datos de autorización utilizados por los servicios de DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ \_Marcas de atributos**</dt> <dt>14</dt> </dl>                                                         | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ marcas SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) .<br/> Devuelve información sobre las marcas de contexto negociadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ \_ \_ Información de clave de ATTR**</dt> <dt>5</dt> </dl>                                                | El parámetro *pBuffer* contiene un puntero a una [**estructura \_ KeyInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa) .<br/> Consulta información acerca de las claves utilizadas en un [*contexto de seguridad*](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ \_Duración del atributo**</dt> <dt>2</dt> </dl>                                                 | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ duración SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan) .<br/> Consulta el intervalo de vida del contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**\_ \_ credenciales locales de SECPKG ATTR \_**</dt> </dl>                                                                                                 | El parámetro *pBuffer* contiene un puntero a una estructura **SecPkgContext \_ LocalCredentialInfo** . (obsoleto)<br/> Se ha sustituido por el \_ contexto de certificado local de SECPKG ATTR \_ \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ \_Nombres de atributos**</dt> <dt>1</dt> </dl>                                                          | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ nombres SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa) .<br/> Consulta el nombre asociado al contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ \_ \_ Nombres nativos de ATTR**</dt> <dt>13</dt> </dl>                                   | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ NativeNames**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa) .<br/> Devuelve el nombre principal (CNAME) del vale de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ \_ \_ Información de negociación de ATTR**</dt> <dt>12</dt> </dl>                       | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ NegotiationInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa) .<br/> Devuelve información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) que se va a utilizar con el proceso de negociación y el estado actual de la negociación para el uso de ese paquete.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Información del paquete ATTR**</dt> <dt>10</dt> </dl>                                   | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .<br/> Devuelve información sobre el SSP en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ \_ \_ Expiración**</dt> de la contraseña de ATTR <dt>8</dt> </dl>                           | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ PasswordExpiry**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry) .<br/> Devuelve la información de expiración de la contraseña.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ 0x55 \_ del \_ almacén raíz de ATTR**</dt> <dt></dt> </dl>                                       | El parámetro *pBuffer* contiene un puntero a un **HCERTCONTEXT**. Busca un contexto de certificado que contenga un certificado proporcionado por el almacén raíz.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ \_ \_ Clave de sesión de ATTR**</dt> <dt>9</dt> </dl>                                       | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ SessionKey**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey) .<br/> Devuelve información sobre la [*clave de sesión*](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_Tamaños de ATTR**</dt> <dt>0</dt> </dl>                                                          | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Consulta los tamaños de las estructuras utilizadas en las funciones por mensaje.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_STREAM_SIZES"></span><span id="secpkg_attr_stream_sizes"></span><dl> <dt>**SECPKG \_ \_ \_ Tamaños de flujo de atributos**</dt> <dt>4</dt> </dl>                                    | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) .<br/> Consulta los tamaños de las distintas partes de una secuencia utilizada en las funciones por mensaje.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ \_ \_ Información de destino de ATTR**</dt> <dt>17</dt> </dl>                 | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ TargetInformation**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation) .<br/> Devuelve información sobre el nombre del servidor remoto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe los atributos. El tipo de estructura señalado depende del valor especificado en el parámetro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es SEC \_ E \_ OK.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero.

## <a name="remarks"></a>Observaciones

La estructura a la que apunta el parámetro *pBuffer* varía en función del atributo que se consulta. El autor de la llamada debe asignar la propia estructura *pBuffer* , pero el SSP asigna la memoria necesaria para almacenar los miembros de tamaño variable de la estructura *pBuffer* . La memoria asignada por el SSP se puede liberar llamando a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Una vez que se ha leído el valor de contexto de certificado \_ remoto SECPKG ATTR \_ o de \_ \_ SECPKG \_ ATTR \_ \_ \_ , el miembro **hCertStore** se establecerá en un identificador de un almacén de certificados que contenga los certificados intermedios, si los hay. Además, la aplicación es responsable de llamar a [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar la memoria que usa el contexto de certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **QueryContextAttributesW** (Unicode) y **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**contexto de certificado \_**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**\_Autoridad SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**\_KeyInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**Duración de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Nombres de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Tamaños de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
