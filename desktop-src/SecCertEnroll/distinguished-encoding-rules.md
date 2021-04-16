---
description: La notación de sintaxis abstracta uno (ASN. 1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre los equipos.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: reglas de codificación distinguida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542694"
---
# <a name="distinguished-encoding-rules"></a>reglas de codificación distinguida

La notación de sintaxis abstracta uno (ASN. 1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre los equipos.

-   Reglas de codificación básicas (BER)
-   Reglas de codificación canónica (CER)
-   Reglas de codificación distinguida (DER)
-   Reglas de codificación empaquetadas (por)

El conjunto de reglas original se definió mediante la especificación BER. CER y DER se desarrollaron más adelante como subconjuntos especializados de BER. POR se desarrolló en respuesta a críticas sobre la cantidad de ancho de banda necesario para transmitir datos mediante BER o sus variantes. POR proporciona un ahorro significativo.

Se creó DER para satisfacer los requisitos de la especificación X. 509 para la transferencia de datos segura. La API de inscripción de certificados usa DER exclusivamente. Para obtener más información, vea los siguientes temas.

-   [Sintaxis de transferencia DER](about-der-transfer-syntax.md)
-   [Codificación DER de tipos ASN. 1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipos ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación de solicitud de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Introducción a la codificación y sintaxis de ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



