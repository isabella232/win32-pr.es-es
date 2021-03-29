---
description: Crea una \# solicitud PKCS 7 desde un certificado existente heredando las claves públicas y privadas y la plantilla de certificado.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808665"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="cbaf4-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="cbaf4-103">enrollPKCS7</span></span>

<span data-ttu-id="cbaf4-104">El ejemplo enrollPKCS7 crea una \# solicitud PKCS 7 a partir de un certificado existente heredando las claves públicas y privadas y la plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="cbaf4-105">El certificado existente se usa para firmar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="cbaf4-106">En este ejemplo se inscribe el usuario en una jerarquía de certificados y se instala la respuesta del certificado.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="cbaf4-107">En el ejemplo se utiliza un certificado existente para inscribir e instalar uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="cbaf4-108">Para obtener más información sobre cómo renovar un certificado existente, vea [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="cbaf4-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="cbaf4-109">Location</span><span class="sxs-lookup"><span data-stu-id="cbaf4-109">Location</span></span>

<span data-ttu-id="cbaf4-110">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="cbaf4-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="cbaf4-111">Debate</span><span class="sxs-lookup"><span data-stu-id="cbaf4-111">Discussion</span></span>

<span data-ttu-id="cbaf4-112">El ejemplo enrollPKCS7:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="cbaf4-113">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-113">Processes the command line arguments.</span></span> <span data-ttu-id="cbaf4-114">La línea de comandos debe contener el nombre de la plantilla de certificado que se usa para buscar un certificado existente.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="cbaf4-115">Recupera un certificado existente usando el nombre de la plantilla especificada en la línea de comandos o, si no se encuentra un certificado, intenta inscribir uno nuevo creado con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="cbaf4-116">Las funciones findCertByTemplate y enrollCertByTemplate se definen en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="cbaf4-117">Comprueba la cadena de certificados y convierte el certificado en un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="cbaf4-118">Crea un objeto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) y lo inicializa mediante el certificado existente.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="cbaf4-119">El nuevo \# objeto de solicitud PKCS 7 hereda las claves públicas y privadas y la plantilla del certificado existente.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="cbaf4-120">Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado existente y lo agrega al \# objeto de solicitud PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="cbaf4-121">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el \# objeto de solicitud PKCS 7, intenta inscribirlo con la CA y supervisa el estado del proceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="cbaf4-122">La función checkEnrollStatus se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbaf4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbaf4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbaf4-124">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="cbaf4-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="cbaf4-125">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="cbaf4-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



