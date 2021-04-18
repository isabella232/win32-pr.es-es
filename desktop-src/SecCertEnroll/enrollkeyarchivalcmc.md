---
description: Crea una solicitud de certificado CMC para archivar una clave privada en una entidad de certificación (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686988"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="96fde-103">enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="96fde-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="96fde-104">El ejemplo enrollKeyArchivalCMC crea una solicitud de certificado CMC para archivar una clave privada en una entidad de certificación (CA).</span><span class="sxs-lookup"><span data-stu-id="96fde-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="96fde-105">Para obtener más información, consulte [solicitud de archivo de clave CMC](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="96fde-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="96fde-106">Location</span><span class="sxs-lookup"><span data-stu-id="96fde-106">Location</span></span>

<span data-ttu-id="96fde-107">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="96fde-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="96fde-108">Debate</span><span class="sxs-lookup"><span data-stu-id="96fde-108">Discussion</span></span>

<span data-ttu-id="96fde-109">El ejemplo enrollKeyArchivalCMC:</span><span class="sxs-lookup"><span data-stu-id="96fde-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="96fde-110">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="96fde-110">Processes the command line arguments.</span></span> <span data-ttu-id="96fde-111">La línea de comandos debe contener el nombre de la plantilla de certificado que se va a usar para la inscripción.</span><span class="sxs-lookup"><span data-stu-id="96fde-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="96fde-112">Crea un objeto de solicitud de certificado [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) y lo inicializa para un contexto de usuario final mediante el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="96fde-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="96fde-113">Establece la propiedad [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) en la solicitud CMC.</span><span class="sxs-lookup"><span data-stu-id="96fde-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="96fde-114">Crea un objeto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) y lo usa para recuperar una cadena que contiene la configuración de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="96fde-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="96fde-115">Crea un objeto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) de CryptoAPI y lo usa para recuperar el certificado de Exchange para la CA.</span><span class="sxs-lookup"><span data-stu-id="96fde-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="96fde-116">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inicializa mediante la solicitud CMC, crea una cadena codificada en Base64 que contiene la solicitud de archivo de clave y la envía a la CA.</span><span class="sxs-lookup"><span data-stu-id="96fde-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96fde-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96fde-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96fde-118">Solicitud de archivo de clave de CMC</span><span class="sxs-lookup"><span data-stu-id="96fde-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="96fde-119">Solicitud de CMC</span><span class="sxs-lookup"><span data-stu-id="96fde-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="96fde-120">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="96fde-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
