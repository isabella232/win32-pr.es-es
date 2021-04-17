---
description: El SDK de inscripción de certificados se puede usar para crear \# solicitudes de certificados PKCS 10, PKCS \# 7, CMC y autofirmado.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Solicitudes de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686994"
---
# <a name="certificate-requests"></a><span data-ttu-id="078e5-103">Solicitudes de certificado</span><span class="sxs-lookup"><span data-stu-id="078e5-103">Certificate Requests</span></span>

<span data-ttu-id="078e5-104">El SDK de inscripción de certificados se puede usar para crear \# solicitudes de certificados PKCS 10, PKCS \# 7, CMC y autofirmado.</span><span class="sxs-lookup"><span data-stu-id="078e5-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="078e5-105">Cada tipo de solicitud se representa mediante una de las interfaces enumeradas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="078e5-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="078e5-106">Todas las interfaces de solicitud heredan directa o indirectamente de la interfaz [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) .</span><span class="sxs-lookup"><span data-stu-id="078e5-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="078e5-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="078e5-107">Interface</span></span>                                                                        | <span data-ttu-id="078e5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="078e5-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="078e5-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="078e5-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="078e5-110">Representa una \# solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="078e5-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="078e5-111">Esta interfaz hereda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="078e5-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="078e5-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="078e5-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="078e5-113">Representa una \# solicitud PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="078e5-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="078e5-114">Esta interfaz hereda de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="078e5-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="078e5-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="078e5-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="078e5-116">Representa un certificado autofirmado.</span><span class="sxs-lookup"><span data-stu-id="078e5-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="078e5-117">Esta interfaz hereda de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="078e5-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="078e5-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="078e5-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="078e5-119">Representa una solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="078e5-119">Represents a CMC request.</span></span> <span data-ttu-id="078e5-120">Esta interfaz hereda de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="078e5-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="078e5-121">En la ilustración siguiente se muestra la estructura de herencia de los objetos de solicitud admitidos por la API de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="078e5-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="078e5-122">Un objeto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) actúa, directa o indirectamente, como la clase base para todos los objetos de solicitud disponibles.</span><span class="sxs-lookup"><span data-stu-id="078e5-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![estructura de herencia para las interfaces de solicitud](images/certificate-request-inheritance.png)

<span data-ttu-id="078e5-124">Independientemente del tipo, una solicitud de certificado contiene información sobre el sujeto que realiza la solicitud, la clave pública del sujeto, un conjunto de atributos, un conjunto de extensiones X. 509 versión 3 (que pueden enviarse como parte de los atributos) y una firma.</span><span class="sxs-lookup"><span data-stu-id="078e5-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="078e5-125">Estos problemas se abordan en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="078e5-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="078e5-126">Nombres de sujeto</span><span class="sxs-lookup"><span data-stu-id="078e5-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="078e5-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="078e5-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="078e5-128">Extensiones</span><span class="sxs-lookup"><span data-stu-id="078e5-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="078e5-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="078e5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="078e5-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="078e5-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="078e5-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="078e5-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="078e5-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="078e5-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="078e5-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="078e5-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



