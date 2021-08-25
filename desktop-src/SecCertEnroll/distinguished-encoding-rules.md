---
description: La notación de sintaxis abstracta Uno (ASN.1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre equipos.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: reglas de codificación distinguida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d592fdfbb2532f5c718aadaaf32e63f352ed6ab427e9908465fcb5998839f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883075"
---
# <a name="distinguished-encoding-rules"></a>reglas de codificación distinguida

La notación de sintaxis abstracta Uno (ASN.1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre equipos.

-   Reglas básicas de codificación (BER)
-   Reglas de codificación canónica (CER)
-   reglas de codificación distinguida (DER)
-   Reglas de codificación empaquetadas (PER)

El conjunto de reglas original se definió mediante la especificación BER. CER y DER se desarrollaron más adelante como subconjuntos especializados de BER. PER se desarrolló en respuesta a reprobaciones sobre la cantidad de ancho de banda necesaria para transmitir datos mediante BER o sus variantes. PER proporciona un ahorro significativo.

DER se creó para satisfacer los requisitos de la especificación X.509 para la transferencia de datos segura. La API de inscripción de certificados usa DER exclusivamente. Para obtener más información, vea los temas siguientes:

-   [Sintaxis de transferencia de DER](about-der-transfer-syntax.md)
-   [Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación de solicitudes de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Introducción a la sintaxis y codificación de ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



