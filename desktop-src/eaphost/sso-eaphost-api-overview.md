---
title: Introducción a la API de EAPHost de SSO
description: Proporciona información general sobre las API de EAPHost que admiten el inicio de sesión único (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a38c6dd35dd2506f8aa26412b09db0f9c9951241bd0f017ed5e55d7f5484b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085880"
---
# <a name="sso-eaphost-api-overview"></a>Introducción a la API de EAPHost de SSO

En este tema se proporciona información general sobre las API de EAPHost que admiten el inicio de sesión único (SSO). Para escenarios específicos de SSO, consulte [Escenarios de EAPHost de SSO.](why-eaphost-sso.md)

## <a name="eaphost-enumerations"></a>Enumeraciones eaphost

Las enumeraciones siguientes admiten sso.



| Nombre                                                                    | Propósito                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**TIPO DE \_ CAMPO DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Define un conjunto de posibles tipos de campos de entrada disponibles al consultar las credenciales de usuario.    |
| [**TIPO DE \_ DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Especifica los tipos de datos de contexto de interfaz de usuario interactivos proporcionados a determinadas llamadas API suplicantes. |



 

## <a name="eaphost-structures"></a>Estructuras eaphost

Las siguientes estructuras de datos admiten sso.



| Nombre                                                                     | Propósito                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS DE \_ CAMPO DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene los datos asociados a un único campo de entrada.                                                                                                                         |
| [**MATRIZ DE \_ CAMPOS DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un conjunto de estructuras [**DE DATOS DE CAMPO DE \_ \_ ENTRADA \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) DE CONFIGURACIÓN DE EAP que contienen colectivamente los datos de campo de entrada del usuario obtenidos del usuario. |
| [**DATOS DE \_ LA INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contiene información de configuración para los componentes interactivos de la interfaz de usuario que se genera en un suplicante EAP.                                                                                   |
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                   | Contiene las credenciales eap antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                 | Contiene las credenciales eap antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**SOLICITUD \_ DE SOLICITUD DE \_ EXPIRACIÓN \_ CRED DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contiene las credenciales eap antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contiene las credenciales eap antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API del mismo nivel de EAPHost (supplicant)

Las siguientes funciones suplicantes admiten sso.

Las [**funciones EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) y [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) son exclusivas del inicio de sesión único.



| Nombre                                                                                                             | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Pedido al que se llama |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtiene los campos de entrada para los componentes de interfaz de usuario interactivos que se deben generar en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permite al usuario determinar qué tipo de credenciales requieren los métodos para realizar la autenticación en un escenario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Convierte la información del usuario en un BLOB de usuario que pueden consumir las funciones en tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtiene un blob de credenciales que se puede usar para iniciar la autenticación a partir de la entrada del usuario recibida por la interfaz de usuario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | El suplicante usa la marca **EAP \_ FLAG PRE \_ \_ LOGON** para indicar que EAPHost debe proporcionar sso. Si se devuelve el código de acción [EapHostPeerResponseInvokeUI,](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Si no se devuelve el código de acción [EapHostPeerResponseInvokeUI,](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) EAPHost continúa con la secuencia de llamada normal y no SSO. Para obtener más información, consulte [Secuencia de llamadas api de suplicación.](supplicant-api-call-sequence.md)<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API del método del mismo nivel de EAPHost

Las siguientes funciones del mismo nivel admiten sso.

Las [**funciones EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) y [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) son exclusivas del inicio de sesión único.



| Nombre                                                                                                      | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Pedido al que se llama |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define la implementación de una API de método EAP que proporciona los campos de entrada para los componentes de interfaz de usuario interactivos que se deben generar en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define la implementación de una función específica del método EAP que obtiene los campos de entrada de credenciales de SSO de EAP para ese método EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convierte la información del usuario en un BLOB de usuario que pueden consumir las funciones en tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define la implementación de una función de método EAP que obtiene los datos blob de usuario proporcionados por la interfaz de usuario interactiva de SSO que se genera en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | La **marca EAP FLAG PRE \_ \_ \_ LOGON** indica que EAPHost debe proporcionar sso. En un escenario de SSO si se devuelve el código de acción **EapPeerResponseInvokeUI,** EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapPeerQueryUserBlobFromCredentialInputFields.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Si no se devuelve el código de acción **EapPeerResponseInvokeUI,** EAPHost continúa con la secuencia de llamada normal y no SSO. Para obtener más información, consulte [Secuencia de llamadas api del método del mismo nivel.](peer-method-api-call-sequence.md)<br/> | 3            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> </dl>

 

