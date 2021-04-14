---
description: Crea un objeto de solicitud CMC a partir de una solicitud PKCS 10 anidada interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360145"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="59298-103">createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="59298-103">createCNGCustomCMC</span></span>

<span data-ttu-id="59298-104">En el ejemplo createCNGCustomCMC se crea un objeto de solicitud CMC a partir de una solicitud anidada PKCS \# 10 interna.</span><span class="sxs-lookup"><span data-stu-id="59298-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="59298-105">La solicitud interna se crea con una [*clave privada*](/windows/desktop/SecGloss/p-gly)asimétrica.</span><span class="sxs-lookup"><span data-stu-id="59298-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="59298-106">La clave privada se crea mediante el proveedor criptográfico Cryptography API: Next Generation (CNG) y el algoritmo especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="59298-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="59298-107">También se establecen opciones personalizadas como la Directiva de exportación y el nivel de protección de claves en la clave privada.</span><span class="sxs-lookup"><span data-stu-id="59298-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="59298-108">Location</span><span class="sxs-lookup"><span data-stu-id="59298-108">Location</span></span>

<span data-ttu-id="59298-109">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="59298-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="59298-110">Debate</span><span class="sxs-lookup"><span data-stu-id="59298-110">Discussion</span></span>

<span data-ttu-id="59298-111">El ejemplo createCNGCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="59298-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="59298-112">Procesa los siguientes argumentos de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="59298-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="59298-113">Nombre de un proveedor de [*servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) de CNG.</span><span class="sxs-lookup"><span data-stu-id="59298-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="59298-114">Nombre del algoritmo utilizado para generar una clave privada asimétrica.</span><span class="sxs-lookup"><span data-stu-id="59298-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="59298-115">Nombre del algoritmo utilizado para aplicar un algoritmo [*hash*](/windows/desktop/SecGloss/h-gly) a la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="59298-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="59298-116">Archivo de salida en el que se va a guardar la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="59298-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="59298-117">Una cadena opcional (AlternateSignature) que, si está presente, especifica que se use un algoritmo de firma discreto en lugar de uno combinado.</span><span class="sxs-lookup"><span data-stu-id="59298-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="59298-118">Para obtener más información, vea la propiedad [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .</span><span class="sxs-lookup"><span data-stu-id="59298-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="59298-119">Crea un objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) y establece las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="59298-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="59298-120">**LegacyCsp**</span><span class="sxs-lookup"><span data-stu-id="59298-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="59298-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="59298-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="59298-122">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="59298-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="59298-123">**KeyProtection**</span><span class="sxs-lookup"><span data-stu-id="59298-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="59298-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="59298-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="59298-125">Crea una clave privada asimétrica.</span><span class="sxs-lookup"><span data-stu-id="59298-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="59298-126">Crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) y lo inicializa mediante la clave privada.</span><span class="sxs-lookup"><span data-stu-id="59298-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="59298-127">Crea un objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa mediante el \# objeto de solicitud PKCS 10 creado en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="59298-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="59298-128">Establece la marca de algoritmo de firma alternativa en **Variant \_ true** o **Variant \_ false** en función de si se ha especificado una cadena de firma alternativa en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="59298-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="59298-129">Para obtener más información, vea [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span><span class="sxs-lookup"><span data-stu-id="59298-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="59298-130">Crea un [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) de [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) (OID) a partir del nombre del algoritmo especificado en la línea de comandos y establece el OID en el objeto de solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="59298-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="59298-131">Firma la solicitud de certificado y la codifica mediante [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="59298-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="59298-132">Recupera una cadena que contiene la solicitud de certificado CMC codificada y la guarda en un archivo.</span><span class="sxs-lookup"><span data-stu-id="59298-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="59298-133">La función EncodeToFileW se define en EnrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="59298-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59298-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59298-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59298-135">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="59298-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="59298-136">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="59298-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="59298-137">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="59298-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="59298-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="59298-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
