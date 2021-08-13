---
description: Permite que una aplicación de transporte consulte el paquete de seguridad del Proveedor de compatibilidad con seguridad de credenciales (CredSSP) para determinados atributos de un contexto de seguridad.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: Función QueryContextAttributes (CredSSP, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b8ff421a2173f2ce2c5521e0706b53c3f6c326038179345d139acd0a157c7d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920234"
---
# <a name="querycontextattributes-credssp-function"></a>Función QueryContextAttributes (CredSSP)

La **función QueryContextAttributes (CredSSP)** permite a una aplicación de transporte consultar el paquete [](../secgloss/a-gly.md#_security_attribute_gly) de seguridad del Proveedor de compatibilidad con seguridad de credenciales (CredSSP) para determinados atributos de un contexto de seguridad.

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

Identificador del contexto de seguridad que se va a consultar.

</dd> <dt>

*ulAttribute* \[ En\]
</dt> <dd>

Atributo del contexto que se va a devolver. Este parámetro puede ser uno de los valores siguientes. A menos que se especifique lo contrario, los atributos son aplicables tanto al cliente como al servidor.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ AtTR \_ C ACCESS TOKEN \_ \_ 0x80000012**</dt> <dt></dt> </dl>                                 | El *parámetro pBuffer* contiene un puntero a una estructura [**\_ AccessToken de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica el token de acceso para el contexto de seguridad actual.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ AtTR \_ C FULL ACCESS TOKEN \_ \_ \_ 0x80000082**</dt> <dt></dt> </dl>                 | El *parámetro pBuffer* contiene un puntero a una estructura [**\_ AccessToken de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica el token de acceso para el contexto de seguridad actual.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ESTADO DE \_ CONFIANZA \_ DEL \_ CERTIFICADO ATTR**</dt> <dt>0x80000084</dt> </dl>                        | El *parámetro pBuffer* contiene un puntero a una [**estructura CERT TRUST \_ \_ STATUS**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) que especifica información de confianza sobre el certificado.<br/> Este atributo solo se admite en el cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS**</dt> <dt>0x80000080</dt> </dl>                                                              | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ ClientCreds de SecPkgContext**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales de cliente.<br/> Las credenciales de cliente pueden ser nombre de usuario y contraseña o nombre de usuario y PIN de tarjeta inteligente.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ CREDS \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ ClientCreds de SecPkgContext**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales de cliente. <br/> Si la credencial de cliente es el nombre de usuario y la contraseña, el búfer es una estructura [**KERB \_ INTERACTIVE \_ LOGON**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) empaquetada.<br/> Si la credencial de cliente es el nombre de usuario y el PIN de tarjeta inteligente, el búfer es una estructura DE INICIO DE [**\_ \_ SESIÓN DE CERTIFICADO KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empaquetada.<br/> Si la credencial de cliente es una credencial de identidad en línea, el búfer es una estructura [**SEC \_ \_ WINNT AUTH \_ IDENTITY \_ EX2**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) serializada.<br/> Este atributo solo se admite en el servidor CredSSP.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ PAQUETE DE \_ \_ NEGOCIACIÓN DE ATTR**</dt> <dt>0x80000081</dt> </dl>                   | El *parámetro pBuffer* contiene un puntero a una estructura [**\_ PackageInfo de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) que especifica el nombre del paquete de autenticación negociado por el [proveedor Microsoft Negotiate.](microsoft-negotiate.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ ATTR \_ PACKAGE \_ INFO**</dt> <dt>10</dt> </dl>                                                | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ PackageInfo de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa)<br/> Devuelve información sobre el SSP en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ MARCAS DE \_ \_ AUTENTICACIÓN DE ATTR \_ SERVER**</dt> <dt>0x80000083</dt> </dl>                        | El *parámetro pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ Flags**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) que especifica información sobre las marcas en el contexto de seguridad actual.<br/> Este atributo solo se admite en el cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ TAMAÑOS \_ DE ATTR**</dt> <dt>0x0</dt> </dl>                                                                     | El *parámetro pBuffer* contiene un puntero a una [**estructura SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)<br/> Consulta los tamaños de las estructuras usadas en las funciones por mensaje y los intercambios de autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ ATRIBUTOS DE \_ SEGURIDAD \_ DEL SUJETO \_ DE ATTR**</dt> <dt>124</dt> </dl> | El *parámetro pBuffer* contiene un puntero a una [**estructura \_ SubjectAttributes de SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes)<br/> Este valor devuelve información sobre los atributos de seguridad de la conexión.<br/> Este valor solo se admite en el servidor CredSSP.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe los atributos. El tipo de estructura depende del valor del *parámetro ulAttribute.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve SEC \_ E \_ OK.

Si se produce un error en la función, puede devolver los siguientes códigos de error.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ Identificador \_ no**</dt> válido <dt>0x80100003</dt> </dl>       | Error en la función. El *parámetro phContext* especifica un identificador para un contexto incompleto.<br/> |
| <dl> <dt>**SEC \_ E \_ UNSUPPORTED \_ FUNCTION**</dt> <dt>0x80090302</dt> </dl> | Error en la función. El valor del *parámetro ulAttribute* no es válido.<br/>                 |



 

## <a name="remarks"></a>Observaciones

La estructura a la que apunta el *parámetro pBuffer* varía en función del atributo que se está consultando.

Aunque el autor de la llamada debe asignar la propia estructura *pBuffer,* el SSP asigna la memoria necesaria para contener miembros de tamaño variable de la *estructura pBuffer.* La memoria asignada por el SSP debe liberarse llamando a la [**función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **QueryContextAttributesW** (Unicode) y **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**CONTEXTO \_ DE CERTIFICADO**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Tamaños de \_ SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
