---
description: Inicializa un objeto de \# solicitud de certificado PKCS 10, lo encapsula en un objeto de solicitud CMC, envía la solicitud CMC a una entidad de certificación (CA) empresarial y guarda el certificado devuelto por la CA en un archivo.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810694"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="0f4e1-103">enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="0f4e1-103">enrollFromPublicKey</span></span>

<span data-ttu-id="0f4e1-104">En el ejemplo enrollFromPublicKey se inicializa un \# objeto de solicitud de certificado PKCS 10, se encapsula en un objeto de solicitud CMC, se envía la solicitud CMC a una entidad de certificación (CA) empresarial y se guarda el certificado devuelto por la CA en un archivo.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="0f4e1-105">Location</span><span class="sxs-lookup"><span data-stu-id="0f4e1-105">Location</span></span>

<span data-ttu-id="0f4e1-106">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="0f4e1-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0f4e1-107">Debate</span><span class="sxs-lookup"><span data-stu-id="0f4e1-107">Discussion</span></span>

<span data-ttu-id="0f4e1-108">El ejemplo enrollFromPublicKey:</span><span class="sxs-lookup"><span data-stu-id="0f4e1-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="0f4e1-109">Procesa los siguientes argumentos de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="0f4e1-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0f4e1-110">Nombre de una plantilla de certificado.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="0f4e1-111">Nombre de un archivo en el que se va a guardar el certificado instalado como una matriz de bytes codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="0f4e1-112">Nombre opcional de la plantilla de certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-112">An optional signing certificate template name.</span></span> <span data-ttu-id="0f4e1-113">La plantilla se usa para crear un certificado de firma si no existe ninguno en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="0f4e1-114">Crea un objeto de clave privada [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y llama al método [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) para crear una clave privada asimétrica con el proveedor de servicios criptográficos, el tamaño de clave y los valores de [**especificación**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) de clave predeterminados para el equipo actual.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="0f4e1-115">Recupera la parte de la clave pública del objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .</span><span class="sxs-lookup"><span data-stu-id="0f4e1-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="0f4e1-116">Crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo Inicializa utilizando la plantilla especificada en la línea de comandos y la clave pública.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="0f4e1-117">Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el \# objeto de solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="0f4e1-118">Recupera un certificado de firma existente o, si no se encuentra ninguno, crea una solicitud de certificado a partir de la plantilla especificada en la línea de comandos e intenta inscribirla.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="0f4e1-119">FindCertByKeyUsage se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="0f4e1-120">Comprueba la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="0f4e1-121">Crea un objeto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inicializa mediante el certificado de firma, recupera la colección [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) del objeto de solicitud CMC y agrega el objeto de certificado de firma a la colección.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="0f4e1-122">Codifica la solicitud CMC mediante [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="0f4e1-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="0f4e1-123">Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="0f4e1-124">Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa más las cadenas que contienen la configuración de la entidad de certificación y la solicitud de certificado para enviar la solicitud a la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="0f4e1-125">Comprueba el estado del proceso de inscripción y guarda el certificado instalado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="0f4e1-126">La función EncodeToFileW se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="0f4e1-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f4e1-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f4e1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f4e1-128">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="0f4e1-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="0f4e1-129">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="0f4e1-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0f4e1-130">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="0f4e1-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
