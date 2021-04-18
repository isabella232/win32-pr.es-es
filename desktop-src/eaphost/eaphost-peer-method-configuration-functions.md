---
title: Funciones de configuración del método del mismo nivel de EAPHost
description: Obtenga información sobre las funciones de configuración de métodos del mismo nivel de EAPHost. Vea una lista de las funciones de configuración y vea los recursos adicionales disponibles.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695756"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funciones de configuración del método del mismo nivel de EAPHost

Las funciones de configuración de la API del método EAP del mismo nivel son las siguientes.



| Función                                                                                                  | Descripción                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Convierte el BLOB de configuración en XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Convierte XML en el BLOB de configuración.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Convierte las credenciales XML en un BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera toda la memoria específica del error de EAP devuelta por las API del mismo nivel de EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Libera toda la memoria asignada por los parámetros OUT del método EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Genera el cuadro de diálogo de la interfaz de usuario de configuración de conexión específica del método EAP en el cliente.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Genera un cuadro de diálogo de interfaz de usuario interactivo personalizado para obtener información de identidad de usuario para el método EAP en el cliente.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Genera un cuadro de diálogo de interfaz de usuario interactivo personalizado para el método EAP en el cliente.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define la implementación de una función específica del método EAP que obtiene los campos de entrada de credenciales de inicio de sesión único (SSO) de EAP para ese método EAP                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define la implementación de una función de suplicante EAP que obtiene los campos de entrada de los componentes de interfaz de usuario interactivos que se van a elevar en el suplicante.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convierte la información de usuario en un BLOB de usuario que pueden usar las funciones de tiempo de ejecución de EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define la implementación de una función específica del método EAP que genera un BLOB de credenciales de usuario de EAP a partir de una estructura de matriz de campos de entrada de configuración de EAP que contiene los datos de credenciales proporcionados por un usuario solicitante. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones Run-Time del método del mismo nivel](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




