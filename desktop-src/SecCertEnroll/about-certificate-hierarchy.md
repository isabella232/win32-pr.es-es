---
description: A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede ser difícil que una única entidad de certificación (CA) realice un seguimiento eficaz de los certificados que ha emitido.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Jerarquía de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173353"
---
# <a name="certificate-hierarchy"></a>Jerarquía de certificados

A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede ser difícil que una única entidad de certificación (CA) realice un seguimiento eficaz de los certificados que ha emitido. Una manera de solucionar este problema es crear una jerarquía de certificados en la que la entidad de certificación delegue la autoridad para emitir certificados a las autoridades subordinadas que, a su vez, puedan delegar la autoridad a sus subordinados. Cada entidad de certificación delega la autoridad mediante la emisión de un certificado de entidad de certificación a un subordinado. La entidad de certificación inicial de la cadena se denomina raíz y no es necesario que [](about-certificate-chain.md) una entidad establezca la confianza con ninguna entidad de certificación que resida en una cadena de certificados diferente de la en la que reside la entidad.

En la ilustración siguiente se muestra una jerarquía de certificados que se conste de una CA raíz, dos CA subordinadas a la raíz (una para el departamento de marketing y otra para el departamento de fabricación) y ca que están subordinadas a estas.

![diagrama de jerarquía de certificados](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



