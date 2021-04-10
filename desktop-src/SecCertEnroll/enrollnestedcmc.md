---
description: Lee una solicitud de certificado CMC existente desde un archivo, la incluye en otra solicitud CMC, firma esta solicitud externa, la envía a una entidad de certificación (CA) y guarda la respuesta del certificado de la CA en un archivo.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275210"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="13cd4-103">enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="13cd4-103">enrollNestedCMC</span></span>

<span data-ttu-id="13cd4-104">En el ejemplo enrollNestedCMC se lee una solicitud de certificado CMC existente desde un archivo, se incluye en otra solicitud CMC, se firma esta solicitud externa, se envía a una entidad de certificación (CA) y se guarda la respuesta del certificado de la CA en un archivo.</span><span class="sxs-lookup"><span data-stu-id="13cd4-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="13cd4-105">Location</span><span class="sxs-lookup"><span data-stu-id="13cd4-105">Location</span></span>

<span data-ttu-id="13cd4-106">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples enrollNestedCMC de la \\ inscripción de certificados de \\ VC \\ .</span><span class="sxs-lookup"><span data-stu-id="13cd4-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="13cd4-107">Debate</span><span class="sxs-lookup"><span data-stu-id="13cd4-107">Discussion</span></span>

<span data-ttu-id="13cd4-108">El ejemplo enrollNestedCMC:</span><span class="sxs-lookup"><span data-stu-id="13cd4-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="13cd4-109">Procesa los siguientes argumentos de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="13cd4-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="13cd4-110">Nombre del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="13cd4-110">The name of the input file.</span></span>
    -   <span data-ttu-id="13cd4-111">Nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="13cd4-111">The name of the output file.</span></span>
    -   <span data-ttu-id="13cd4-112">Una plantilla de solicitud opcional.</span><span class="sxs-lookup"><span data-stu-id="13cd4-112">An optional request template.</span></span>
2.  <span data-ttu-id="13cd4-113">Lee una solicitud CMC existente desde un archivo como una matriz de bytes codificada en base63, convierte la matriz de bytes en un **BSTR**, crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y usa **BSTR** para inicializar el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="13cd4-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="13cd4-114">El objeto inicializado se convierte en la solicitud interna.</span><span class="sxs-lookup"><span data-stu-id="13cd4-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="13cd4-115">Usa el objeto de solicitud interno creado e inicializado en el paso anterior para inicializar otra solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="13cd4-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="13cd4-116">Recupera un certificado de firma existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirla.</span><span class="sxs-lookup"><span data-stu-id="13cd4-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="13cd4-117">Las funciones findCertByTemplate y enrollCertByTemplate se definen en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="13cd4-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="13cd4-118">Recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de la solicitud CMC externa, crea un nuevo objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de firma recuperado y lo agrega a la colección.</span><span class="sxs-lookup"><span data-stu-id="13cd4-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="13cd4-119">Codifica la solicitud CMC mediante reglas de codificación distinguida (DER) y recupera la solicitud como **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="13cd4-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="13cd4-120">Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="13cd4-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="13cd4-121">Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="13cd4-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="13cd4-122">Comprueba el estado del proceso de inscripción y guarda la respuesta del certificado de la CA en un archivo.</span><span class="sxs-lookup"><span data-stu-id="13cd4-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="13cd4-123">La función EncodeToFileW se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="13cd4-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13cd4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13cd4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cd4-125">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="13cd4-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="13cd4-126">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="13cd4-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
