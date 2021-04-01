---
description: Inscribe a un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre de sujeto y la longitud, en bits, de la clave.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082876"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="7774b-103">enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="7774b-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="7774b-104">El ejemplo enrollSimpleUserCert inscribe a un usuario final con una entidad de certificación (CA) mediante una plantilla, el nombre de sujeto y la longitud, en bits, de la clave.</span><span class="sxs-lookup"><span data-stu-id="7774b-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="7774b-105">Location</span><span class="sxs-lookup"><span data-stu-id="7774b-105">Location</span></span>

<span data-ttu-id="7774b-106">Cuando se instala el kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ enrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="7774b-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="7774b-107">Una versión de C# se instala en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Enrollment \\ CSharp \\ EnrollSimpleUserCert</span><span class="sxs-lookup"><span data-stu-id="7774b-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="7774b-108">Debate</span><span class="sxs-lookup"><span data-stu-id="7774b-108">Discussion</span></span>

<span data-ttu-id="7774b-109">El ejemplo enrollSimpleUserCert:</span><span class="sxs-lookup"><span data-stu-id="7774b-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="7774b-110">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7774b-110">Processes the command line arguments.</span></span> <span data-ttu-id="7774b-111">La línea de comandos debe contener el nombre de la plantilla, el nombre del firmante y la longitud de la clave.</span><span class="sxs-lookup"><span data-stu-id="7774b-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="7774b-112">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo inicializa mediante la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7774b-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="7774b-113">Recupera el objeto de solicitud de certificado interno del objeto de inscripción y lo consulta para el objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="7774b-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="7774b-114">La solicitud más interna es siempre una \# solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="7774b-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="7774b-115">Recupera el objeto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) de la solicitud PKCS \# 10 y establece la longitud de clave especificada en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7774b-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="7774b-116">Crea un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , lo usa para codificar el nombre de sujeto X. 500 y agrega el nombre a la \# solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="7774b-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="7774b-117">Intenta inscribir el usuario final con la CA y supervisa el progreso del proceso de inscripción.</span><span class="sxs-lookup"><span data-stu-id="7774b-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="7774b-118">La función checkEnrollStatus se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="7774b-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7774b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7774b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7774b-120">\#Solicitud PKCS 10</span><span class="sxs-lookup"><span data-stu-id="7774b-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="7774b-121">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="7774b-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



