---
description: A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede resultar difícil para una sola entidad de certificación (CA) realizar un seguimiento eficaz de los certificados emitidos.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Jerarquía de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570263"
---
# <a name="certificate-hierarchy"></a>Jerarquía de certificados

A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede resultar difícil para una sola entidad de certificación (CA) realizar un seguimiento eficaz de los certificados emitidos. Una manera de solucionar este problema consiste en crear una jerarquía de certificados en la que la entidad de certificación delegue la autoridad para emitir certificados a entidades subordinadas que, a su vez, pueden delegar la autoridad a sus subordinadas. Cada entidad de certificación delega la autoridad mediante la emisión de un certificado de entidad de certificación a un subordinado. La entidad de certificación inicial de la cadena se denomina raíz y no es necesario que una entidad establezca confianza con cualquier CA que resida en una [cadena de certificados](about-certificate-chain.md) diferente de la en la que reside la entidad.

En la ilustración siguiente se muestra una jerarquía de certificados formada por una CA raíz, dos entidades de certificación subordinadas a la raíz (una para el Departamento de marketing y otra para el Departamento de fabricación) y las CA subordinadas a ellas.

![diagrama de jerarquía de certificados](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de confianza](about-trust-models.md)
</dt> </dl>

 

 



