---
description: En una PKI de Microsoft, las solicitudes de certificado se envían desde equipos cliente a entidades de certificación (CA) como una cadena binaria que contiene una secuencia de estructuras de datos codificadas.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificación de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6bb65b496264fcd1f9667416c78d5d8cf246f1c9aa4cf736990a1f61669f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904854"
---
# <a name="certificate-request-encoding"></a>Codificación de solicitud de certificado

En una PKI de Microsoft, las solicitudes de certificado se envían desde equipos cliente a entidades de certificación (CA) como una cadena binaria que contiene una secuencia de estructuras de datos codificadas. La API de inscripción de certificados usa la notación de sintaxis abstracta One (ASN.1) para describir y codificar estas estructuras. Para los fines de esta documentación, ASN.1 se puede dividir conceptualmente en las reglas de sintaxis (ISO 8824) que describen las estructuras de datos y las reglas de codificación (ISO 8825) que especifican cómo se codificarán los datos para la transmisión de red. Para obtener más información, vea los temas siguientes:

-   [Introducción a la sintaxis y codificación de ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Sistema de tipo ASN.1](about-asn-1-type-system.md)
-   [reglas de codificación distinguida](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



