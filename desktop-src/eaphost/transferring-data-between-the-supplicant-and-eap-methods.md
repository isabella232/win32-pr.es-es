---
title: Transferencia de datos entre los métodos supplicant y EAP
description: Obtenga información sobre la transferencia de datos entre los métodos Supplicant y EAP. La transferencia de datos entre métodos se realiza mediante atributos eap.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085656"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Transferencia de datos entre los métodos supplicant y EAP

El uso de atributos eap permite intercambiar datos entre los suplicantes y los métodos EAP.

## <a name="attribute-consumption"></a>Consumo de atributos

[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consume atributos de EAP que se pasan directamente al método EAP configurado. Del mismo modo, los métodos EAP son libres de devolver un código de acción que indica al suplicante que los atributos están disponibles y que debe recopilar los atributos mediante [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Para obtener más información, vea los temas siguientes:

-   [Códigos de acción de suplicación del mismo nivel de EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Códigos de motivo de suplicación del mismo nivel de EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [Eap Authenticator códigos de acción del método](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Se espera que los suplicantes ignoren los atributos que no reconocen o sobre los que no pueden actuar. Con [**EapHostPeerSetResponseAttributes,**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) estos atributos omitido se devuelven a EAPHost y al método EAP.

## <a name="vendor-specific-attributes"></a>Atributos específicos del proveedor

Mediante el uso del atributo EAP específico del proveedor, los métodos EAP y los suplicantes pueden participar en el intercambio de datos para un propósito específico. Los suplicadores y métodos que no admiten el atributo específico del proveedor omiten los atributos específicos del proveedor.

Para obtener más información, vea los temas siguientes:

-   [Atributos de EAP](about-eap-attributes.md).
-   [**EAP \_ TIPO \_ DE ATRIBUTO**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del método EAP Interfaz de usuario](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Habilitar directiva de grupo](enabling-group-policy.md)
</dt> <dt>

[Implementar la compatibilidad In-Band NAP para los métodos EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementación de la compatibilidad de NAP con métodos EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




