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
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118433"
---
# <a name="attributes-certificate-enrollment-api"></a>Atributos (API de inscripción de certificados)

Los atributos se pueden agregar a una solicitud de certificado para proporcionar una entidad de certificación (CA) con información adicional que puede usar al crear y emitir un certificado. Cada atributo es una [*estructura*](/windows/desktop/SecGloss/d-gly) de notación [](/windows/desktop/SecGloss/a-gly) de sintaxis abstracta (ASN.1) codificada por reglas de codificación distinguida (DER) que contiene un identificador de objeto (OID) y cero o más valores. Los atributos se definen mediante interfaces incluidas con la API de inscripción de certificados. En los temas siguientes se tratan los atributos con más detalle:

-   [Atributos compatibles](supported-attributes.md)
-   [Arquitectura de atributos](attribute-architecture.md)
-   [Atributos PKCS \# 7](pkcs--7-attributes.md)
-   [Atributos PKCS \# 10](pkcs--10-attributes.md)
-   [Atributos de CMC](cmc-attributes.md)

 

 
