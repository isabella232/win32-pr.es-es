---
description: La certificación cruzada permite a las entidades de una infraestructura de clave pública (PKI) confiar en entidades de otra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificación cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277966"
---
# <a name="cross-certification"></a><span data-ttu-id="ce28e-103">Certificación cruzada</span><span class="sxs-lookup"><span data-stu-id="ce28e-103">Cross Certification</span></span>

<span data-ttu-id="ce28e-104">La certificación cruzada permite a las entidades de una infraestructura de clave pública (PKI) confiar en entidades de otra PKI.</span><span class="sxs-lookup"><span data-stu-id="ce28e-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="ce28e-105">Esta relación de confianza mutua normalmente es compatible con un acuerdo de certificación cruzada entre las entidades de certificación (CA) de cada PKI.</span><span class="sxs-lookup"><span data-stu-id="ce28e-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="ce28e-106">El acuerdo establece las responsabilidades y responsabilidad de cada entidad.</span><span class="sxs-lookup"><span data-stu-id="ce28e-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="ce28e-107">Una relación de confianza mutua entre dos CA requiere que cada CA emita un certificado al otro para establecer la relación en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="ce28e-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="ce28e-108">La ruta de acceso de confianza no es jerárquica (ninguna de las entidades de certificación de control está subordinada al otro), aunque las PKI independientes pueden ser jerarquías de certificados.</span><span class="sxs-lookup"><span data-stu-id="ce28e-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="ce28e-109">Una vez que se han establecido dos CA y se han especificado las condiciones de confianza y los certificados emitidos entre sí, las entidades dentro de PKI independientes pueden interactuar de acuerdo con las directivas especificadas en los certificados.</span><span class="sxs-lookup"><span data-stu-id="ce28e-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![diagrama de certificación cruzada](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="ce28e-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce28e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce28e-112">Modelos de confianza</span><span class="sxs-lookup"><span data-stu-id="ce28e-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



