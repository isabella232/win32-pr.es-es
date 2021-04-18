---
description: Los servicios de Certificate Server admiten jerarquías de entidades de certificación (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Jerarquías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668207"
---
# <a name="hierarchies"></a><span data-ttu-id="abb21-103">Jerarquías</span><span class="sxs-lookup"><span data-stu-id="abb21-103">Hierarchies</span></span>

<span data-ttu-id="abb21-104">Los servicios de Certificate Server admiten jerarquías de [*entidades de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="abb21-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="abb21-105">Una [*jerarquía de entidad de certificación*](../secgloss/c-gly.md) consta de una entidad de certificación de nivel superior (denominada entidad de certificación raíz) con una o más CA subordinadas que la CA raíz ha emitido certificados.</span><span class="sxs-lookup"><span data-stu-id="abb21-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="abb21-106">Un posible escenario de jerarquía de CA sería en una organización con una CA raíz que se usaba para emitir certificados a varias CA subordinadas.</span><span class="sxs-lookup"><span data-stu-id="abb21-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="abb21-107">A continuación, las CA subordinadas pueden emitir certificados de entidad final, como los certificados emitidos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="abb21-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="abb21-108">El certificado del usuario contendrá una ruta de acceso de confianza para la jerarquía de la entidad de certificación, en este caso, incluido el certificado para la CA subordinada emisora y la CA raíz.</span><span class="sxs-lookup"><span data-stu-id="abb21-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
