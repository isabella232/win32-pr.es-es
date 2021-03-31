---
title: Valores de error de registro de MDM (MDMRegistration. h)
description: Los siguientes valores de error son con el registro de MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c21732a102b052d4be51cbbbf5627e42cc487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079450"
---
# <a name="mdm-registration-error-values"></a>Valores de error de registro de MDM

Los siguientes valores de error son con el registro de MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ no coinciden los tipos de tipo de. \_**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



DataType no coincide con el tipo de DataType esperado.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_error de \_ formato de mensaje de dispositivo MREGISTER E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Esquema no válido, error de formato de mensaje del servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_error de \_ formato de mensaje de dispositivo MENROLL E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Esquema no válido, error de formato de mensaje del servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**\_error de \_ autenticación de dispositivo \_ \_ de MREGISTER E**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



El servidor no pudo autenticar al usuario.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**\_error de \_ autenticación de dispositivo \_ \_ de MENROLL E**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



El servidor no pudo autenticar al usuario.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_error de \_ autorización del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



El usuario no está autorizado para inscribirse.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_error de \_ autorización del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



El usuario no está autorizado para inscribirse.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER \_ E \_ \_ CERTIFCATEREQUEST \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



El usuario no tiene permiso para la plantilla de certificado o no se puede tener acceso a la entidad de certificación.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL \_ E \_ \_ CERTIFCATEREQUEST \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



El usuario no tiene permiso para la plantilla de certificado o no se puede tener acceso a la entidad de certificación.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER \_ E \_ \_ CONFIGMGRSERVER \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Se produjo un error en el servidor de administración, como un error de acceso a la base de datos.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL \_ E \_ \_ CONFIGMGRSERVER \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Se produjo un error en el servidor de administración, como un error de acceso a la base de datos.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER \_ E \_ \_ INTERNALSERVICE \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Se produjo una excepción no controlada en el servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL \_ E \_ \_ INTERNALSERVICE \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Se produjo una excepción no controlada en el servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER \_ E \_ \_ INVALIDSECURITY \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Se produjo una excepción no controlada en el servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL \_ E \_ \_ INVALIDSECURITY \_ error de dispositivo**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Se produjo una excepción no controlada en el servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ error desconocido del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Error desconocido del servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ error desconocido del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Error desconocido del servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**\_ \_ Registro \_ en curso de MREGISTER E \_**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Hay otra operación de inscripción en curso.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_ \_ inscripción \_ en curso de MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Hay otra operación de inscripción en curso.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**el \_ dispositivo MREGISTER E \_ \_ ya está \_ registrado**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo ya está inscrito.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**el \_ dispositivo MENROLL E \_ \_ ya está \_ inscrito**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



El dispositivo ya está inscrito.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_dispositivo MREGISTER \_ E \_ no \_ registrado**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo no está inscrito.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**el \_ dispositivo MENROLL E \_ \_ no está \_ inscrito**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



El dispositivo no está inscrito.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**detección de MREGISTER \_ E \_ \_ redirigida**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Ya no se usa.

**Windows 8.1:** Se necesita redirección.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**\_error del dispositivo MREGISTER E \_ \_ no \_ registrado en ad \_ \_**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo no está registrado con Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**fecha de certificado de detección de MENROLL \_ \_ \_ s \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Durante la detección, la fecha del certificado en segundos no era válida.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**error de detección de MREGISTER \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Ya no se usa.

**Windows 8.1:** Error en la detección; se necesita redirección.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ contraseña \_ necesaria**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Se necesita una contraseña, pero no se ha proporcionado.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**ERROR de MENROLL \_ E \_ WAB \_**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Se produjo un error durante la inscripción de WAB.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**Conectividad de MENROLL \_ E \_**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Se produjo un error de red, como DNS o un tiempo de espera de red.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**inscripción de MENROLL \_ S \_ \_ suspendida**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



La inscripción se suspendió. Ya no se admite.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



El certificado SSL no era válido.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



El usuario ya ha inscrito demasiados dispositivos. Elimine o anule la inscripción de los antiguos para corregir este error. Tenga en cuenta que el usuario puede resolver este error sin necesidad de ayuda del administrador.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

código 0x80180014
</dt> <dt>



No se admite una plataforma específica (por ejemplo, Windows) o una versión. La corrección general para este error es actualizar el dispositivo.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



La administración de dispositivos móviles generalmente no es compatible con este dispositivo: el usuario puede llamar al administrador, pero no es probable que resuelva este problema.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



El dispositivo está intentando renovar, pero el servidor rechazó la solicitud. Compruebe la hora del dispositivo. Es posible que el usuario pueda resolver este error volviendo a inscribirlo.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ inmantenimiento**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



La cuenta está en mantenimiento; Inténtelo de nuevo más tarde. El usuario puede volver a intentarlo más tarde. Sin embargo, el usuario puede elegir llamar al administrador para determinar la programación de mantenimiento.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



La licencia del usuario está en una inscripción de bloqueo de estado incorrecto. el usuario deberá llamar al administrador.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



El servidor rechazó los datos de inscripción; es posible que el servidor no esté configurado correctamente.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



El servidor solicitó HTTP en lugar de HTTPS, pero no se aceptó.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ Estado incorrecto de la plataforma MENROLL E \_**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Se intentó realizar una operación no válida, intentando inscribir el mismo dispositivo dos veces o anular la inscripción de un dispositivo desconocido.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**ERROR de licencia de la \_ plataforma MENROLL E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



La versión de Windows instalada en el cliente no admite este tipo de inscripción.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**\_ \_ \_ error desconocido de la plataforma MENROLL E \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Se ha producido un error desconocido en el cliente.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ Prov \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



No se pudo realizar el aprovisionamiento en el CSP del almacén de certificados.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ Prov \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Error de aprovisionamiento en un CPP W7/DMAcc.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ Prov \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Error de aprovisionamiento en un CSP de cliente de DM.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ Prov \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Error de aprovisionamiento en un CSP de Passport for work.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ Prov \_ CSP \_ varios**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Error de aprovisionamiento en un CSP no indicado anteriormente.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ Prov \_ desconocido**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Error de aprovisionamiento, pero no se ha indicado un CSP específico.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ Prov \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Al intentar enlazar la clave pública o el certificado público, no se encontró el certificado público: al intentar enlazar la clave pública o de certificado público, o al buscar la carga de aprovisionamiento (quizás se dirija al almacén equivocado).

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ Prov \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Error de aprovisionamiento en el CSP EnterpriseAppManagement.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**\_Administración de dispositivos MENROLL E \_ \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



Se bloqueó la administración de dispositivos móviles (MDM), posiblemente directiva de grupo o la función [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**error de MENROLL \_ E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



No se pudo crear la clave privada.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ no \_ pudo \_ encontrar el \_ certificado**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



Se solicitó la autenticación del certificado, pero no se encontró un certificado para usarlo.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ \_ mensaje vacío**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



El servidor respondió con HTTP 200, pero el mensaje estaba vacío.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ cancelado por el usuario \_** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



El usuario canceló la operación.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E \_ MDM \_ no \_ configurado**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



La administración de dispositivos móviles (MDM) no está configurada.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>MDMRegistration. h</dt> </dl> |



 

 





