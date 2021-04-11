---
description: Las funciones CertAddCertificateLinkToStore, CertAddCRLLinkToStore y CertAddCTLLinkToStore agregan vínculos a los contextos existentes en los almacenes de certificados en lugar de agregar copias de esos contextos.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Vínculos de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156292"
---
# <a name="certificate-links"></a><span data-ttu-id="e83b6-103">Vínculos de certificado</span><span class="sxs-lookup"><span data-stu-id="e83b6-103">Certificate Links</span></span>

<span data-ttu-id="e83b6-104">Las funciones [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)y [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) agregan vínculos a los contextos existentes en los [*almacenes de certificados*](../secgloss/c-gly.md) en lugar de agregar copias de esos contextos.</span><span class="sxs-lookup"><span data-stu-id="e83b6-104">The functions [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore), and [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) add links to existing contexts into [*certificate stores*](../secgloss/c-gly.md) rather than adding copies of those contexts.</span></span> <span data-ttu-id="e83b6-105">La adición de vínculos a almacenes hace que el mismo [*certificado*](../secgloss/c-gly.md)físico, [*CRL*](../secgloss/c-gly.md)o [*CTL*](../secgloss/c-gly.md) esté disponible a través de varios almacenes diferentes.</span><span class="sxs-lookup"><span data-stu-id="e83b6-105">Adding links to stores makes the same physical [*certificate*](../secgloss/c-gly.md), [*CRL*](../secgloss/c-gly.md), or [*CTL*](../secgloss/c-gly.md) available through several different stores.</span></span> <span data-ttu-id="e83b6-106">Los cambios realizados en las propiedades extendidas de un [*contexto*](../secgloss/c-gly.md) desde el almacén del contexto original, o desde un almacén donde se almacena un vínculo a ese contexto, están disponibles en el almacén que contiene el contexto original y en todos los demás almacenes que tienen vínculos a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="e83b6-106">Changes made to the extended properties of a [*context*](../secgloss/c-gly.md) from the store of the original context, or from a store where a link to that context is stored, are available in the store that holds the original context and in all other stores that have links to that context.</span></span>

<span data-ttu-id="e83b6-107">Para obtener un ejemplo en el que se usa [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), vea [programa C del ejemplo: operaciones del almacén de certificados](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e83b6-107">For an example that uses [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

![vínculos de certificado](images/mancert1.png)

<span data-ttu-id="e83b6-109">Suponga que los certificados A. 1, A. 2, A. 3 y A. 4 se encuentran originalmente en el almacén A, y los certificados B. 1, b. 2, B. 3 y B. 4 se encuentran originalmente en la tienda B.</span><span class="sxs-lookup"><span data-stu-id="e83b6-109">Assume that certificates A.1, A.2, A.3, and A.4 are originally in store A, and certificates B.1, B.2, B.3, and B.4 are originally in store B.</span></span>

-   <span data-ttu-id="e83b6-110">En el diagrama se muestra un vínculo agregado en la tienda B al certificado A. 2 y un vínculo agregado en el almacén a al certificado B. 2.</span><span class="sxs-lookup"><span data-stu-id="e83b6-110">The diagram shows a link added in store B to certificate A.2 and a link added in store A to certificate B.2.</span></span>
-   <span data-ttu-id="e83b6-111">El original del certificado A. 2 todavía está en el almacén A. El original de B. 2 todavía está en la tienda B.</span><span class="sxs-lookup"><span data-stu-id="e83b6-111">The original of certificate A.2 is still in store A. The original of B.2 is still in store B.</span></span>
-   <span data-ttu-id="e83b6-112">Cualquier cambio realizado en las propiedades extendidas del certificado A. 2 o del certificado B. 2 de la tienda A o B estará disponible en ambas tiendas.</span><span class="sxs-lookup"><span data-stu-id="e83b6-112">Any changes made to the extended properties of certificate A.2 or certificate B.2 from either store A or store B will be available to both stores.</span></span>
-   <span data-ttu-id="e83b6-113">Si se realizó una copia del certificado A. 3 y se almacenó en el almacén B, los cambios que se realicen en las propiedades extendidas del certificado. 3 original creado en el almacén A no estarán visibles en la nueva copia del almacén B. Si se realizaron cambios en las propiedades extendidas de la copia del certificado A. 3 en la tienda B, esos cambios no afectarán al contenido del certificado A. 3 original y no se verán desde el almacén A.</span><span class="sxs-lookup"><span data-stu-id="e83b6-113">If a copy of certificate A.3 were made and stored in store B, any changes to the extended properties of the original A.3 certificate made from store A would not be visible in the new copy in store B. If changes were made to the extended properties of the copy of certificate A.3 in store B, those changes would not affect the contents of the original A.3 certificate and would not be visible from store A.</span></span>

 

 
