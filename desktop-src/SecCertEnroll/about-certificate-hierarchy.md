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
# <a name="certificate-hierarchy"></a><span data-ttu-id="07190-103">Jerarquía de certificados</span><span class="sxs-lookup"><span data-stu-id="07190-103">Certificate Hierarchy</span></span>

<span data-ttu-id="07190-104">A medida que aumenta el número de certificados emitidos en una infraestructura de clave pública (PKI), puede resultar difícil para una sola entidad de certificación (CA) realizar un seguimiento eficaz de los certificados emitidos.</span><span class="sxs-lookup"><span data-stu-id="07190-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="07190-105">Una manera de solucionar este problema consiste en crear una jerarquía de certificados en la que la entidad de certificación delegue la autoridad para emitir certificados a entidades subordinadas que, a su vez, pueden delegar la autoridad a sus subordinadas.</span><span class="sxs-lookup"><span data-stu-id="07190-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="07190-106">Cada entidad de certificación delega la autoridad mediante la emisión de un certificado de entidad de certificación a un subordinado.</span><span class="sxs-lookup"><span data-stu-id="07190-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="07190-107">La entidad de certificación inicial de la cadena se denomina raíz y no es necesario que una entidad establezca confianza con cualquier CA que resida en una [cadena de certificados](about-certificate-chain.md) diferente de la en la que reside la entidad.</span><span class="sxs-lookup"><span data-stu-id="07190-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="07190-108">En la ilustración siguiente se muestra una jerarquía de certificados formada por una CA raíz, dos entidades de certificación subordinadas a la raíz (una para el Departamento de marketing y otra para el Departamento de fabricación) y las CA subordinadas a ellas.</span><span class="sxs-lookup"><span data-stu-id="07190-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![diagrama de jerarquía de certificados](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="07190-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07190-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07190-111">Modelos de confianza</span><span class="sxs-lookup"><span data-stu-id="07190-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



