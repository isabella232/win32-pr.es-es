---
description: Se pueden usar las siguientes interfaces para crear solicitudes de certificado.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfaces de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154737"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="e39eb-103">Interfaces de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="e39eb-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="e39eb-104">Se pueden usar las siguientes interfaces para crear solicitudes de certificado.</span><span class="sxs-lookup"><span data-stu-id="e39eb-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="e39eb-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e39eb-105">Interface</span></span>                                                                          | <span data-ttu-id="e39eb-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e39eb-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e39eb-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="e39eb-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="e39eb-108">Representa la interfaz abstracta de nivel superior para una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="e39eb-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="e39eb-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="e39eb-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="e39eb-110">Permite crear certificados directamente sin pasar por un registro o una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="e39eb-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="e39eb-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="e39eb-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="e39eb-112">Extiende la interfaz [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) para habilitar la inicialización desde una plantilla.</span><span class="sxs-lookup"><span data-stu-id="e39eb-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="e39eb-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="e39eb-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="e39eb-114">Representa una solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="e39eb-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="e39eb-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="e39eb-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="e39eb-116">Extiende la interfaz [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) para habilitar la inicialización desde una plantilla.</span><span class="sxs-lookup"><span data-stu-id="e39eb-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="e39eb-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="e39eb-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="e39eb-118">Representa una \# solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="e39eb-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="e39eb-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="e39eb-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="e39eb-120">Extiende la interfaz [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) para habilitar la inicialización desde una plantilla.</span><span class="sxs-lookup"><span data-stu-id="e39eb-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="e39eb-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="e39eb-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="e39eb-122">Extiende la interfaz [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y agrega propiedades que habilitan la atestación de certificados TPM.</span><span class="sxs-lookup"><span data-stu-id="e39eb-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="e39eb-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="e39eb-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="e39eb-124">Representa una \# solicitud PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="e39eb-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="e39eb-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="e39eb-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="e39eb-126">Extiende la interfaz [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) para habilitar la inicialización desde una plantilla.</span><span class="sxs-lookup"><span data-stu-id="e39eb-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="e39eb-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e39eb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39eb-128">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="e39eb-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



