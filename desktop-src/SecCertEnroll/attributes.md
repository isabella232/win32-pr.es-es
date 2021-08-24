---
description: 'Atributos (API de inscripción de certificados): se pueden agregar atributos a una solicitud de certificado para proporcionar una entidad de certificación (CA) con información adicional que puede usar al crear y emitir un certificado.'
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Atributos (API de inscripción de certificados)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aec93ec47a700902cb1275e25af6649e6988b76f7204b01487249e0130dd35b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903107"
---
# <a name="attributes-certificate-enrollment-api"></a>Atributos (API de inscripción de certificados)

Los atributos se pueden agregar a una solicitud de certificado para proporcionar una entidad de certificación (CA) con información adicional que puede usar al crear y emitir un certificado. Cada atributo es una estructura de [*notación*](/windows/desktop/SecGloss/d-gly) de sintaxis abstracta (ASN.1) codificada por reglas de codificación distinguida (DER) que contiene un identificador de objeto (OID) y cero o más valores. [](/windows/desktop/SecGloss/a-gly) Los atributos se definen mediante interfaces incluidas con la API de inscripción de certificados. En los temas siguientes se tratan los atributos con más detalle:

-   [Atributos compatibles](supported-attributes.md)
-   [Arquitectura de atributos](attribute-architecture.md)
-   [Atributos PKCS \# 7](pkcs--7-attributes.md)
-   [Atributos PKCS \# 10](pkcs--10-attributes.md)
-   [Atributos de CMC](cmc-attributes.md)

 

 
