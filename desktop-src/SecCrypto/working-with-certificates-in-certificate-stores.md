---
description: Varias funciones agregan un contexto de certificado o un vínculo a un contexto a un \[ Kit de desarrollo de software (SDK) de plataforma de almacén \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Trabajar con certificados en almacenes de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361131"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="fdc59-103">Trabajar con certificados en almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="fdc59-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="fdc59-104">Varias funciones agregan un contexto de certificado o un vínculo a un contexto de un almacén.</span><span class="sxs-lookup"><span data-stu-id="fdc59-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="fdc59-105">Para certificados que ya están en forma de contexto de certificado:</span><span class="sxs-lookup"><span data-stu-id="fdc59-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="fdc59-106">**CertAddCertificateContextToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="fdc59-107">**CertAddCRLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="fdc59-108">**CertAddCTLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="fdc59-109">**CertAddCertificateLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="fdc59-110">**CertAddCRLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="fdc59-111">**CertAddCTLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="fdc59-112">Para los certificados que están en forma codificada pero no con contextos de certificado completos:</span><span class="sxs-lookup"><span data-stu-id="fdc59-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="fdc59-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="fdc59-114">**CertAddEncodedCRLToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="fdc59-115">**CertAddEncodedCTLToStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="fdc59-116">Las siguientes funciones eliminan un certificado, una CRL o una CTL de un almacén mediante la reducción de su recuento de referencias en uno.</span><span class="sxs-lookup"><span data-stu-id="fdc59-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="fdc59-117">Si esto hace que el recuento de referencias sea cero, se libera la memoria usada para almacenar el certificado, la CRL o la CTL.</span><span class="sxs-lookup"><span data-stu-id="fdc59-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="fdc59-118">**CertDeleteCertificateFromStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="fdc59-119">**CertDeleteCRLFromStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="fdc59-120">**CertDeleteCTLFromStore**</span><span class="sxs-lookup"><span data-stu-id="fdc59-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



