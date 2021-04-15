---
description: Una cadena de certificados es una colección jerárquica de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación (CA) raíz de una organización.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadena de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669907"
---
# <a name="certificate-chain"></a><span data-ttu-id="e26c4-103">Cadena de certificados</span><span class="sxs-lookup"><span data-stu-id="e26c4-103">Certificate Chain</span></span>

<span data-ttu-id="e26c4-104">Una cadena de certificados es una colección jerárquica de certificados que conduce desde el usuario final o el equipo a una raíz de confianza, normalmente la entidad de certificación (CA) raíz de una organización.</span><span class="sxs-lookup"><span data-stu-id="e26c4-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="e26c4-105">Dado que todas las partes presuponen la confianza del certificado raíz, una entidad puede obtener confianza en un certificado de entidad final comprobando la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="e26c4-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="e26c4-106">Normalmente, la comprobación requiere el establecimiento de que cada certificado de la cadena:</span><span class="sxs-lookup"><span data-stu-id="e26c4-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="e26c4-107">Está firmado por la clave pública del certificado anterior.</span><span class="sxs-lookup"><span data-stu-id="e26c4-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="e26c4-108">No ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e26c4-108">Has not expired.</span></span>
-   <span data-ttu-id="e26c4-109">No se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="e26c4-109">Has not been revoked.</span></span>
-   <span data-ttu-id="e26c4-110">Se ajusta a las directivas especificadas por los certificados anteriores.</span><span class="sxs-lookup"><span data-stu-id="e26c4-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e26c4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e26c4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e26c4-112">Jerarquía de certificados</span><span class="sxs-lookup"><span data-stu-id="e26c4-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="e26c4-113">Certificación cruzada</span><span class="sxs-lookup"><span data-stu-id="e26c4-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="e26c4-114">Modelos de confianza</span><span class="sxs-lookup"><span data-stu-id="e26c4-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



