---
description: Inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar del certificado y la descripción del certificado.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687759"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="dea60-103">enrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="dea60-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="dea60-104">El ejemplo enrollSimpleMachineCert inscribe un equipo en una jerarquía de certificados mediante una plantilla, un nombre para mostrar del certificado y la descripción del certificado.</span><span class="sxs-lookup"><span data-stu-id="dea60-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="dea60-105">Location</span><span class="sxs-lookup"><span data-stu-id="dea60-105">Location</span></span>

<span data-ttu-id="dea60-106">Cuando se instala el kit de desarrollo de software (SDK) de Microsoft Windows, se instala una versión de C++ del ejemplo, de forma predeterminada, en la carpeta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VC \\ EnrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="dea60-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="dea60-107">Se instala una versión de VBScript en la carpeta *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Enrollment \\ VBS \\ EnrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="dea60-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="dea60-108">Debate</span><span class="sxs-lookup"><span data-stu-id="dea60-108">Discussion</span></span>

<span data-ttu-id="dea60-109">El ejemplo enrollSimpleMachineCert:</span><span class="sxs-lookup"><span data-stu-id="dea60-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="dea60-110">Procesa los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="dea60-110">Processes the command line arguments.</span></span> <span data-ttu-id="dea60-111">La línea de comandos debe contener el nombre de la plantilla, un nombre para mostrar del certificado y una descripción del certificado.</span><span class="sxs-lookup"><span data-stu-id="dea60-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="dea60-112">Crea un objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) y lo Inicializa utilizando la plantilla especificada en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="dea60-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="dea60-113">El valor ContextAdministratorForceMachine para el primer parámetro especifica que un administrador que actúa en nombre de un equipo solicita el certificado.</span><span class="sxs-lookup"><span data-stu-id="dea60-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="dea60-114">Agrega el nombre para mostrar y la descripción al objeto de inscripción.</span><span class="sxs-lookup"><span data-stu-id="dea60-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="dea60-115">Intenta inscribir la solicitud de certificado y comprueba el estado del proceso.</span><span class="sxs-lookup"><span data-stu-id="dea60-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="dea60-116">La función checkEnrollStatus se define en enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="dea60-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dea60-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dea60-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea60-118">Usar los ejemplos incluidos</span><span class="sxs-lookup"><span data-stu-id="dea60-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



