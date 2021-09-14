---
title: Introducción a la API de EAPHost de SSO
description: Proporciona información general sobre las API de EAPHost que admiten el inicio de sesión único (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963411"
---
# <a name="sso-eaphost-api-overview"></a>Introducción a la API de EAPHost de SSO

En este tema se proporciona información general sobre las API de EAPHost que admiten el inicio de sesión único (SSO). Para escenarios específicos de SSO, consulte [Escenarios de EAPHost de SSO.](why-eaphost-sso.md)

## <a name="eaphost-enumerations"></a>Enumeraciones EAPHost

Las enumeraciones siguientes admiten sso.



| Nombre                                                                    | Propósito                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**TIPO DE \_ CAMPO DE ENTRADA DE CONFIGURACIÓN \_ \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Define un conjunto de posibles tipos de campos de entrada disponibles al consultar las credenciales de usuario.    |
| [**TIPO DE \_ DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Especifica los tipos de datos de contexto de interfaz de usuario interactivos proporcionados a determinadas llamadas API suplicantes. |



 

## <a name="eaphost-structures"></a>Estructuras de EAPHost

Las siguientes estructuras de datos admiten SSO.



| Nombre                                                                     | Propósito                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS DEL \_ CAMPO DE ENTRADA DE CONFIGURACIÓN \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene los datos asociados a un único campo de entrada.                                                                                                                         |
| [**MATRIZ DE \_ CAMPOS DE ENTRADA DE CONFIGURACIÓN \_ \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un conjunto de estructuras DE DATOS DE CAMPO DE ENTRADA DE [**\_ CONFIGURACIÓN \_ \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) que contienen colectivamente los datos de campo de entrada del usuario obtenidos del usuario. |
| [**DATOS DE LA \_ INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contiene información de configuración para los componentes de interfaz de usuario interactivos que se genera en un suplicante eap.                                                                                   |
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                   | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                 | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**SOLICITUD \_ DE EXPIRACIÓN CRED \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API del mismo nivel de EAPHost (supplicant)

Las siguientes funciones suplicantes admiten SSO.

Las [**funciones EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) y [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) son exclusivas de SSO.



| Nombre                                                                                                             | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Pedido llamado |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtiene los campos de entrada para los componentes de interfaz de usuario interactivos que se deben generar en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permite al usuario determinar qué tipo de credenciales requieren los métodos para realizar la autenticación en un escenario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Convierte la información del usuario en un BLOB de usuario que pueden consumir las funciones en tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtiene un blob de credenciales que se puede usar para iniciar la autenticación a partir de la entrada del usuario recibida por la interfaz de usuario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | El suplicante usa la marca **EAP \_ FLAG PRE \_ \_ LOGON** para indicar que EAPHost debe proporcionar SSO. Si se devuelve el código de acción [EapHostPeerResponseInvokeUI,](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Si no se devuelve el código de acción [EapHostPeerResponseInvokeUI,](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) EAPHost continúa con la secuencia de llamadas normal y no SSO. Para más información, consulte [Secuencia de llamadas de API suplicante.](supplicant-api-call-sequence.md)<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API del método del mismo nivel de EAPHost

Las siguientes funciones del mismo nivel admiten sso.

Las [**funciones EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) y [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) son exclusivas de SSO.



| Nombre                                                                                                      | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Pedido llamado |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define la implementación de una API de método EAP que proporciona los campos de entrada para los componentes de interfaz de usuario interactivos que se deben generar en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define la implementación de una función específica del método EAP que obtiene los campos de entrada de credenciales de SSO de EAP para ese método EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convierte la información del usuario en un BLOB de usuario que pueden consumir las funciones en tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define la implementación de una función de método EAP que obtiene los datos blob de usuario proporcionados por la interfaz de usuario de SSO interactiva que se genera en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | La **marca EAP FLAG PRE \_ \_ \_ LOGON** indica que EAPHost debe proporcionar SSO. En un escenario de SSO si se devuelve el código de acción **EapPeerResponseInvokeUI,** EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapPeerQueryUserBlobFromCredentialInputFields.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Si no se devuelve el código de acción **EapPeerResponseInvokeUI,** EAPHost continúa con la secuencia de llamadas normal y no SSO. Para obtener más información, vea [Secuencia de llamadas api de métodos del mismo nivel.](peer-method-api-call-sequence.md)<br/> | 3            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> </dl>

 

