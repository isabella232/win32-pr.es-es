---
description: Crea una solicitud de certificado CMC en nombre de otro usuario e inscribe el usuario en una jerarquía de certificados.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542683"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="03950-103">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="03950-103">enrollEOBOCMC</span></span>

<span data-ttu-id="03950-104">El ejemplo enrollEOBOCMC crea una solicitud de certificado CMC en nombre de otro usuario e inscribe el usuario en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="03950-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="03950-105">La inscripción en nombre de otro usuario requiere que la solicitud de certificado se firme con un certificado de agente de inscripción.</span><span class="sxs-lookup"><span data-stu-id="03950-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="03950-106">Location</span><span class="sxs-lookup"><span data-stu-id="03950-106">Location</span></span>

<span data-ttu-id="03950-107">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="03950-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="03950-108">Debate</span><span class="sxs-lookup"><span data-stu-id="03950-108">Discussion</span></span>

<span data-ttu-id="03950-109">El ejemplo enrollEOBOCMC:</span><span class="sxs-lookup"><span data-stu-id="03950-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="03950-110">Procesa los siguientes argumentos de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="03950-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="03950-111">Nombre de una plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="03950-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="03950-112">Nombre del usuario que solicita el certificado.</span><span class="sxs-lookup"><span data-stu-id="03950-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="03950-113">El nombre de un archivo de intercambio de información personal (PFX) en el que se guardará la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03950-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="03950-114">Contraseña que se va a usar con el archivo PFX.</span><span class="sxs-lookup"><span data-stu-id="03950-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="03950-115">Un nombre de plantilla de agente de inscripción opcional.</span><span class="sxs-lookup"><span data-stu-id="03950-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="03950-116">La plantilla se usa para crear un certificado de agente de inscripción si no existe ninguno en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="03950-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="03950-117">Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el uso de la plantilla de certificado especificada en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="03950-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="03950-118">Agrega el nombre del solicitante al objeto de solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="03950-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="03950-119">Recupera un certificado de agente de inscripción existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla de agente de inscripción especificada en la línea de comandos e intenta inscribirla.</span><span class="sxs-lookup"><span data-stu-id="03950-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="03950-120">Comprueba la cadena de certificados que contiene el certificado de agente de inscripción.</span><span class="sxs-lookup"><span data-stu-id="03950-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="03950-121">Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de agente de inscripción, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud CMC y agrega el objeto de certificado de firma del agente de inscripción a la colección.</span><span class="sxs-lookup"><span data-stu-id="03950-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="03950-122">El objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) que se describe en el siguiente paso usa el certificado para firmar la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="03950-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="03950-123">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante la solicitud CMC, intenta inscribirse y comprueba el progreso del proceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="03950-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="03950-124">Exporta el certificado instalado a un archivo PFX.</span><span class="sxs-lookup"><span data-stu-id="03950-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="03950-125">El archivo está protegido mediante la contraseña especificada en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="03950-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="03950-126">La función EncodeToFileW se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="03950-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="03950-127">Elimina el certificado del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="03950-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="03950-128">Las funciones que se usan en el siguiente ejemplo de código se pueden encontrar en la documentación de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="03950-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="03950-129">Elimina la clave privada del equipo.</span><span class="sxs-lookup"><span data-stu-id="03950-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03950-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03950-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03950-131">Solicitud EOBO de CMC</span><span class="sxs-lookup"><span data-stu-id="03950-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="03950-132">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="03950-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="03950-133">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="03950-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



