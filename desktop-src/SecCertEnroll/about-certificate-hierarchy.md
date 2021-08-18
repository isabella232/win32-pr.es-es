---
description: A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede ser difícil que una única entidad de certificación (CA) realice un seguimiento eficaz de los certificados que ha emitido.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Jerarquía de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904985"
---
# <a name="certificate-hierarchy"></a>Jerarquía de certificados

A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede ser difícil que una única entidad de certificación (CA) realice un seguimiento eficaz de los certificados que ha emitido. Una manera de solucionar este problema es crear una jerarquía de certificados en la que la entidad de certificación delegue la autoridad para emitir certificados a las autoridades subordinadas que, a su vez, puedan delegar la autoridad a sus subordinados. Cada entidad de certificación delega la autoridad mediante la emisión de un certificado de entidad de certificación a un subordinado. La entidad de certificación inicial de la cadena se denomina raíz y no es necesario que [](about-certificate-chain.md) una entidad establezca la confianza con ninguna entidad de certificación que resida en una cadena de certificados diferente de la en la que reside la entidad.

En la ilustración siguiente se muestra una jerarquía de certificados que se conste de una CA raíz, dos CA subordinadas a la raíz (una para el departamento de marketing y otra para el departamento de fabricación) y ca que están subordinadas a estas.

![diagrama de jerarquía de certificados](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



