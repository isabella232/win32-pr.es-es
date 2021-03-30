---
title: Constantes de información y errores relacionados con EAP (Eaphosterror. h)
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079462"
---
# <a name="eap-related-error-and-information-constants"></a>Constantes de información y errores relacionados con EAP

Grupos individuales de constantes de información y errores relacionados con EAP comunes a todas las tecnologías de API de EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ primero**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con EAPHost se producirá **\_ \_ \_ primero entre EAP e** EAPHost y **EAP \_ e \_ EAPHost en \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST en \_ último lugar** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con EAPHost se producirá **\_ \_ \_ primero entre EAP e** EAPHost y **EAP \_ e \_ EAPHost en \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**\_primero EAP I \_ EAPHOST \_** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativo relacionado con EAPHost se producirá primero entre el **EAP \_ i \_ EAPHost \_** y el **EAP \_ i EAPHost en \_ \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ en \_ último lugar**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativo relacionado con EAPHost se producirá primero entre el **EAP \_ i \_ EAPHost \_** y el **EAP \_ i EAPHost en \_ \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**no \_ se \_ \_ \_ puede obtener acceso al almacén de certificados EAP E**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Ni el autenticador ni el mismo nivel pueden tener acceso al almacén de certificados.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ no está instalado el método \_ EAPHOST de EAP E**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



El método EAP solicitado no está instalado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_ \_ \_ método THIRDPARTY de \_ \_ host \_ de EAPHost de EAP E**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



El host del método de terceros no responde y se reinició automáticamente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAPQEC de EAPHost de EAP \_ E \_ \_ \_ inaccesible**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost no puede comunicarse con el [cliente de cumplimiento de cuarentena](/windows/desktop/NAP/nap-client-architecture) de EAP (qec) en un cliente habilitado para protección de [acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identidad EAP \_ E \_ EAPHOST \_ desconocida**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost devuelve este error si el autenticador no supera la autenticación después de enviar la identidad del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**error de autenticación de EAP \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost devuelve este error en caso de error de autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ \_ no se pudo negociar EAP de EAPHost de EAP**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost registra este evento de información cuando el cliente y el servidor no están configurados con tipos de EAP compatibles.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ paquete no válido del método EAPHOST de EAP E \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Un método EAP recibió un paquete EAP que no se puede procesar. Otro nombre para **el \_ \_ \_ \_ \_ paquete no válido del método EAPHost de EAP E** es un **\_ \_ \_ paquete no válido del método EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_paquete remoto de EAPHost de EAP E \_ \_ \_ no válido \_**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost recibió un paquete que no se puede procesar. Otro nombre para **el \_ \_ \_ \_ \_ paquete remoto no válido de EAPHost de EAP E** es un **\_ \_ paquete no válido de EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**XML de EAPHost de EAP \_ E \_ \_ \_ incorrecto** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Error en la validación del esquema de configuración de EAPHost.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**la \_ configuración del método EAP E no es \_ \_ \_ \_ \_ compatible con \_ SSO**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 o posterior: el método EAP no admite el inicio de sesión único (SSO) para la configuración proporcionada.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_no se \_ \_ \_ \_ admite la operación de método EAPHOST de EAP \_ E**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost devuelve este error cuando un método EAP configurado no admite una operación solicitada (llamada a procedimiento).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_ \_ primer usuario de EAP E \_**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá primero entre los usuarios de **EAP \_ e \_ \_** **EAP \_ \_ \_** e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_ \_ último usuario de EAP E \_** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el usuario se producirá primero entre los usuarios de **EAP \_ e \_ \_** **EAP \_ \_ \_** e.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ \_ primero**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre el usuario de **EAP \_ i \_ \_ primero** y el **usuario de EAP \_ i en \_ \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ último usuario de \_ EAP**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Define el límite de los informes de información; cualquier registro de eventos informativos relacionado con EAP se producirá entre el usuario de **EAP \_ i \_ \_ primero** y el **usuario de EAP \_ i en \_ \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**certificado de usuario de EAP \_ E \_ \_ \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost no encontró un certificado de usuario para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**certificado de usuario de EAP \_ E \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



El certificado de usuario para la autenticación no tiene un conjunto de uso mejorado de clave (EKU) adecuado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**certificado de usuario de EAP \_ E \_ \_ \_ expirado**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost encontró un certificado de usuario expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**certificado de usuario de EAP \_ E \_ \_ \_ revocado**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Se ha revocado el certificado de usuario que se usa para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_error de \_ \_ otro certificado \_ de \_ usuario de EAP E**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Se produjo un error desconocido con la certificación de usuario usada para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**certificado de usuario de EAP \_ E \_ \_ \_ rechazado** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



El autenticador rechazó la certificación del usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**ERROR en la cuenta de usuario de EAP \_ I \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Se recibió un error de EAP después de un intercambio de identidades que indica la probabilidad de que se produzca un problema con la cuenta del usuario que realiza la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_credenciales de usuario de EAP E \_ \_ \_ rechazadas**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



El autenticador rechazó las credenciales de usuario para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**contraseña del nombre de usuario de EAP \_ E \_ \_ \_ \_ rechazada**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 o posterior: error de autenticación. El autenticador rechazó las credenciales de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ no \_ \_ lector de tarjeta inteligente \_**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 o posterior: no se encontró ningún lector de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ servidor \_ primero**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá primero entre el **\_ \_ servidor \_ EAP e** y el **\_ servidor EAP e \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_ \_ último servidor EAP \_ E**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el servidor se producirá primero entre el **\_ \_ servidor \_ EAP e** y el **\_ servidor EAP e \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ \_ \_ no se encontró el certificado \_ del servidor EAP E**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost no encontró el certificado de servidor para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_certificado de servidor EAP E \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



El certificado de servidor que se va a usar para la autenticación no tiene un conjunto de uso mejorado de clave (EKU) adecuado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**el \_ certificado del servidor EAP E ha \_ \_ \_ expirado**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost encontró un certificado de servidor expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**se \_ ha \_ \_ revocado el certificado de servidor EAP E \_**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Se ha revocado el certificado de servidor que se usa para la autenticación.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_error de \_ \_ otro certificado \_ de servidor EAP E \_**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Se produjo un error desconocido con el certificado de servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ \_ \_ primero certificado raíz de usuario de EAP E \_**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá **\_ \_ \_ \_ \_ primero** entre el certificado **raíz de usuario de EAP \_ \_ \_ \_ \_ e** y el certificado raíz de usuario de EAP e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ último certificado raíz de usuario de EAP \_**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz de usuario se producirá **\_ \_ \_ \_ \_ primero** entre el certificado **raíz de usuario de EAP \_ \_ \_ \_ \_ e** y el certificado raíz de usuario de EAP e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró el certificado raíz de usuario de EAP.**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost no encontró un certificado en un almacén de certificados raíz de confianza para la validación de la certificación de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_certificado raíz de usuario de EAP E \_ \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



Error de autenticación porque el certificado raíz utilizado para esta red no es válido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_certificado raíz de usuario de EAP E \_ \_ \_ \_ expirado**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



El certificado raíz de confianza necesario para la validación de certificado de usuario ha expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificado raíz de servidor EAP E \_ \_ \_ primero**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá primero entre el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_** y el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_ EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ último certificado raíz de servidor EAP E \_**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Define el límite de los informes de errores; cualquier error relacionado con el certificado raíz del servidor se producirá primero entre el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_** y el certificado **\_ raíz del servidor EAP e \_ \_ \_ \_ EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró el certificado raíz del servidor EAP E**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost no encontró un certificado raíz en un almacén de certificados raíz de confianza para la validación de la certificación del servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificado raíz del servidor EAP E \_ \_ \_ no válido** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



No se pudo realizar la autenticación porque el certificado de servidor necesario para esta red en el equipo servidor no es válido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_nombre de \_ certificado raíz del servidor EAP E \_ \_ \_ \_ necesario**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



No se pudo realizar la autenticación porque el certificado del equipo servidor no tiene especificado un nombre de servidor.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Hay nombres alternativos para determinados errores:

-   Otro nombre para **el \_ \_ \_ \_ \_ paquete no válido del método EAPHost de EAP E** es un **\_ \_ \_ paquete no válido del método EAP**.
-   Otro nombre para **el \_ \_ \_ \_ \_ paquete remoto no válido de EAPHost de EAP E** es un **\_ \_ paquete no válido de EAP**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de EAPHost comunes](common-eap-host-error-constants.md)
</dt> </dl>

 

