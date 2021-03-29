---
description: Crea una solicitud de certificado CMC e inscribe un equipo en una jerarquía de certificados.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810700"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="71e3f-103">enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="71e3f-103">enrollCustomCMC</span></span>

<span data-ttu-id="71e3f-104">El ejemplo enrollCustomCMC crea una solicitud de certificado CMC e inscribe un equipo en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="71e3f-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="71e3f-105">Location</span><span class="sxs-lookup"><span data-stu-id="71e3f-105">Location</span></span>

<span data-ttu-id="71e3f-106">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="71e3f-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="71e3f-107">Debate</span><span class="sxs-lookup"><span data-stu-id="71e3f-107">Discussion</span></span>

<span data-ttu-id="71e3f-108">El ejemplo enrollCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="71e3f-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="71e3f-109">Procesa los siguientes argumentos de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="71e3f-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="71e3f-110">Par de nombre y valor personalizado que se va a agregar a la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="71e3f-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="71e3f-111">Un nombre de sujeto alternativo.</span><span class="sxs-lookup"><span data-stu-id="71e3f-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="71e3f-112">Identificador de objeto (OID) para la extensión uso mejorado de clave (EKU).</span><span class="sxs-lookup"><span data-stu-id="71e3f-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="71e3f-113">Crea un objeto de solicitud [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante el contexto de equipo.</span><span class="sxs-lookup"><span data-stu-id="71e3f-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="71e3f-114">Usa la \# solicitud PKCS 10 para inicializar un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="71e3f-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="71e3f-115">Crea un objeto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) mediante el OID especificado en la línea de comandos y lo agrega a la colección de extensiones para la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="71e3f-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="71e3f-116">Crea el objeto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) con el nombre especificado en la línea de comandos, lo agrega a la colección [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa la colección para inicializar una extensión [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) y lo agrega a la colección de extensiones para la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="71e3f-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="71e3f-117">Crea un objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) con el nombre y el valor especificados en la línea de comandos y lo agrega a la colección [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) en la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="71e3f-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="71e3f-118">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante el objeto de solicitud CMC y recupera una cadena que contiene una solicitud codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="71e3f-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="71e3f-119">Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="71e3f-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="71e3f-120">Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="71e3f-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="71e3f-121">Comprueba el estado de envío y, si se realiza correctamente, instala el certificado en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="71e3f-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e3f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71e3f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e3f-123">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="71e3f-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="71e3f-124">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="71e3f-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="71e3f-125">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="71e3f-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
