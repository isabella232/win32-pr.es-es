---
title: Estructuras de métodos del mismo nivel de EAPHost
description: Obtenga información sobre las estructuras de API del método del mismo nivel de EAPHost, como EapCertificateCredential y EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252981"
---
# <a name="eaphost-peer-method-structures"></a>Estructuras de métodos del mismo nivel de EAPHost

Las estructuras de API del método del mismo nivel de EAPHost son las siguientes.



| Estructura                                                              | Descripción                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contiene información sobre el certificado que usa el método EAP para la autenticación.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contiene información sobre el tipo de credenciales y las credenciales adecuadas. Esto se pasa como entrada a la API [**EapPeerGetConfigBlobAndUserBlob.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) |
| [**RUTINAS \_ DEL MÉTODO DEL MISMO NIVEL \_ \_ DE EAP**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contiene un conjunto de punteros de función a las API del método del mismo nivel de EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contiene la información de acción devuelta por un método del mismo nivel eap.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contiene los datos de resultados generados por un método EAP durante la autenticación.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contiene información sobre la SIM que usa el método EAP para la autenticación.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contiene el nombre de usuario y la contraseña que usa el método EAP para autenticar al usuario.                                                                                                     |



 

 

 




