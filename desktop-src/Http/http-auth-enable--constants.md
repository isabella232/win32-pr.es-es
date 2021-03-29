---
title: Constantes de HTTP_AUTH_ENABLE_ (http. h)
description: Defina los esquemas de autenticación que pueden habilitarse en un grupo de direcciones URL.
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
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492832"
---
# <a name="http_auth_enable_-constants"></a>\_ \_ Habilitación de las constantes de autenticación HTTP \_

Las constantes de **\_ \_ habilitación** de la autenticación http definen los esquemas de autenticación que se pueden habilitar en un grupo de direcciones URL.

Estas constantes se utilizan en la estructura [**de \_ \_ \_ información de autenticación del servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_autenticación HTTP \_ habilitada \_ básica**
</dt> <dd> <dl> <dt>



El esquema de autenticación básica está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_autenticación HTTP \_ habilitar \_ Resumen**
</dt> <dd> <dl> <dt>



El esquema de autenticación implícita está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_autenticación HTTP \_ habilitar \_ Kerberos**
</dt> <dd> <dl> <dt>



El esquema de autenticación Kerberos está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_marca http auth \_ ex habilitar el \_ \_ \_ \_ \_ almacenamiento en caché de credenciales de Kerberos**
</dt> <dd> <dl> <dt>



El almacenamiento en caché de credenciales de Kerberos está habilitado.

**Windows Server 2003 y anteriores:** No disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_credencial de \_ \_ captura de \_ marca \_ de autenticación http**
</dt> <dd> <dl> <dt>



La API del servidor HTTP captura la identidad del autor de la llamada y la usa solo para la autenticación para los esquemas Negotiate y Kerberos.

**Windows Server 2003 y anteriores:** No disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_autenticación HTTP \_ habilitar \_ NTLM**
</dt> <dd> <dl> <dt>



El esquema de autenticación NTLM está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_autenticación HTTP \_ habilitar \_ Negotiate**
</dt> <dd> <dl> <dt>



El esquema de autenticación Negotiate está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_habilitación de autenticación HTTP \_ \_**
</dt> <dd> <dl> <dt>



Están habilitados todos los esquemas de autenticación.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API del servidor HTTP versión 2,0 constantes](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_información de \_ autenticación del servidor HTTP \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





