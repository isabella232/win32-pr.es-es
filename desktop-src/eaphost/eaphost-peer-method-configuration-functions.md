---
title: Funciones de configuración del método del mismo nivel eaphost
description: Obtenga información sobre las funciones de configuración del método del mismo nivel de EAPHost. Consulte una lista de las funciones de configuración y vea los recursos disponibles adicionales.
ms.assetid: ba5c90b2-5185-4810-84a2-d08e62e8105c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3081f8a54482c48c7c506a25bfaf7f18cf3193ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252921"
---
# <a name="eaphost-peer-method-configuration-functions"></a>Funciones de configuración del método del mismo nivel eaphost

Las funciones de configuración de EAP Peer Method API son las siguientes.



| Función                                                                                                  | Descripción                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerConfigBlob2Xml**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigblob2xml)                                                    | Convierte el blob de configuración en XML.                                                                                                                                                                                                                          |
| [**EapPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerconfigxml2blob)                                                    | Convierte XML en el blob de configuración.                                                                                                                                                                                                                        |
| [**EapPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeercredentialsxml2blob)                                          | Convierte las credenciales XML en un BLOB.                                                                                                                                                                                                                            |
| [**EapPeerFreeErrorMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory)                                                  | Libera toda la memoria específica del error de EAP devuelta por las API del mismo nivel de EapHost.                                                                                                                                                                                               |
| [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)                                                            | Libera toda la memoria asignada por los parámetros OUT del método EAP.                                                                                                                                                                                                      |
| [**EapPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui)                                                    | Genera el cuadro de diálogo de interfaz de usuario de configuración de conexión específica del método EAP en el cliente.                                                                                                                                                                   |
| [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui)                                                | Genera un cuadro de diálogo de interfaz de usuario interactiva personalizada para obtener información de identidad de usuario para el método EAP en el cliente.                                                                                                                                          |
| [**EapPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui)                                          | Genera un cuadro de diálogo de interfaz de usuario interactiva personalizada para el método EAP en el cliente.                                                                                                                                                                              |
| [**EapPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Define la implementación de una función específica del método EAP que obtiene los campos de entrada de credenciales de inicio de sesión único (SSO) de EAP para ese método EAP.                                                                                                              |
| [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Define la implementación de una función de suplicación eap que obtiene los campos de entrada para los componentes de interfaz de usuario interactivos que se deben generar en el suplicante.                                                                                                     |
| [**EapPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Convierte la información del usuario en un BLOB de usuario que pueden consumir las funciones en tiempo de ejecución de EAPHost.                                                                                                                                                                   |
| [**EapPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Define la implementación de una función específica del método EAP que genera un blob de credenciales de usuario eap a partir de una estructura [**EAP CONFIG INPUT FIELD \_ \_ \_ \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) que contiene datos de credenciales proporcionados por un usuario suplicante. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones del método del mismo nivel EAPHost Run-Time](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




