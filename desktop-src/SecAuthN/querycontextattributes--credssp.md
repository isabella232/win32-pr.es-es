---
description: Permite que una aplicación de transporte consulte el paquete de seguridad del proveedor de compatibilidad para seguridad de credenciales (CredSSP) para determinados atributos de un contexto de seguridad.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: Función QueryContextAttributes (CredSSP, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 191c3c8d3b2b5bd829aaf8eb45bacadbbd2bbade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720576"
---
# <a name="querycontextattributes-credssp-function"></a>QueryContextAttributes (CredSSP) (función)

La función **QueryContextAttributes (CredSSP)** permite que una aplicación de transporte consulte el paquete de seguridad del proveedor de compatibilidad para seguridad de credenciales (CredSSP) para determinados [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) de un contexto de seguridad.

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

Identificador del contexto de seguridad que se va a consultar.

</dd> <dt>

*ulAttribute* \[ de\]
</dt> <dd>

Atributo del contexto que se va a devolver. Este parámetro puede ser uno de los valores siguientes. A menos que se especifique lo contrario, los atributos son aplicables tanto al cliente como al servidor.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ Atributo \_ de \_ acceso \_ de ATTR C**</dt> <dt>0x80000012</dt> </dl>                                 | El parámetro *pBuffer* contiene un puntero a una [**estructura \_ AccessToken de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica el token de acceso para el contexto de seguridad actual.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ Atributo \_ de \_ \_ acceso completo \_ de ATTR C**</dt> <dt>0x80000082</dt> </dl>                 | El parámetro *pBuffer* contiene un puntero a una [**estructura \_ AccessToken de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica el token de acceso para el contexto de seguridad actual.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ ATRIBUTO \_ de \_ \_ Estado de confianza CERT**</dt> <dt>0x80000084</dt> </dl>                        | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ \_ Estado de confianza de CERT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) que especifica la información de confianza del certificado.<br/> Este atributo solo se admite en el cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ \_Credenciales de ATTR**</dt> <dt>0x80000080</dt> </dl>                                                              | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales del cliente.<br/> Las credenciales del cliente pueden ser el nombre de usuario, la contraseña, el nombre de usuario y el PIN de la tarjeta inteligente.<br/> Este atributo solo se admite en el servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ credenciales \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica las credenciales del cliente. <br/> Si la credencial del cliente es el nombre de usuario y la contraseña, el búfer es una estructura de [**\_ Inicio de \_ sesión interactiva Kerb**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) empaquetada.<br/> Si la credencial del cliente es el nombre de usuario y el PIN de la tarjeta inteligente, el búfer es una estructura de [**\_ Inicio de \_ sesión de certificado Kerb**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empaquetada.<br/> Si la credencial del cliente es una credencial de identidad en línea, el búfer es una estructura de [**EX2 de identidad de \_ autenticación de WinNT \_ \_ \_ de seg**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) .<br/> Este atributo solo se admite en el servidor CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ \_ \_ Paquete de negociación de ATTR**</dt> <dt>0x80000081</dt> </dl>                   | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) que especifica el nombre del paquete de autenticación negociado por el proveedor [Microsoft Negotiate](microsoft-negotiate.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Información del paquete ATTR**</dt> <dt>10</dt> </dl>                                                | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa).<br/> Devuelve información sobre el SSP en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ \_Marcadores de \_ autenticación \_ del servidor ATTR**</dt> <dt>0x80000083</dt> </dl>                        | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ marcas SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) que especifica información sobre las marcas en el contexto de seguridad actual.<br/> Este atributo solo se admite en el cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ ATTR \_ sizes**</dt> <dt>0X0</dt> </dl>                                                                     | El parámetro *pBuffer* contiene un puntero a una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Consulta los tamaños de las estructuras utilizadas en las funciones por mensaje y los intercambios de autenticación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ \_Atributos de \_ seguridad \_ del asunto de ATTR**</dt> <dt>124</dt> </dl> | El parámetro *pBuffer* contiene un puntero a una estructura [**SecPkgContext \_ SubjectAttributes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes) .<br/> Este valor devuelve información acerca de los atributos de seguridad para la conexión.<br/> Este valor solo se admite en el servidor CredSSP.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe los atributos. El tipo de estructura depende del valor del parámetro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve SEC \_ E \_ OK.

Si se produce un error en la función, puede devolver los siguientes códigos de error.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ \_ identificador no válido**</dt> <dt>0x80100003</dt> </dl>       | Error en la función. El parámetro *phContext* especifica un identificador para un contexto incompleto.<br/> |
| <dl> <dt>**S \_ E 0x80090302 de \_ \_ función no admitida**</dt> <dt></dt> </dl> | Error en la función. El valor del parámetro *ulAttribute* no es válido.<br/>                 |



 

## <a name="remarks"></a>Observaciones

La estructura a la que apunta el parámetro *pBuffer* varía en función del atributo que se consulta.

Mientras que el autor de la llamada debe asignar la propia estructura *pbuffer* , el SSP asigna la memoria necesaria para almacenar los miembros de tamaño variable de la estructura *pBuffer* . La memoria asignada por el SSP se debe liberar mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                   |
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

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Tamaños de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
