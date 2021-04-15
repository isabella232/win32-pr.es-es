---
title: Estructuras de método del mismo nivel de EAPHost
description: Obtenga información sobre las estructuras de API de método del mismo nivel de EAPHost, como EapCertificateCredential y EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695760"
---
# <a name="eaphost-peer-method-structures"></a>Estructuras de método del mismo nivel de EAPHost

Las estructuras de API del método del mismo nivel de EAPHost son las siguientes.



| Estructura                                                              | Descripción                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contiene información sobre el certificado que el método EAP utiliza para la autenticación.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contiene información sobre el tipo de credenciales y las credenciales adecuadas. Esto se pasa como una entrada a la API de [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) . |
| [**\_ \_ rutinas de método EAP del mismo nivel \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contiene un conjunto de punteros de función a las API de método del mismo nivel de EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contiene la información de la acción devuelta por un método EAP del mismo nivel.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contiene los datos de resultado generados por un método EAP durante la autenticación.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contiene información sobre la tarjeta SIM utilizada por el método EAP para la autenticación.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contiene el nombre de usuario y la contraseña que usa el método EAP para autenticar al usuario.                                                                                                     |



 

 

 




