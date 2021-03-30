---
description: Instala un certificado inscrito de un archivo de intercambio de información personal (PFX) en el almacén de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002677"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="d6eb0-103">installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="d6eb0-103">installResponseFromPFX</span></span>

<span data-ttu-id="d6eb0-104">El ejemplo installResponseFromPFX instala un certificado inscrito de un archivo de intercambio de información personal (PFX) en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="d6eb0-105">Location</span><span class="sxs-lookup"><span data-stu-id="d6eb0-105">Location</span></span>

<span data-ttu-id="d6eb0-106">Al instalar el kit de desarrollo de software (SDK) de Microsoft Windows, el ejemplo se instala, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="d6eb0-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="d6eb0-107">Debate</span><span class="sxs-lookup"><span data-stu-id="d6eb0-107">Discussion</span></span>

<span data-ttu-id="d6eb0-108">El ejemplo installResponseFromPFX:</span><span class="sxs-lookup"><span data-stu-id="d6eb0-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="d6eb0-109">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-109">Processes the command line arguments.</span></span> <span data-ttu-id="d6eb0-110">La línea de comandos debe contener:</span><span class="sxs-lookup"><span data-stu-id="d6eb0-110">The command line should contain:</span></span>
    -   <span data-ttu-id="d6eb0-111">Nombre del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-111">The name of the sample.</span></span>
    -   <span data-ttu-id="d6eb0-112">Nombre del archivo PFX que contiene el certificado inscrito.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="d6eb0-113">Una contraseña asociada con el archivo PFX.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="d6eb0-114">Lee el archivo PFX, intentando primero el formato Base64 y el formato binario si se produce un error en Base64.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="d6eb0-115">La función DecodeFileW () se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="d6eb0-116">Convierte el certificado inscrito en un **BSTR** y lo utiliza para inicializar un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="d6eb0-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="d6eb0-117">La función convertWszToBstr se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="d6eb0-118">Instala el certificado en el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="d6eb0-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6eb0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6eb0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6eb0-120">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="d6eb0-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="d6eb0-121">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="d6eb0-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



