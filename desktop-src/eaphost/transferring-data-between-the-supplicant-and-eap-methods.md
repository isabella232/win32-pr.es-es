---
title: Transferencia de datos entre el suplicante y los métodos EAP
description: Obtenga información acerca de la transferencia de datos entre el suplicante y los métodos EAP. La transferencia de datos entre métodos se logra mediante el uso de atributos EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421423"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Transferencia de datos entre el suplicante y los métodos EAP

El uso de atributos EAP permite intercambiar datos entre suplicantes y métodos EAP.

## <a name="attribute-consumption"></a>Consumo de atributos

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consume atributos EAP que se pasan directamente al método EAP configurado. Del mismo modo, los métodos EAP pueden devolver un código de acción que indica al suplicante que los atributos están disponibles y que debe recopilar los atributos mediante [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Para obtener más información, vea los siguientes temas.

-   [Códigos de acción de suplicante EAP del mismo nivel](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Códigos de motivo del suplicante de EAP del mismo nivel](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Códigos de acción del método de autenticador de EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Se espera que los suplicantes omitan los atributos que no reconocen o en los que no puede actuar. El uso de [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) estos atributos omitidos se envían de vuelta a EAPHost y al método EAP.

## <a name="vendor-specific-attributes"></a>Atributos específicos del proveedor

Mediante el uso del atributo EAP específico del proveedor, los métodos y suplicantes EAP pueden interactuar en el intercambio de datos para un propósito específico. Los suplicantes y los métodos que no admiten el atributo específico del proveedor omiten los atributos específicos del proveedor.

Para obtener más información, vea los siguientes temas.

-   [Atributos EAP](about-eap-attributes.md).
-   [**EAP \_ de \_tipo de atributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la interfaz de usuario del método EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementación de la compatibilidad de In-Band NAP con métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Suplicantes de EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




