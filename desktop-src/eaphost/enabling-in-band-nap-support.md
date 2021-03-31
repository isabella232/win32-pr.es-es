---
title: Implementación de la compatibilidad de In-Band NAP con métodos EAP
description: Se puede habilitar para los métodos EAP de EAPHost que admiten la transmisión de objetos de tipo-longitud-valor (TLVs).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797110"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementación de la compatibilidad de In-Band NAP con métodos EAP

La compatibilidad con la [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP) en banda para un método EAP se puede habilitar para los métodos EAP de EAPHost que admiten la transmisión de objetos de tipo longitud-valor (TLVs). Cuando está habilitada la compatibilidad con NAP en banda, los paquetes NAP se transportan dentro de paquetes de método EAP.

Por el contrario, cuando la compatibilidad de NAP fuera de banda está habilitada, el intercambio del [Informe de mantenimiento](https://go.microsoft.com/fwlink/p/?linkid=83917) (SOH) de NAP se produce a través de medios distintos de los paquetes de métodos internos a EAP.

Todos los TLVs son específicos del proveedor.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementación de la compatibilidad con NAP en métodos EAP del mismo nivel

La implementación del método del mismo nivel de EAP recibe un TLV que contiene el TLV [de solicitud del informe de mantenimiento](https://go.microsoft.com/fwlink/p/?linkid=83917) (SOH) de un servidor EAP.

A continuación, la implementación del método EAP peer pasa el TLV que contiene el TLV de solicitud de SoH a EAPHost como se indica a continuación.

-   La implementación del método EAP peer devuelve el código de acción [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) a EAPHost en la devolución de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost llama a [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) desde la implementación del método EAP del mismo nivel. Los atributos se pasan en el proceso.
-   La implementación del método EAP peer devuelve el TLV que contiene el TLV de solicitud de SoH en [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Los atributos se reciben en el proceso.

La implementación del método EAP peer recibe un TLV que contiene un TLV de SoH de EAPHost, como se indica a continuación.

-   EAPHost llama a [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) desde la implementación del método EAP del mismo nivel. **EapPeerSetResponseAttributes** contiene un TLV que hospeda un TLV de SOH.
-   La implementación del método EAP peer envía el TLV de SoH al servidor EAP.
-   La implementación del método EAP peer recibe un TLV que contiene un TLV de respuesta de SoH del servidor EAP.

La implementación del método EAP peer pasa el TLV que contiene el TLV de respuesta de SoH a EAPHost como se indica a continuación.

-   La implementación del método EAP peer devuelve el código de acción **EapPeerMethodResponseActionRespond** a EAPHost en la devolución de [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost llama a [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) desde las implementaciones de método EAP del mismo nivel. La estructura de [**\_ atributos EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) se pasa en el proceso.
-   La implementación del método EAP peer devuelve el TLV que contiene el TLV de respuesta de SoH en [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> El miembro **eapType** de la estructura del [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) siempre se establecerá en **eatEAPTLV** y el miembro **pValue** apuntará al primer byte del TLV que contenga el TLV de respuesta de SOH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementación de la compatibilidad de NAP en métodos de servidor EAP

La implementación del método de servidor EAP crea un TLV que contiene un TLV de solicitud SoH. La implementación del método de servidor EAP envía este TLV que contiene el TLV de solicitud de SoH al elemento EAP del mismo nivel. La implementación del método de servidor EAP recibe el TLV del EAP del mismo nivel.

La implementación del método de servidor EAP pasa el TLV que contiene un TLV de SoH a EAPHost como se indica a continuación.

-   La implementación del método de servidor EAP devuelve la **\_ respuesta del \_ autenticador del método \_ \_ EAP** del código de acción responder a EAPHost en la devolución de [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost llama a [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) desde la implementación del método de servidor EAP.
-   La implementación del método de servidor EAP devuelve el TLV que contiene el TLV de SoH en [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

La implementación del método de servidor EAP recibe un TLV que contiene un TLV de respuesta de SoH de EAPHost, como se indica a continuación.

-   EAPHost llama a [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) desde la implementación del método de servidor EAP.
-   El TLV que contiene el TLV de respuesta de SoH se devuelve en [ **EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   La implementación del método de servidor EAP envía el TLV que contiene el TLV de respuesta de SoH.

> [!Note]  
> El miembro **eapType** de la estructura del [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) siempre se establecerá en **eatEAPTLV** y el miembro **pValue** apuntará al primer byte del TLV que contenga el TLV de respuesta de SOH.

 

### <a name="messages"></a>error de Hadoop

El TLV EAP SoH se usa para encapsular el protocolo SoH para la transmisión a través de un método EAP. All EAP SoH TLVs tiene la misma estructura, que solo se diferencia en el identificador de mensaje y en la parte de datos del mensaje.

Para obtener más información, consulte [mensajes del informe de mantenimiento (SOH) de protección de acceso a redes (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la interfaz de usuario del método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transferencia de datos entre el suplicante y los métodos EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 