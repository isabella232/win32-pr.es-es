---
description: Crea un \# objeto de solicitud PKCS 7 para renovar un certificado existente. El objeto de solicitud usa un nuevo par de claves, pero conserva el proveedor de servicios criptográficos asociado al certificado que se va a renovar.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545878"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="dc04d-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="dc04d-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="dc04d-105">En el ejemplo enrollRenewalPKCS7 se crea un \# objeto de solicitud PKCS 7 para renovar un certificado existente.</span><span class="sxs-lookup"><span data-stu-id="dc04d-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="dc04d-106">El objeto de solicitud usa un nuevo par de claves, pero conserva el proveedor de servicios criptográficos asociado al certificado que se va a renovar.</span><span class="sxs-lookup"><span data-stu-id="dc04d-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="dc04d-107">Location</span><span class="sxs-lookup"><span data-stu-id="dc04d-107">Location</span></span>

<span data-ttu-id="dc04d-108">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="dc04d-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="dc04d-109">Debate</span><span class="sxs-lookup"><span data-stu-id="dc04d-109">Discussion</span></span>

<span data-ttu-id="dc04d-110">El ejemplo enrollRenewalPKCS7:</span><span class="sxs-lookup"><span data-stu-id="dc04d-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="dc04d-111">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="dc04d-111">Processes the command line arguments.</span></span> <span data-ttu-id="dc04d-112">La línea de comandos debe contener el nombre de la plantilla que se usa para crear la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="dc04d-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="dc04d-113">Recupera un certificado existente usando el nombre de la plantilla especificada en la línea de comandos o, si no se encuentra un certificado, intenta inscribir uno utilizando la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dc04d-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="dc04d-114">Las funciones findCertByTemplate y enrollCertByTemplate se definen en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="dc04d-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="dc04d-115">Comprueba la cadena de certificados y convierte el certificado en un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="dc04d-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="dc04d-116">Crea un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) y lo inicializa mediante el certificado existente.</span><span class="sxs-lookup"><span data-stu-id="dc04d-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="dc04d-117">Dado que el parámetro *inheritOptions* se establece en InheritDefault, se crea un nuevo par de claves para la solicitud, pero se usa el proveedor de servicios criptográficos del certificado existente.</span><span class="sxs-lookup"><span data-stu-id="dc04d-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="dc04d-118">Para obtener más información, vea el método [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .</span><span class="sxs-lookup"><span data-stu-id="dc04d-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="dc04d-119">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el \# objeto de solicitud PKCS 7, intenta inscribirlo con la CA y supervisa el estado del proceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="dc04d-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="dc04d-120">La función checkEnrollStatus se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="dc04d-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc04d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc04d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc04d-122">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="dc04d-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="dc04d-123">Solicitud de renovación de PKCS \# 7</span><span class="sxs-lookup"><span data-stu-id="dc04d-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="dc04d-124">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="dc04d-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



