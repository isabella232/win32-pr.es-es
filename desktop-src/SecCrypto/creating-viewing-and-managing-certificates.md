---
description: Los certificados tienen propiedades asociadas, como un nombre para mostrar, una descripción y usos permitidos, que se pueden ver y editar.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Creación, visualización y administración de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666419"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="f4742-103">Creación, visualización y administración de certificados</span><span class="sxs-lookup"><span data-stu-id="f4742-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="f4742-104">Los [*certificados*](../secgloss/c-gly.md) son estructuras de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4742-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="f4742-105">Se puede ver el contenido de un certificado, pero no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="f4742-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="f4742-106">La información del propio certificado incluye las fechas de validez del certificado, el emisor, el asunto y la clave pública.</span><span class="sxs-lookup"><span data-stu-id="f4742-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="f4742-107">Sin embargo, los certificados tienen propiedades asociadas, como un nombre para mostrar, una descripción y usos permitidos, que se pueden ver y editar.</span><span class="sxs-lookup"><span data-stu-id="f4742-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="f4742-108">En esta sección se muestra cómo crear certificados de prueba, ver certificados y administrar certificados y otros objetos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f4742-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="f4742-109">Los certificados y los [*certificados de editor de software*](../secgloss/s-gly.md) (SPCS) que se pueden crear con Makecert están estrictamente para fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="f4742-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="f4742-110">Un [*certificado raíz*](../secgloss/r-gly.md) de prueba y una [*clave privada*](../secgloss/p-gly.md) raíz de prueba se proporcionan únicamente con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="f4742-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="f4742-111">Los fabricantes de software independientes deben obtener un certificado de GTE, VeriSign, Inc. u otra [*entidad de certificación*](../secgloss/c-gly.md) (CA) para firmar el código que se distribuirá al público.</span><span class="sxs-lookup"><span data-stu-id="f4742-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="f4742-112">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="f4742-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="f4742-113">Uso de MakeCert</span><span class="sxs-lookup"><span data-stu-id="f4742-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="f4742-114">Usar Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="f4742-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="f4742-115">Usar CertMgr</span><span class="sxs-lookup"><span data-stu-id="f4742-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
