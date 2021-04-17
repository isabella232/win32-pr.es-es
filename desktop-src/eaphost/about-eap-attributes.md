---
title: Atributos EAP
description: Es una \_ estructura de atributo EAP que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105714503"
---
# <a name="eap-attributes"></a>Atributos EAP

Un atributo EAP es una estructura de [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación. Los atributos se utilizan para comunicar información entre los métodos y suplicantes EAP o entre los métodos EAP y los autenticadores. Las implementaciones del mismo nivel y autenticador de un método EAP pueden intercambiar estos atributos a través de una red.

En el tema [**\_ \_ tipo de atributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)se muestra una lista completa de los tipos de atributos admitidos.

## <a name="attributes-consumed-by-supplicants"></a>Atributos utilizados por suplicantes

Los suplicantes de 802.1 X consumen los siguientes tipos de atributos.

-   **eatVendorSpecific**

Los suplicantes de cliente PPP consumen los siguientes tipos de atributos.

-   **eatMinimum**
-   **eatEAPTLV**

Los suplicantes del servidor PPP consumen los siguientes tipos de atributos.

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>Atributos exportados por métodos

Los métodos EAP pueden exportar los siguientes tipos de atributos.

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

Los métodos de [seguridad de nivel de transporte (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) de EAP exportan el siguiente tipo de atributo.

-   **eatCertificateOID**

Los siguientes tipos de atributo se exportan mediante los métodos de la versión 2,0 (MS-CHAPv2) del [Protocolo de autenticación por desafío mutuo de Microsoft](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .

-   **eatUserName**
-   **eatCredentialsChanged**

El tipo de atributo siguiente lo consume el servidor de directivas de redes (NPS).

-   **eatCertificateOID**

Los métodos del [Protocolo de autenticación extensible protegido (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportan los siguientes tipos de atributos.

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**\_tipo de atributo EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 