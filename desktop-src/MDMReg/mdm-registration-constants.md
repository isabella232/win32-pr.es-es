---
title: Valores de error de registro de MDM (MDMRegistration.h)
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
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548990"
---
# <a name="mdm-registration-error-values"></a>Valores de error de registro de MDM

Los siguientes valores de error son con el registro de MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DATATYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



El tipo de datos no coincide con el tipo de datos esperado.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER \_ E \_ DEVICE \_ MESSAGE \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Esquema no válido, Error de formato de mensaje del servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**ERROR DE \_ FORMATO DE MENSAJE DE \_ \_ \_ DISPOSITIVO \_ MENROLL E**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Esquema no válido, Error de formato de mensaje del servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER \_ E \_ DEVICE \_ AUTHENTICATION \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



El servidor no pudo autenticar al usuario.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**ERROR DE \_ AUTENTICACIÓN \_ DE DISPOSITIVO \_ \_ MENROLL E**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



El servidor no pudo autenticar al usuario.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**ERROR DE AUTORIZACIÓN DEL DISPOSITIVO MREGISTER \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



El usuario no está autorizado para inscribirse.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**ERROR DE AUTORIZACIÓN DEL DISPOSITIVO MENROLL \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



El usuario no está autorizado para inscribirse.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**MREGISTER \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



El usuario no tiene permiso para la plantilla de certificado o no se puede acceder a la entidad de certificación.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**MENROLL \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



El usuario no tiene permiso para la plantilla de certificado o no se puede acceder a la entidad de certificación.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER \_ E \_ DEVICE \_ CONFIGMGRSERVER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Se produjo un error en el servidor de administración, como un error de acceso a la base de datos.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**MENROLL \_ E \_ DEVICE \_ CONFIGMGRSERVER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Se produjo un error en el servidor de administración, como un error de acceso a la base de datos.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**MREGISTER \_ E \_ DEVICE \_ INTERNALSERVICE \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Se produjo una excepción no controlada en el servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**MENROLL \_ E \_ DEVICE \_ INTERNALSERVICE \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Hubo una excepción no controlada en el servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER \_ E \_ DEVICE \_ INVALIDSECURITY \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Se produjo una excepción no controlada en el servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**ERROR DE \_ SEGURIDAD DE LA SEGURIDAD DEL DISPOSITIVO \_ \_ MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Se produjo una excepción no controlada en el servidor.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**ERROR DESCONOCIDO DEL DISPOSITIVO MREGISTER \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Error de servidor desconocido.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**ERROR DESCONOCIDO DEL DISPOSITIVO MENROLL \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Error de servidor desconocido.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**REGISTRO E DE MREGISTER \_ \_ EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Actualmente se está realizando otra operación de inscripción.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**INSCRIPCIÓN \_ MENROLL E \_ \_ EN \_ CURSO**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Actualmente se está realizando otra operación de inscripción.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER \_ E \_ DEVICE \_ ALREADY \_ REGISTERED**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo ya está inscrito.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**DISPOSITIVO MENROLL \_ E \_ YA \_ \_ INSCRITO**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



El dispositivo ya está inscrito.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER \_ E \_ DEVICE \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo no está inscrito.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**DISPOSITIVO MENROLL \_ E \_ NO \_ \_ INSCRITO**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



El dispositivo no está inscrito.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ DISCOVERY \_ REDIRECTED**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Ya no se usa.

**Windows 8.1:** Se necesita redirección.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER \_ E \_ DEVICE \_ NOT \_ AD \_ REGISTERED \_ ERROR**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Ya no se usa.

**Windows 8.1:** El dispositivo no está registrado con Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL \_ E \_ DISCOVERY \_ SEC \_ CERT \_ DATE \_ INVALID**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Durante la detección, la fecha del certificado por segundo no era válida.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**ERROR DE \_ DETECCIÓN DE MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Ya no se usa.

**Windows 8.1:** Error de detección; se necesita el redireccionamiento.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ PASSWORD \_ NEEDED**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Se necesita una contraseña, pero no se ha proporcionado.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**ERROR DE MENROLL \_ E \_ \_ WAB**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Error durante la inscripción de WAB.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL \_ E \_ CONNECTIVITY**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Se produjo un error de red, como DNS o un tiempo de espera de red.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**INSCRIPCIÓN DE MENROLL \_ S \_ \_ SUSPENDIDA**
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



El usuario ya ha inscrito demasiados dispositivos. Elimine o desenrolle los antiguos para corregir este error. Tenga en cuenta que el usuario puede resolver este error sin ayuda del administrador.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



No se admite una plataforma específica (por ejemplo, Windows) o una versión. La corrección general de este error es actualizar el dispositivo.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



Por lo general, la administración de dispositivos móviles no se admite para este dispositivo: el usuario puede llamar al administrador, pero es poco probable que resuelva este problema.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



El dispositivo está intentando renovarse, pero el servidor rechazó la solicitud. Comprobación de la hora en el dispositivo. Es posible que el usuario pueda resolver este error mediante la rescripción.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ INMAINTENANCE**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



La cuenta está en mantenimiento; vuelva a intentarlo más adelante. El usuario puede volver a intentarlo más adelante. Sin embargo, el usuario puede optar por llamar al administrador para determinar la programación de mantenimiento.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



La licencia del usuario está en estado de bloqueo de inscripción; el usuario tendrá que llamar al administrador.

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

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**ESTADO INCORRECTO DE \_ \_ LA PLATAFORMA MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Se intentó realizar una operación no válida, como intentar inscribir el mismo dispositivo dos veces o deshacer la inscripción de un dispositivo desconocido.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**ERROR DE \_ LICENCIA DE LA PLATAFORMA MENROLL E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



La versión de Windows instalada en el cliente no admite este tipo de inscripción.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**ERROR DESCONOCIDO \_ DE \_ LA PLATAFORMA MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Error desconocido en el cliente.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ PROV \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Error de aprovisionamiento en el CSP del almacén de certificados.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ PROV \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Error de aprovisionamiento en un CPP W7/DMAcc.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ PROV \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Error de aprovisionamiento en un CSP de cliente dm.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**CSP DE MENROLL \_ E \_ PROV \_ \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Error de aprovisionamiento en un CSP de Passport for Work.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MISC DEL CSP DE MENROLL \_ E \_ \_ \_ PROV**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Error de aprovisionamiento en un CSP no enumerado anteriormente.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ PROV \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Error de aprovisionamiento, pero no se indica un CSP específico.

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ PROV \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Al intentar enlazar el certificado público o la clave privada, no se encontró el certificado público: al intentar enlazar la clave pública o privada, o al buscar la carga de aprovisionamiento (quizás el destino es el almacén incorrecto).

**Windows 8.1:** Esta constante no está disponible antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ PROV \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Error de aprovisionamiento en el CSP de EnterpriseAppManagement.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**ADMINISTRACIÓN DE DISPOSITIVOS MENROLL \_ E \_ \_ \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



Los Administración de dispositivos móviles (MDM) se bloquearon, posiblemente por directiva de grupo o la [**función SetManagedExternally.**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**ERROR DE \_ MENROLL E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



No se pudo crear la clave privada.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH NO PUDO ENCONTRAR EL \_ \_ \_ \_ CERTIFICADO**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



Se solicitó la autenticación de certificado, pero no se pudo encontrar un certificado para usar.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENSAJE VACÍO DE MENROLL \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



El servidor respondió con HTTP 200, pero el mensaje estaba vacío.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ USER \_ CANCELED** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



El usuario canceló la operación.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MDM MENROLL \_ E \_ NO \_ \_ CONFIGURADA**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



La Administración de dispositivos móvil (MDM) no está configurada.

> [!Note]  
> Esta constante no está disponible antes de Windows 10, versión 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>MDMRegistration.h</dt> </dl> |



 

 





