---
title: Implementar la compatibilidad In-Band NAP para métodos EAP
description: Se puede habilitar para los métodos EAP de EAP de EAPHost que admiten la transmisión de objetos de valor de longitud de tipo (TLV).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477ad8f2ee033b3f98f9cac0e7ee34d18dc62f00dd5bd7c0e09509ad32bcfa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904281"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementar la compatibilidad In-Band NAP para métodos EAP

La compatibilidad [con](/windows/desktop/NAP/network-access-protection-start-page) protección de acceso a redes (NAP) en banda para un método EAP se puede habilitar para los métodos EAP de EAP de EAPHost que admiten la transmisión de objetos de valor de longitud de tipo (TLV). Cuando se habilita la compatibilidad con NAP en banda, los paquetes NAP se transportan dentro de paquetes de método EAP.

Por el contrario, cuando se habilita la compatibilidad [](https://go.microsoft.com/fwlink/p/?linkid=83917) con NAP fuera de banda, el intercambio de la declaración de mantenimiento (SoH) de NAP se produce a través de medios distintos de los paquetes de método interno a EAP.

Todos los TLV son específicos del proveedor.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementación de la compatibilidad con NAP en métodos del mismo nivel de EAP

La implementación del método del mismo [](https://go.microsoft.com/fwlink/p/?linkid=83917) nivel de EAP recibe un TLV que contiene la TLV de solicitud de instrucción de mantenimiento (SoH) de un servidor EAP.

A continuación, la implementación del método del mismo nivel de EAP pasa el TLV que contiene la TLV de solicitud de SoH a EAPHost como se muestra a continuación.

-   La implementación del método del mismo nivel de EAP devuelve el código de acción [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) a EAPHost al devolver [**desde EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost llama [**a EapPeerGetResponseAttributes desde**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) la implementación del método del mismo nivel de EAP. Los atributos se pasan en el proceso.
-   La implementación del método del mismo nivel de EAP devuelve el TLV que contiene la TLV de solicitud soH [**en EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Los atributos se reciben en el proceso.

La implementación del método del mismo nivel de EAP recibe un TLV que contiene un TLV de SoH de EAPHost como se muestra a continuación.

-   EAPHost llama [**a EapPeerSetResponseAttributes desde**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) la implementación del método del mismo nivel de EAP. **EapPeerSetResponseAttributes** contiene un TLV que aloja un TLV de SoH.
-   La implementación del método del mismo nivel de EAP envía el TLV de SoH al servidor EAP.
-   La implementación del método del mismo nivel de EAP recibe un TLV que contiene un TLV de respuesta de SoH del servidor EAP.

La implementación del método del mismo nivel de EAP pasa el TLV que contiene la TLV de respuesta de SoH a EAPHost como se muestra a continuación.

-   La implementación del método del mismo nivel de EAP devuelve el código de acción **EapPeerMethodResponseActionRespond** a EAPHost al devolver [**desde EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost llama [**a EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) desde las implementaciones del método del mismo nivel de EAP. La [**estructura EAP \_ ATTRIBUTES**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) se pasa en el proceso.
-   La implementación del método del mismo nivel de EAP devuelve el TLV que contiene la TLV de respuesta de SoH [**en EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> El **miembro eapType** de la estructura [**EAP \_ ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) siempre se establecerá en **byteEAPTLV** y el miembro **pValue** apuntará al primer byte de la TLV que contiene la TLV de respuesta de SoH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementación de la compatibilidad con NAP en métodos de servidor EAP

La implementación del método de servidor EAP construye un TLV que contiene un TLV de solicitud de SoH. La implementación del método del servidor EAP envía este TLV que contiene la TLV de solicitud de SoH al par EAP. La implementación del método del servidor EAP recibe el TLV del mismo nivel de EAP.

La implementación del método de servidor EAP pasa el TLV que contiene un TLV de SoH a EAPHost como se muestra a continuación.

-   La implementación del método de servidor EAP devuelve el código de acción **EAP METHOD AUTHENTICATOR RESPONSE \_ \_ \_ \_ RESPOND** to EAPHost al devolver [**desde EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost llama [**a EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) desde la implementación del método de servidor EAP.
-   La implementación del método de servidor EAP devuelve el TLV que contiene el TLV de SoH [**en EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

La implementación del método de servidor EAP recibe un TLV que contiene un TLV de respuesta de SoH de EAPHost como se muestra a continuación.

-   EAPHost llama [**a EapMethodAuthenticatorSetAttributes desde**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) la implementación del método de servidor EAP.
-   El TLV que contiene la TLV de respuesta de SoH se devuelve [ **en EapMethodAuthenticatorSetAttributes.**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   La implementación del método de servidor EAP envía el TLV que contiene la TLV de respuesta de SoH.

> [!Note]  
> El **miembro eapType** de la estructura [**EAP \_ ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) siempre se establecerá en **byteEAPTLV** y el miembro **pValue** apuntará al primer byte de la TLV que contiene la TLV de respuesta de SoH.

 

### <a name="messages"></a>error de Hadoop

Eap SoH TLV se usa para encapsular el protocolo SoH para su transmisión a través de un método EAP. Todos los TLV de EAP SoH tienen la misma estructura, que difiere solo en el identificador del mensaje y la parte de datos del mensaje.

Para obtener más información, vea Mensajes de declaración de mantenimiento [(SoH) de](https://go.microsoft.com/fwlink/p/?linkid=83918)Protección de acceso a redes (NAP).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del método EAP Interfaz de usuario](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre los métodos supplicant y EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 