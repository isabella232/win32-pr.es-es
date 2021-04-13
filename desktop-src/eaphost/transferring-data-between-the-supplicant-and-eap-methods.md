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
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="e871f-104">Transferencia de datos entre el suplicante y los métodos EAP</span><span class="sxs-lookup"><span data-stu-id="e871f-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="e871f-105">El uso de atributos EAP permite intercambiar datos entre suplicantes y métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="e871f-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="e871f-106">Consumo de atributos</span><span class="sxs-lookup"><span data-stu-id="e871f-106">Attribute Consumption</span></span>

<span data-ttu-id="e871f-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consume atributos EAP que se pasan directamente al método EAP configurado.</span><span class="sxs-lookup"><span data-stu-id="e871f-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="e871f-108">Del mismo modo, los métodos EAP pueden devolver un código de acción que indica al suplicante que los atributos están disponibles y que debe recopilar los atributos mediante [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="e871f-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="e871f-109">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="e871f-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="e871f-110">[Códigos de acción de suplicante EAP del mismo nivel](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="e871f-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="e871f-111">[Códigos de motivo del suplicante de EAP del mismo nivel](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="e871f-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="e871f-112">[Códigos de acción del método de autenticador de EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="e871f-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="e871f-113">Se espera que los suplicantes omitan los atributos que no reconocen o en los que no puede actuar.</span><span class="sxs-lookup"><span data-stu-id="e871f-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="e871f-114">El uso de [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) estos atributos omitidos se envían de vuelta a EAPHost y al método EAP.</span><span class="sxs-lookup"><span data-stu-id="e871f-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="e871f-115">Atributos específicos del proveedor</span><span class="sxs-lookup"><span data-stu-id="e871f-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="e871f-116">Mediante el uso del atributo EAP específico del proveedor, los métodos y suplicantes EAP pueden interactuar en el intercambio de datos para un propósito específico.</span><span class="sxs-lookup"><span data-stu-id="e871f-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="e871f-117">Los suplicantes y los métodos que no admiten el atributo específico del proveedor omiten los atributos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e871f-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="e871f-118">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="e871f-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="e871f-119">[Atributos EAP](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e871f-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="e871f-120">[**EAP \_ de \_tipo de atributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="e871f-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e871f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e871f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e871f-122">Configuración de la interfaz de usuario del método EAP</span><span class="sxs-lookup"><span data-stu-id="e871f-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="e871f-123">Habilitar directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="e871f-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="e871f-124">Implementación de la compatibilidad de In-Band NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="e871f-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="e871f-125">Implementación de la compatibilidad de NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="e871f-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="e871f-126">Suplicantes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="e871f-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




