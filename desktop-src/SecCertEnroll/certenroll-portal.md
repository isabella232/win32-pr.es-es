---
description: Ejemplo de certificado. Cree aplicaciones para la certificación de API, instale el certificado SSL, el certificado de servidor, cree un certificado a través de medios, como Internet o una intranet, que no son intrínsecamente seguros.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de inscripción de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541806"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="e3082-104">API de inscripción de certificado</span><span class="sxs-lookup"><span data-stu-id="e3082-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="e3082-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="e3082-105">Purpose</span></span>

<span data-ttu-id="e3082-106">La API de inscripción de certificados se puede usar para crear una aplicación cliente para solicitar un certificado e instalar una respuesta de certificado.</span><span class="sxs-lookup"><span data-stu-id="e3082-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="e3082-107">Esta API se implementa en CertEnroll.dll a partir de Windows Vista; reemplaza Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="e3082-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e3082-108">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="e3082-108">Developer audience</span></span>

<span data-ttu-id="e3082-109">La API de inscripción de certificados es para su uso por parte de desarrolladores de aplicaciones que permitirán a los usuarios crear, solicitar y recuperar certificados a través de medios, como Internet o una intranet, que no son intrínsecamente seguros.</span><span class="sxs-lookup"><span data-stu-id="e3082-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="e3082-110">Los desarrolladores deben estar familiarizados con los lenguajes de programación de C y C++, el modelo de objetos componentes (COM) y el entorno de programación basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="e3082-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="e3082-111">Aunque no es necesario, se recomienda comprender la infraestructura de clave pública y criptografía.</span><span class="sxs-lookup"><span data-stu-id="e3082-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e3082-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e3082-112">Run-time requirements</span></span>

<span data-ttu-id="e3082-113">La API de inscripción de certificados se admite a partir de Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3082-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="e3082-114">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="e3082-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e3082-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e3082-115">In this section</span></span>



| <span data-ttu-id="e3082-116">Tema</span><span class="sxs-lookup"><span data-stu-id="e3082-116">Topic</span></span>                                                                                       | <span data-ttu-id="e3082-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3082-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3082-118">Acerca de la API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="e3082-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="e3082-119">Se describen los conceptos clave de las solicitudes de certificados.</span><span class="sxs-lookup"><span data-stu-id="e3082-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="e3082-120">Uso de la API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="e3082-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="e3082-121">Cómo usar la API de inscripción de certificados para ampliar las capacidades de Active Directory servicios de Certificate Server.</span><span class="sxs-lookup"><span data-stu-id="e3082-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="e3082-122">Referencia de API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="e3082-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="e3082-123">Descripciones detalladas de las interfaces, las enumeraciones y otros elementos de programación que se pueden usar para inscribir un usuario o un equipo en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="e3082-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




