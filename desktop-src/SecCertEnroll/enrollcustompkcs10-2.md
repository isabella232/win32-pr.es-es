---
description: Crea una solicitud PKCS \# 10 personalizada e intenta inscribirla en una entidad de certificación (CA) empresarial.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686992"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="8a74e-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="8a74e-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="8a74e-104">En el \_ ejemplo enrollCustomPKCS10 2 se crea una \# solicitud de PKCS 10 personalizada y se intenta inscribir en una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) empresarial.</span><span class="sxs-lookup"><span data-stu-id="8a74e-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="8a74e-105">Location</span><span class="sxs-lookup"><span data-stu-id="8a74e-105">Location</span></span>

<span data-ttu-id="8a74e-106">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala de forma predeterminada en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="8a74e-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="8a74e-107">Debate</span><span class="sxs-lookup"><span data-stu-id="8a74e-107">Discussion</span></span>

<span data-ttu-id="8a74e-108">El \_ ejemplo enrollCustomPKCS10 2:</span><span class="sxs-lookup"><span data-stu-id="8a74e-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="8a74e-109">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8a74e-109">Processes the command line arguments.</span></span> <span data-ttu-id="8a74e-110">La línea de comandos debe contener el nombre de una plantilla y el nombre de un proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="8a74e-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="8a74e-111">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo Inicializa utilizando el nombre de la plantilla especificada en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8a74e-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="8a74e-112">Recupera la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly) del objeto de inscripción.</span><span class="sxs-lookup"><span data-stu-id="8a74e-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="8a74e-113">Recupera la solicitud PKCS 10 más interna \# del objeto de solicitud de certificado obtenido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="8a74e-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="8a74e-114">Recupera una [*clave privada*](/windows/desktop/SecGloss/p-gly) de la solicitud PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="8a74e-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="8a74e-115">Crea una colección [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) y agrega los proveedores de servicios criptográficos disponibles a la colección y, a continuación, recupera un objeto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) para el proveedor especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8a74e-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="8a74e-116">Establece el objeto de estado en la clave privada.</span><span class="sxs-lookup"><span data-stu-id="8a74e-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="8a74e-117">Intenta inscribir la [*solicitud de certificado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="8a74e-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a74e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a74e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a74e-119">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="8a74e-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="8a74e-120">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="8a74e-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
