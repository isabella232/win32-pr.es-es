---
description: Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una entidad de certificación (CA) información adicional que puede utilizar al crear y emitir un certificado.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811263"
---
# <a name="attributes-certificate-enrollment-api"></a>Atributos (API de inscripción de certificados)

Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una entidad de certificación (CA) información adicional que puede utilizar al crear y emitir un certificado. Cada atributo es una estructura de [*notación de sintaxis abstracta*](/windows/desktop/SecGloss/a-gly) (ASN. 1) codificada en [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der) que contiene un identificador de objeto (OID) y cero o más valores. Los atributos se definen mediante interfaces que se incluyen con la API de inscripción de certificados. En los temas siguientes se describen los atributos con más detalle:

-   [Atributos compatibles](supported-attributes.md)
-   [Arquitectura de atributo](attribute-architecture.md)
-   [\#Atributos PKCS 7](pkcs--7-attributes.md)
-   [\#Atributos PKCS 10](pkcs--10-attributes.md)
-   [Atributos de CMC](cmc-attributes.md)

 

 
