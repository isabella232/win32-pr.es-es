---
title: Introducción a la API de EAPHost de SSO
description: Proporciona información general de las API de EAPHost que admiten el inicio de sesión único (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077703"
---
# <a name="sso-eaphost-api-overview"></a>Introducción a la API de EAPHost de SSO

En este tema se proporciona información general sobre las API de EAPHost que admiten el inicio de sesión único (SSO). Para ver escenarios de SSO específicos, consulte [escenarios de EAPHost de SSO](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Enumeraciones de EAPHost

Las enumeraciones siguientes admiten SSO.



| Nombre                                                                    | Propósito                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_tipo de \_ campo de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Define un conjunto de posibles tipos de campo de entrada disponibles cuando se consultan las credenciales de usuario.    |
| [**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Especifica los tipos de datos interactivos de contexto de interfaz de usuario proporcionados a ciertas llamadas API de suplicante. |



 

## <a name="eaphost-structures"></a>Estructuras de EAPHost

Las siguientes estructuras de datos admiten SSO.



| Nombre                                                                     | Propósito                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_datos de \_ campo de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene los datos asociados a un único campo de entrada.                                                                                                                         |
| [**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un conjunto de estructuras de datos de campo de entrada de configuración de EAP que contienen colectivamente los datos de campo de entrada del usuario obtenidos del usuario. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) |
| [**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Contiene información de configuración para los componentes de interfaz de usuario interactivos generados en un suplicante EAP.                                                                                   |
| [**\_solicitud de credenciales de EAP \_**](eap-cred-req.md)                                   | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**respuesta de cred de EAP \_ \_**](eap-cred-resp.md)                                 | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                                                                               |
| [**\_solicitud de \_ expiración de credenciales de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |
| [**respuesta \_ de \_ expiración de credenciales de EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>API del homólogo de EAPHost (suplicante)

Las siguientes funciones del suplicante admiten SSO.

Las funciones [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) y [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) son exclusivas del inicio de sesión único (SSO).



| Nombre                                                                                                             | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Pedido llamado |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Obtiene los campos de entrada de los componentes de interfaz de usuario interactivos que se van a generar en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Permite al usuario determinar qué tipo de credenciales requieren los métodos para realizar la autenticación en un escenario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Convierte la información de usuario en un BLOB de usuario que pueden usar las funciones de tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Obtiene un BLOB de credencial que se puede usar para iniciar la autenticación desde la entrada del usuario recibida por la interfaz de usuario de SSO.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | El suplicante utiliza la marca de **\_ Inicio de \_ \_ sesión previo de la marca EAP** para indicar que EAPHost debe proporcionar SSO. Si se devuelve el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) , EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Si no se devuelve el código de acción [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) , EAPHost continúa con la secuencia de llamadas normal y no SSO. Para obtener más información, consulte [secuencia de llamadas a la API del suplicante](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API de método del mismo nivel de EAPHost

Las siguientes funciones del mismo nivel admiten SSO.

Las funciones [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) y [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) son exclusivas del inicio de sesión único (SSO).



| Nombre                                                                                                      | Propósito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Pedido llamado |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define la implementación de una API de método EAP que proporciona los campos de entrada para que los componentes de interfaz de usuario interactivas se generen en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define la implementación de una función específica del método EAP que obtiene los campos de entrada de credenciales de SSO de EAP para ese método EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convierte la información de usuario en un BLOB de usuario que pueden usar las funciones de tiempo de ejecución de EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define la implementación de una función de método EAP que obtiene los datos de BLOB de usuario proporcionados por la interfaz de usuario de SSO interactiva generada en el suplicante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | La marca de **\_ Inicio de \_ \_ sesión previo de la marca EAP** indica que EAPHost debe proporcionar SSO. En un escenario de SSO si se devuelve el código de acción **EapPeerResponseInvokeUI** , EAPHost llama a [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)y, a continuación, llama a [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Si no se devuelve el código de acción **EapPeerResponseInvokeUI** , EAPHost continúa con la secuencia de llamadas normal y no SSO. Para obtener más información, vea [secuencia de llamadas API de método del mismo nivel](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Escenarios de EAPHost de SSO](why-eaphost-sso.md)
</dt> </dl>

 

