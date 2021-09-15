---
title: Errores relacionados con EAP e constantes de información (Eaphosterror.h)
description: Grupos individuales de constantes de información y errores relacionados con EAP comunes a todas las tecnologías de API de EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360148"
---
# <a name="eap-related-error-and-information-constants"></a>Errores relacionados con EAP e constantes de información

Grupos individuales de constantes de información y errores relacionados con EAP comunes a todas las tecnologías de API de EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define el límite de los informes de errores; se producirá cualquier error relacionado con EAPHost entre **EAP \_ E \_ EAPHOST \_ FIRST** y **EAP E \_ \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST \_ LAST** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define el límite de los informes de errores; se producirá cualquier error relacionado con EAPHost entre **EAP \_ E \_ EAPHOST \_ FIRST** y **EAP E \_ \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST \_ FIRST** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAPHost se producirá entre **EAP \_ I \_ EAPHOST \_ FIRST** y **EAP I \_ \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHOST \_ LAST**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAPHost se producirá entre **EAP \_ I \_ EAPHOST \_ FIRST** y **EAP I \_ \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**NO SE \_ PUEDE ACCEDER AL ALMACÉN DE CERTIFICADOS EAP \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Ni el autenticador ni el mismo nivel pueden acceder al almacén de certificados.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EL \_ MÉTODO EAP E \_ EAPHOST NO ESTÁ \_ \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



El método EAP solicitado no está instalado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHOST \_ THIRDPARTY \_ METHOD \_ HOST \_ RESET**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



El host del método de terceros no responde y se reinició automáticamente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ EAPQEC \_ INACCESIBLE**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost no puede comunicarse con el cliente de cumplimiento de [cuarentena](/windows/desktop/NAP/nap-client-architecture) de EAP (QEC) en [un](/windows/desktop/NAP/network-access-protection-start-page) cliente habilitado para protección de acceso a redes (NAP).


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**IDENTIDAD DE \_ EAP E \_ EAPHOST \_ \_ DESCONOCIDA**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost devuelve este error si el autenticador produce un error en la autenticación después de enviar la identidad del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**ERROR \_ DE \_ AUTENTICACIÓN EAP E \_**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost devuelve este error en caso de error de autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**ERROR EN \_ LA NEGOCIACIÓN DE EAP I \_ EAPHOST \_ EAP \_ \_**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost registra este evento de información cuando el cliente y el servidor no están configurados con tipos de EAP compatibles.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**PAQUETE \_ NO VÁLIDO DEL MÉTODO EAP E \_ EAPHOST \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Un método EAP recibió un paquete EAP que no se puede procesar. Otro nombre para **EAP \_ E \_ EAPHOST METHOD INVALID \_ \_ \_ PACKET** es **EAP METHOD INVALID \_ \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**PAQUETE \_ NO VÁLIDO REMOTO EAP E \_ EAPHOST \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost recibió un paquete que no se puede procesar. Otro nombre para **EAP \_ E \_ EAPHOST REMOTE INVALID \_ \_ \_ PACKET** es **EAP INVALID \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHOST XML \_ \_ MALFORMADO** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Error en la validación del esquema de configuración de EAPHost.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP \_ E METHOD CONFIG NO ADMITE \_ \_ \_ \_ \_ SSO \_**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 o posterior: el método EAP no admite el inicio de sesión único (SSO) para la configuración proporcionada.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**NO \_ SE ADMITE LA OPERACIÓN DEL MÉTODO EAP E \_ \_ \_ \_ \_ EAPHOST**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost devuelve este error cuando un método EAP configurado no admite una operación solicitada (llamada a procedimiento).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá entre **EAP \_ E USER \_ \_ FIRST** y **EAP E USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ USER \_ LAST** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá entre **EAP \_ E USER \_ \_ FIRST** y **EAP E USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre **EAP \_ I USER \_ \_ FIRST** y **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I \_ USER \_ LAST**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre **EAP \_ I USER \_ \_ FIRST** y **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**NO \_ SE ENCONTRÓ EL CERTIFICADO DE USUARIO EAP \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost no encontró un certificado de usuario para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**CERTIFICADO \_ DE USUARIO EAP E NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



El certificado de usuario que es usuario para la autenticación no tiene establecido el uso de clave extendida (EKU) adecuado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EL CERTIFICADO \_ DE USUARIO EAP E \_ \_ \_ EXPIRÓ**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost encontró un certificado de usuario expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**CERTIFICADO \_ DE USUARIO EAP E \_ \_ \_ REVOCADO**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Se ha revocado el certificado de usuario que se usa para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP \_ E \_ USER \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Se produjo un error desconocido con la certificación de usuario que se usa para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**CERTIFICADO \_ DE USUARIO EAP E \_ \_ \_ RECHAZADO** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



El autenticador rechazó la certificación de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP \_ I \_ USER \_ ACCOUNT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Se recibió un error de EAP después de un intercambio de identidades, lo que indica la probabilidad de que se produzca un problema con la cuenta del usuario autenticado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**CREDENCIALES \_ DE USUARIO EAP E \_ \_ \_ RECHAZADAS**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



El autenticador rechazó las credenciales de usuario para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**CONTRASEÑA \_ DE NOMBRE DE USUARIO EAP E \_ \_ \_ \_ RECHAZADA**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 o posterior: error de autenticación. El autenticador rechazó las credenciales de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ NO \_ SMART \_ CARD \_ READER**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 o posterior: no se encontró ningún lector de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ SERVER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá entre **EAP \_ E SERVER \_ \_ FIRST** y **EAP E SERVER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá entre **EAP \_ E SERVER \_ \_ FIRST** y **EAP E SERVER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**NO SE ENCONTRÓ EL CERTIFICADO DE SERVIDOR EAP \_ \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost no encontró el certificado de servidor para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**CERTIFICADO \_ DE SERVIDOR EAP E NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



El certificado de servidor que es usuario para la autenticación no tiene un conjunto de uso de clave extendido (EKU) adecuado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EL CERTIFICADO \_ DE SERVIDOR EAP E \_ \_ \_ EXPIRÓ**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost encontró un certificado de servidor expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**CERTIFICADO \_ DE SERVIDOR EAP E \_ \_ \_ REVOCADO**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Se ha revocado el certificado de servidor que se usa para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP \_ E \_ SERVER \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Error desconocido con el certificado de servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá entre **EAP E USER ROOT CERT \_ \_ \_ \_ \_ FIRST** y **EAP E USER ROOT CERT \_ \_ \_ \_ \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá entre **EAP E USER ROOT CERT \_ \_ \_ \_ \_ FIRST** y **EAP E USER ROOT CERT \_ \_ \_ \_ \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**NO \_ SE ENCONTRÓ EL CERTIFICADO RAÍZ DE USUARIO \_ \_ \_ \_ DE \_ EAP E**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost no pudo encontrar un certificado en un almacén de certificados raíz de confianza para la validación de la certificación de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**CERTIFICADO \_ RAÍZ DE USUARIO EAP E NO \_ \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



Error de autenticación porque el certificado raíz usado para esta red no es válido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EL CERTIFICADO \_ RAÍZ DE USUARIO EAP E \_ \_ \_ \_ EXPIRÓ**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



El certificado raíz de confianza necesario para la validación de certificados de usuario ha expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá entre **EAP E SERVER ROOT CERT \_ \_ \_ \_ \_ FIRST** y **EAP E SERVER ROOT CERT \_ \_ \_ \_ \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá entre **EAP E SERVER ROOT CERT \_ \_ \_ \_ \_ FIRST** y **EAP E SERVER ROOT CERT \_ \_ \_ \_ \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**NO SE ENCONTRÓ EL CERTIFICADO RAÍZ DEL SERVIDOR EAP \_ \_ \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost no pudo encontrar un certificado raíz en un almacén de certificados raíz de confianza para la validación de certificación del servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**CERTIFICADO \_ RAÍZ DEL SERVIDOR EAP E NO \_ \_ \_ \_ VÁLIDO** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



Error de autenticación porque el certificado de servidor necesario para esta red en el equipo servidor no es válido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**SE REQUIERE EL NOMBRE DEL CERTIFICADO RAÍZ DEL SERVIDOR EAP \_ \_ \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



Error de autenticación porque el certificado del equipo servidor no tiene especificado un nombre de servidor.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Hay nombres alternativos para determinados errores:

-   Otro nombre para **EAP \_ E \_ EAPHOST METHOD INVALID \_ \_ \_ PACKET** es **EAP METHOD INVALID \_ \_ \_ PACKET**.
-   Otro nombre para **EAP \_ E \_ EAPHOST REMOTE INVALID \_ \_ \_ PACKET** es **EAP INVALID \_ \_ PACKET**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Eaphosterror.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes comunes de EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

 

