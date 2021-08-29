---
title: HTTP_AUTH_ENABLE_ constantes (Http.h)
description: Defina esquemas de autenticación que se puedan habilitar en un grupo de direcciones URL.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa66013700dc1ad6b091ccf4738f2af456cb29384fd2d48b2d17a0a244019a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394503"
---
# <a name="http_auth_enable_-constants"></a>Constantes ENABLE \_ de HTTP AUTH \_ \_

Las **constantes HTTP \_ AUTH \_ ENABLE** definen esquemas de autenticación que se pueden habilitar en un grupo de direcciones URL.

Estas constantes se usan en la estructura [**HTTP \_ SERVER AUTHENTICATION \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP \_ AUTH \_ ENABLE \_ BASIC**
</dt> <dd> <dl> <dt>



El esquema de autenticación básica está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP \_ AUTH \_ ENABLE \_ DIGEST**
</dt> <dd> <dl> <dt>



El esquema de autenticación implícita está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HABILITACIÓN DE KERBEROS \_ DE \_ AUTENTICACIÓN \_ HTTP**
</dt> <dd> <dl> <dt>



El esquema de autenticación Kerberos está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**MARCA HTTP \_ AUTH \_ EX ENABLE \_ KERBEROS \_ \_ \_ CREDENTIAL \_ CACHING**
</dt> <dd> <dl> <dt>



El almacenamiento en caché de credenciales de Kerberos está habilitado.

**Windows Server 2003 y anteriores:** No disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_CREDENCIAL DE CAPTURA DE LA \_ \_ \_ MARCA HTTP AUTH EX \_**
</dt> <dd> <dl> <dt>



La API del servidor HTTP captura la identidad del autor de la llamada y la usa para la autenticación solo para los esquemas Negotiate y Kerberos.

**Windows Server 2003 y anteriores:** No disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP \_ AUTH \_ ENABLE \_ NTLM**
</dt> <dd> <dl> <dt>



El esquema de autenticación NTLM está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP \_ AUTH \_ ENABLE \_ NEGOTIATE**
</dt> <dd> <dl> <dt>



El esquema de autenticación Negotiate está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP \_ AUTH \_ ENABLE \_ ALL**
</dt> <dd> <dl> <dt>



Todos los esquemas de autenticación están habilitados.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de LA API del servidor HTTP versión 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMACIÓN \_ DE \_ AUTENTICACIÓN DEL SERVIDOR \_ HTTP**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





