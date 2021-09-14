---
description: En una PKI de Microsoft, las solicitudes de certificado se envían desde equipos cliente a entidades de certificación (CA) como una cadena binaria que contiene una secuencia de estructuras de datos codificadas.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificación de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173349"
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

 

 



