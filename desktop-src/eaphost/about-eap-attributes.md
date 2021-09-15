---
title: Atributos de EAP
description: Es una estructura \_ EAP ATTRIBUTE que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568900"
---
# <a name="eap-attributes"></a>Atributos de EAP

Un atributo EAP es una estructura [**\_ EAP ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación. Los atributos se usan para comunicar información entre métodos eap y suplicantes o entre métodos EAP y autenticadores. Las implementaciones del mismo nivel y autenticador de un método EAP pueden intercambiar estos atributos a través de una red.

Aparece una lista completa de los tipos de atributo admitidos en el tema [**EAP \_ ATTRIBUTE \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Atributos consumidos por los suplicantes

Los siguientes tipos de atributo los consumen los suplicantes 802.1X.

-   **eatVendorSpecific**

Los siguientes tipos de atributo los consumen los suplicadores de cliente PPP.

-   **eatMinimum**
-   **consumeEAPTLV**

Los siguientes tipos de atributo los consumen los suplicadores de servidor PPP.

-   **nombreDeUsuario de la base de datos**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **consumeEAPMessage**

## <a name="attributes-exported-by-methods"></a>Atributos exportados por métodos

Los métodos EAP podrían exportar los siguientes tipos de atributo.

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

Los métodos de seguridad de nivel de transporte [(TLS) de EAP (EAP-TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) exportan el siguiente tipo de atributo.

-   **eatCertificateOID**

Los siguientes tipos de atributo se exportan mediante los métodos del Protocolo de autenticación de desafío de Microsoft versión [2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).

-   **nombreDeUsuario de la base de datos**
-   **lugar De CredencialChanged**

El servidor de directivas de red (NPS) consume el siguiente tipo de atributo.

-   **eatCertificateOID**

Los siguientes tipos de atributo se exportan mediante métodos del Protocolo de autenticación [extensible protegido (PEAP).](/previous-versions/windows/embedded/ms899190(v=msdn.10))

-   **nombreDeUsuario de la base de datos**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**TIPO DE \_ ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 